Exploring best options for creating mindmaps summarising key areas of HSMA content.

This uses the web export of [SimpleMind](https://simplemind.eu/) with the output html just renamed to index.html to conform to expected GH pages structure.

Limitations appear to be 
1) the file starting from the top left and
2) click scrolling not being enabled.

### Overcoming limitation 1
Initial scroll position can be changed by passing in the following snippet within the head of the document
Parameter is (x position in pixels, y position in pixels)
```{html}
<script>
function Scrolldown(){
     window.scroll(2200,650);
}
window.onload = Scrolldown;
</script>
```
Will need updating when document changes significantly; is currently manually centred on central node of diagram.

### Overcoming limitation 2 
We can update the html file output to include the following script tag in the head section:
`<script src="dragscroll.js"></script>`

We then just need to update the body class to be `dragscroll`
<body class=dragscroll>

`dragscroll.js` needs to be in the same folder as `index.html`


# Upload process

- Export file from simplemind as website
- Unzip
- Rename html file to index.html
- Open HTML file in editor
- Add `<script src="dragscroll.js"></script>` to head
- update the body class to be `dragscroll`: `<body class=dragscroll>`
- save and close
- ensure `dragscroll.js` is in the same folder as `index.html`
