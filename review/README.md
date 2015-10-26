# Review

HTML is still a bit sloppy, but functionally correct. This:

```html
<p>The <abbr title="Hypertext markup Language">HTML</abbr> <em>Article Element</em> (<code>&lt;article&gt;</code>) represents a
  self-contained composition in a document, page, application, or site,
  which is intended to be independently distributable or reusable (e.g.,
  in syndication). This could be a forum post, a magazine or newspaper article, a blog
  entry, an object, or any other independent item of content. Each
  <code>&lt;article&gt;</code> should be identified, typically by including a heading
  (h1-h6 element) as a child of the <code>&lt;article&gt;</code> element. <br> <em>Content
  categories</em>: FLow content, sectioning content, palpable
  content.</br>
</p>
```

Should be this:

```html
<p>
  The <abbr title="Hypertext markup Language">HTML</abbr>
  <em>Article Element</em> (<code>&lt;article&gt;</code>) represents a
  self-contained composition in a document, page, application, or site,
  which is intended to be independently distributable or reusable (e.g.,
  in syndication). This could be a forum post, a magazine or newspaper
  article, a blog entry, an object, or any other independent item of
  content. Each <code>&lt;article&gt;</code> should be identified,
  typically by including a heading (h1-h6 element) as a child of the
  <code>&lt;article&gt;</code> element.
</p>
<p>
  <em>Content categories</em>: FLow content, sectioning content,
  palpable content.
</p>
```

No break tags (which are wrong, BTW -- no slash, and if you did use a slash (for XHTML), it would be on the other side of the br: `<br/>`). They just don't belong. Forget you ever saw `<br>` tags. Virtually everyone misuses them. They are rarely needed, and only when you need a line to break in a specific spot, such as in poetry or formatting an address.

They are NOT for making paragraphs. They are NOT for adding space, or eliminating the space between paragraphs. Those are styling issues and must be handled by CSS. Remember separation of concerns.

Watch your indentation. Open and closing tags should line up, with content indented two spaces. Your indentation gets greater as you go down the page. This is far from the worst I've seen, but why not make it perfect? Attention to detail is key in programming. It will serve you well to develop that skill.

On the JavaScript, please don't copy and paste from the console. Type it in your `functions.js` file and the copy and paste TO the console. Your code in the `functions.js` file should be runnable as is.

Your cube function returns the square, not the cube. Add one more `* x` in there.

Good use of the conditional on the absolute function. You can simplify it by using a "guard" condition for the unusual case (negative input) and just returning the same number for every other case. As `return` ends the function call immediately, you can skip the `else` block. Also, instead of multiplying by -1, you can just use the negation operator `-`:

```js
function absolute (n) {
  if (n < 0) return -n

  return n
}
```

Make sense?

Is it just me, or are the other files empty? What happened there?

