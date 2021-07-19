# Get active tab URL

Should be executed in [background script](https://developer.chrome.com/docs/extensions/mv3/background_pages/).
[Tabs permissions](https://developer.chrome.com/docs/extensions/reference/tabs/#manifest) should be set in `manifest.json`.

```javascript
chrome.tabs.query({active: true, currentWindow: true}, function(tabs) {
  var tab = tabs[0];
  console.log(tab.url);
});
```

- chrome.tabs.query - returns tabs list based on query
- active: true, currentWindow: true - we want active tab
- tab = tabs\[0\] - we expect only one tab in the result list, which is a curent tab
- console.log(tab.url) - log tab URL to console

group: active_tab