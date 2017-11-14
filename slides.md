## Why Reveal.js?

SLIDE
## Step 1: Clone

SLIDE
## Step 2: Update index.html
### And delete the things
- README
- LICENSE

SLIDE
## Step 3: Plugins
#### Bottom of Index.html
```javascript
dependencies: [
  { src: 'plugin/markdown/marked.js' },
  { src: 'plugin/markdown/markdown.js' },
  { src: 'plugin/notes/notes.js', async: true },
//{ src: 'plugin/highlight/highlight.js', async: true, callback: function() { hljs.initHighlightingOnLoad(); } },
  { src: 'plugin/zoom-js/zoom.js', async: true },
  { src: 'node_modules/reveal_external/external/external.js', async:true },
  { src: '//cdn.socket.io/socket.io-1.3.5.js', async: true },
  { src: 'plugin/multiplex/client.js', async: true }
]
```
https://github.com/hakimel/reveal.js/wiki/Plugins,-Tools-and-Hardware

SLIDE
## Step 4: Configuration
```javascript
<script>
  // More info about config & dependencies:
  // https://github.com/hakimel/reveal.js#configuration
  const factor = .75 //.875
  Reveal.initialize({
    width: 1600 * factor,
    height: 900 * factor,
    history: true,
            markdown: {
                smartypants: true,
                highlight: function (code, language) {
                    return Prism.highlight(code, Prism.languages[language]);
                }
            }...
    dependencies: ...
  })
</script>
```
<!-- .element class="stretch" data-trim contenteditable -->

SLIDE
## Step 5: Slides

VSLIDE
## We just went down!

VSLIDE
## Now you are in the basement level

```markdown
#SLIDE
## Step 5: Slides

#VSLIDE
## We just went down!

#VSLIDE
## Now you're in the basement level
```

```html
<div class="reveal">
  <div class="slides">
    <section data-markdown="slides.md" data-separator="^SLIDE$" data-separator-vertical="^VSLIDE$" />
  </div>
</div>
```

SLIDE
## Step 6: Code Snippets
### Have you noticed some code blocks are bigger than others?
- `<!-- .element class="stretch" data-trim contenteditable -->`
- `class="stretch"` to the rescue
- `contenteditable` works if using HTML

SLIDE
## Step 7: Fragments
1. Fragments let you apply styles <!-- .element: class="fragment" -->
  - (but not in markdown) <!-- .element: class="fragment" -->
1. And step through your content <!-- .element: class="fragment" -->

```markdown
1. Fragments let you apply styles <!-- .element: class="fragment" -->
  - (but not in markdown) <!-- .element: class="fragment" -->
1. And step through your content <!-- .element: class="fragment" -->
```
<!-- .element: class="fragment" -->

VSLIDE
## You can use HTML to do fancier things

```html
<div class="fragment fade-down" data-fragment-index="3">Appears last</div>
<div class="fragment fade-up" data-fragment-index="1">Appears first</div>
<div class="fragment fade-right" data-fragment-index="2">
Appears <span class="fragment highlight-red">second</span>
</div>
```

<div class="fragment fade-down" data-fragment-index="3">Appears last</div>
<div class="fragment fade-up" data-fragment-index="1">Appears first</div>
<div class="fragment fade-right" data-fragment-index="2">
Appears <span class="fragment highlight-red">second</span>
</div>

SLIDE
## Step 8: Notes
note:
- Speaker things only
- would go here

SLIDE
## Step 9: Publish

SLIDE
## Step 10: Present
