
# Webflow Notes


## Script for opening relevant blocks when linked to

```
document.addEventListener('load', (event) => {
  // Expand the desired block by triggering a click event
  const el = document.getElementById(id);
  const contentEl = el.getElementsByClassName('expand-block__content')[0];
  const triggerEl = el.getElementsByClassName('expand-block__trigger_icon')[0];
  triggerEl.click();
  // Scroll the title into view (taking the header into account)
  document.getElementsByTagName('html')[0].scrollTop -= 60;
});
```
