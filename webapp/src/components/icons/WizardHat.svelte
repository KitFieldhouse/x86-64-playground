<script>
  /** @type {{ [key: string]: any }} */
  let { ...props } = $props();
</script>


<!--@component
  Svg Icon
  By default this icon will have a fill of the default foreground color.

  To override a color, use the style attribute with a theme css variable:
  ```tsx
    <Icon style="fill:var(--theme-primary);" />
  ```
  
  By default, this icon will have a height and width of 24px.
  To override:
  ```tsx
    <Icon width="12px" height="12px" />
  ```
-->
<svg 
  xmlns="http://www.w3.org/2000/svg"
  height="24px" 
  width="24px" 
  viewBox="0 0 455 498"
  class="default-fill"
  {...props}
><path d="M147 103c-1 1-2 2-2 5 0 4 0 4-5 5-10 1-8 12 3 12 2 0 2 0 2 4l2 5c4 4 9 1 9-5 0-4 0-4 2-4 7 0 12-5 9-9-2-2-3-3-6-3-4 0-4 0-5-5 0-4-3-7-5-7l-4 2z"/><path d="M241 114c-19 3-37 13-50 29a386 386 0 0 0-65 146 147 147 0 0 0 153-3c8-5 9-7 9-8a1290 1290 0 0 0-18-70c-2-11-2-11 0-12 4-4 17-8 23-9 7 0 12 1 20 6 12 7 16 9 22 9 4 0 5 0 7-3 4-4 2-10-4-24-17-33-41-55-69-60-7-2-22-2-28-1z"/><path d="m75 149-2 8c-2 14-11 23-26 25-6 1-8 3-8 6 0 4 3 6 9 6 9 1 18 8 23 16l2 9c1 5 1 7 3 8 4 3 9 0 9-5 0-7 3-13 9-19s12-9 19-9c3 0 7-3 7-6s-2-5-9-6c-8-1-15-5-20-11-3-4-6-12-6-17l-2-4c-1-2-6-3-8-1z"/><path d="m312 230-1 6c0 3-1 4-5 4l-6 2c-3 5 0 9 6 10 4 1 5 1 5 5 0 5 2 6 5 6 4 0 6-2 6-7 0-4 0-4 3-4 5 0 7-1 8-4 2-4-1-7-7-8-4 0-4 0-4-4l-2-5c-1-2-6-3-8-1z"/><path d="M297 286a139 139 0 0 1-69 33 170 170 0 0 1-108-20l-9-5-32 9c-14 5-22 10-29 16-11 10-13 19-9 30 6 11 18 15 53 17 19 1 32 2 76 8l26 3 4-4c3-3 5-4 10-5l8-2 6-4c3-3 4-4 5-9 2-13 8-20 18-20s16 6 18 19c2 9 7 14 17 16l8 2c3 1 4 1 12-2 16-6 29-14 43-26 18-14 21-24 14-35-6-9-23-16-49-20-11-2-12-2-13-1z"/><path d="M244 346c-2 2-3 3-3 7-2 14-12 24-25 26-6 0-9 2-9 6s2 5 9 6c13 2 23 12 25 25 0 6 2 9 6 9 3 0 6-3 6-7 0-13 14-27 27-27 4 0 7-2 7-6 0-3-3-6-7-6s-13-3-17-7c-5-4-9-12-10-18 0-4-1-6-3-8s-3-2-6 0z"/></svg>

<style>
.default-fill{
  fill: var(--theme-text-fg-contrasting);
}
</style>
