# tp-CKeditor
CKEditor build for targetprocess

This CKeditor build has patch that disable auto inline CKEditor.
```js
CKEDITOR.disableAutoInline=true;
```
This build has reverted context menu patch. Native browser menu open with `Rightclik`, CKEditor's menu with `Ctrl/CMD + Rightclick`

BEFORE
`a.on("contextmenu",function(a){a=a.data;var b=CKEDITOR.env.webkit?d:CKEDITOR.env.mac?a.$.metaKey:a.$.ctrlKey;if(!f||`**!**`b)if(a.preventDefault()`

AFTER
`a.on("contextmenu",function(a){a=a.data;var b=CKEDITOR.env.webkit?d:CKEDITOR.env.mac?a.$.metaKey:a.$.ctrlKey;if(!f||b)if(a.preventDefault()`