### Invisible tables

You can arrange text in columns, or otherwise make a table invisible, using
`<table class="columns">...</table>`. This is typically used for arranging
long narrow lists.

<table class="columns">
  <tr>
    <td>
      <code>auto</code><br />
      <code>break</code><br />
      <code>case</code><br />
      <code>char</code>
    </td>
    <td>
      <code>const</code><br />
      <code>continue</code><br />
      <code>default</code><br />
      <code>do</code>
    </td>
    <td>
      <code>double</code><br />
      <code>else</code><br />
      <code>enum</code><br />
      <code>extern</code>
    </td>
  </tr>
</table>

    <table class="columns">
      <tr>
        <td>
          <code>auto</code><br />
          <code>break</code><br />
          <code>case</code><br />
          <code>char</code>
        </td>
        <td>
          <code>const</code><br />
          <code>continue</code><br />
          <code>default</code><br />
          <code>do</code>
        </td>
        <td>
          <code>double</code><br />
          <code>else</code><br />
          <code>enum</code><br />
          <code>extern</code>
        </td>
      </tr>
    </table>


## External links

To mark a link as external, use
`<a href="https://www.google.com/" class="external">External Link</a>` when
authoring in HTML, or append `{: .external}` to links when authoring in
Markdown.

<a href="https://www.google.com/" class="external">External Link</a>



## Custom attributes and named anchors

Markdown supports custom markup attributes for block level HTML elements and
headers.

The format for this allows for a custom class, a custom ID, and/or custom
attribute/value pairs in the same statement:

    This is a paragraph.
    {: .customClass #custom_id attribute='value' }

This generates this HTML:

    <p class="customClass" id="custom_id" attribute="value">This is a paragraph.</p>

### Custom attributes on headers

As headers can only be defined in one line, the attributes list should be
defined at the end of the header definition:

    ## Header with custom ID {: #custom_id }

Generates:

    <h2 id="custom_id">Header with custom ID</h2>

## Block quote

    > Lorem ipsum dolor sit amet, consectetur adipiscing elit.


> Lorem ipsum dolor sit amet, consectetur adipiscing elit.






## Tooltips

Any element that has a `title` attribute will show a tooltip (with the value
of the attribute) on mouseover. For example: "...someday screen
<abbr title="pixels per inch">PPI</abbr> may increase further..."
(note that the dotted underline comes from the abbr element, not the tooltip).


    ...someday screen <abbr title="pixels per inch">PPI</abbr> may increase further...

Warning: Be sure to use tooltips only for supplemental information—not essential text or primary user-experience features—since the presence of tooltips is not obvious and users on mobile devices will not see them at all.


## Miscellaneous classes

Use `class="inline"`, `class="inline-block"`, and `class="block"` to force
inline, inline-block, or block layout, in the rare cases when it is necessary.

Use `class="clearfix"` to clear a floated element, for example after using
`attempt-left` or `attempt-right`.

## Comments

A one-line comment and a multi-line comment have different syntax. Both are
removed from the web pages that are produced when staging or publishing.

### One line comments
A one-line comment. Hash characters (#) used like this are reserved only for
one-line comments.

<pre class="prettyprint">
&#123;# Time travel is fun #}
</pre>

### Multi-line comments
A multi-line comment, with start and end tags surrounding the comment.

<pre class="prettyprint">
&#123;% comment %}
Time travel is fun.
I do it literally all the time.
&#123;% endcomment %}
</pre>
