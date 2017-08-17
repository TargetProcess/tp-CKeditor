# tp-CKeditor
CKEditor build for targetprocess

This CKeditor build has patch that disable auto inline CKEditor.
```js
CKEDITOR.disableAutoInline=true;
```
This build has reverted context menu patch. Native browser menu open with `Rightclik`, CKEditor's menu with `Ctrl/CMD + Rightclick`

BEFORE
`a.on("contextmenu",function(a){a=a.data;var c=CKEDITOR.env.webkit?f:CKEDITOR.env.mac?a.$.metaKey:a.$.ctrlKey;if(!e||`**!**`c){a.preventDefault()`

AFTER
`a.on("contextmenu",function(a){a=a.data;var c=CKEDITOR.env.webkit?f:CKEDITOR.env.mac?a.$.metaKey:a.$.ctrlKey;if(!e||c){a.preventDefault()`