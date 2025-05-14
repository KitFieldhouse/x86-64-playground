<!-- @migration-task Error while migrating Svelte code: can't migrate `let termref;` to `$state` because there's a variable named state.
     Rename the variable and try again or migrate by hand. -->
<script lang='ts'>
  import { run } from 'svelte/legacy';

  import {blinkStore, term_buffer, sharedState} from '../core/store'

  let blink = blinkStore.getInstance()
  let termref : HTMLElement = $state();

  function scroll(){
    if(termref != null){
      requestAnimationFrame(()=>{
          termref.scrollTop = termref.scrollHeight;
      })
    }
  }
  // Scroll the terminal wen the program state 
  // or the terminal buffer change
  run(() => {
    ($term_buffer || $sharedState) && scroll()
  });

</script>

<div class="term" bind:this={termref}>
  <div class="term__codewrap">
    <code >{$term_buffer}</code>
  </div>
{#if $sharedState == blink.states.PROGRAM_STOPPED}
    <p class="stopinfo">{blink.stopReason.details}</p>
{/if}
</div>


<style>
  .term{
    background-color: rgb(0,0,0,0.4);
    background-color: var(--theme-panel-bg);
    padding: .5rem;
    padding-left: 0;
    font-family: var(--code-font-family);
    overflow: auto;
    height: 100%;
    display: flex;
    flex-direction: column;
  }
  .term__codewrap{
    padding-left: 1rem;
    flex-grow: 1;
  }
  .term code {
    font-size: .9rem;
    text-align: left;
    white-space: pre;
    word-spacing: normal;
    word-break: normal;
    word-wrap: normal;
    line-height: 1.5;
  }
 .stopinfo{
    /*TODO: remove hardcoded colors, find proper design */
    background-color: rgb(224, 73, 35);
    background-color: rgb(96, 48, 36);
    color: white;
    border: 1px solid rgb(245, 127, 97);

    padding-left: 1rem;
  }
</style>
