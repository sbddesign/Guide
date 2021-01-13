---
layout: guide
title: Formatting
description: Visual examples of formatting options available for content authors.
nav_order: 11
parent: Contribute
permalink: /guide/contribute/formatting/
image: /assets/images/guide/contribute/formatting-preview.jpg
---

# Formatting

This page showcases the various formatting and layout options available for content. This allows editors to better understand their toolbox and access reference code. It also allows for designers to see the design system in one place. The design source file is a public Figma community file you can find [here](https://www.figma.com/community/file/862622015964353400/Bitcoin-Designers-site). To improve the design, please start with the Figma file and make a proposal in Slack or Github before implementing.


## Basic markdown formatting

We use [Markdown](https://daringfireball.net/projects/markdown/) when writing content. Markdown is a plain-text formatting syntax that helps us better prepare our text for the web. Below you can find an overview of commonly used syntax elements.

### Text formatting

Text can be **bold**, _italic_, or ~~strikethrough~~.

```markdown
**bold**
_italic_
~~strikethrough~~
```
There should be whitespace between paragraphs.

### Headers

```markdown
# h1
## h2
### h3
#### h4
##### h5
###### h6
```

# h1 header
## h2 header
### h3 header
#### H4 header
##### h5 header
###### h6 header

### Blockquote

```markdown
> This is a blockquote text.
```

> This is a blockquote text.


### Links

### External Links

```markdown
[Link to another page](https://bitcoin.org/bitcoin.pdf)
```

[Link to another page](https://bitcoin.org/bitcoin.pdf).

#### Internal links

```markdown
[Linking]({{ '/guide/getting-started/why-bitcoin-is-unique/' | relative_url }})
```
[Linking]({{ '/guide/getting-started/why-bitcoin-is-unique/' | relative_url }})

### Images

Let's start with a very wide image that extends beyond the content with on desktops. Note how a different image is shown on mobile. This can be used to reformat image content to a portrait format.

{% raw %}
```liquid
{% include picture.html
   image = "/assets/images/style/example-image-wide-desktop.jpg"
   retina = "/assets/images/style/example-image-wide-desktop@2x.jpg"
   mobile = "/assets/images/style/example-image-wide-mobile.jpg"
   mobileRetina = "/assets/images/style/example-image-wide-mobile@2x.jpg"
   alt-text = "Example image"
   width = 1600
   height = 800
   layout = "full-width"
%}
```
{% endraw %}

{% include picture.html
   image = "/assets/images/style/example-image-wide-desktop.jpg"
   retina = "/assets/images/style/example-image-wide-desktop@2x.jpg"
   mobile = "/assets/images/style/example-image-wide-mobile.jpg"
   mobileRetina = "/assets/images/style/example-image-wide-mobile@2x.jpg"
   alt-text = "Example image"
   width = 1600
   height = 800
   layout = "full-width"
%}

#### Image fits content width

{% raw %}
```liquid
{% include picture.html
   image = "/assets/images/style/example-image-wide-desktop.jpg"
   retina = "/assets/images/style/example-image-wide-desktop@2x.jpg"
   mobile = "/assets/images/style/example-image-wide-mobile.jpg"
   mobileRetina = "/assets/images/style/example-image-wide-mobile@2x.jpg"
   alt-text = "Example image"
   width = 1600
   height = 800
%}
```
{% endraw %}

{% include picture.html
   image = "/assets/images/style/example-image-wide-desktop.jpg"
   retina = "/assets/images/style/example-image-wide-desktop@2x.jpg"
   mobile = "/assets/images/style/example-image-wide-mobile.jpg"
   mobileRetina = "/assets/images/style/example-image-wide-mobile@2x.jpg"
   alt-text = "Example image"
   width = 1600
   height = 800
%}
### Image inline with the content

Images can also be inline with the content. This one is inline on desktop, but takes the full screen width on mobile.

{% raw %}
```liquid
<div class="center" markdown="1">

{% include image.html
   image = "/assets/images/style/example-image-square.jpg"
   retina = "/assets/images/style/example-image-square@2x.jpg"
   alt-text = "Example image"
   width = 400
   height = 400
   layout = "float-left-desktop"
%}
```
{% endraw %}

<div class="center" markdown="1">

{% include image.html
   image = "/assets/images/style/example-image-square.jpg"
   retina = "/assets/images/style/example-image-square@2x.jpg"
   alt-text = "Example image"
   width = 400
   height = 400
   layout = "float-left-desktop"
%}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus rhoncus ultricies sapien, sed facilisis justo tristique a. Cras faucibus elementum neque. Quisque ac gravida metus. Vestibulum vehicula lobortis magna quis luctus. Donec lorem erat, convallis imperdiet mattis at, pretium id quam. Curabitur lobortis tincidunt neque.

</div>

#### Image inline on mobile and desktop

This next image is inline on both mobile and desktop.

{% raw %}
```liquid
<div class="center" markdown="1">

{% include image.html
   image = "/assets/images/style/example-image-square.jpg"
   retina = "/assets/images/style/example-image-square@2x.jpg"
   alt-text = "Example image"
   width = 100
   height = 100
   layout = "float-left"
%}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus rhoncus ultricies sapien, sed facilisis justo tristique a. Cras faucibus elementum neque. Quisque ac gravida metus. Vestibulum vehicula lobortis magna quis luctus. Donec lorem erat, convallis imperdiet mattis at, pretium id quam. Curabitur lobortis tincidunt neque.

</div>
```
{% endraw %}

<div class="center" markdown="1">

{% include image.html
   image = "/assets/images/style/example-image-square.jpg"
   retina = "/assets/images/style/example-image-square@2x.jpg"
   alt-text = "Example image"
   width = 100
   height = 100
   layout = "float-left"
%}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus rhoncus ultricies sapien, sed facilisis justo tristique a. Cras faucibus elementum neque. Quisque ac gravida metus. Vestibulum vehicula lobortis magna quis luctus. Donec lorem erat, convallis imperdiet mattis at, pretium id quam. Curabitur lobortis tincidunt neque.

</div>

### Lists

Breaking down content into lists is useful for readability. Here are examples of different list types.

#### Unordered list:

```markdown
*   Item foo
*   Item bar
*   Item baz
*   Item zip
```
*   Item foo
*   Item bar
*   Item baz
*   Item zip

#### Ordered list:

```markdown
1.  Item one
1.  Item two
1.  Item three
1.  Item four
```
1.  Item one
1.  Item two
1.  Item three
1.  Item four

#### Nested list

```markdown
- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item
```
- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

#### Nesting an ol in ul in an ol

```markdown
- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
  1. level 4 item (ol)
  1. level 4 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)
```
- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
  1. level 4 item (ol)
  1. level 4 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)

#### Task list

```markdown
- [ ] Hello, this is a TODO item
- [ ] Hello, this is another TODO item
- [x] Goodbye, this item is done
```
- [ ] Hello, this is a TODO item
- [ ] Hello, this is another TODO item
- [x] Goodbye, this item is done

#### Definition with HTML syntax.

```markdown
<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>
```
<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

### Tables

```markdown
| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |
```

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### Code embedding

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```


### There's a horizontal rule below this.
```markdown
* * *
```
* * *

### Embedding content from external sources

#### YouTube video embed

```markdown
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/zKMRSLbQEqk/mqdefault.jpg)](https://www.youtube.com/watch?v=zKMRSLbQEqk)
```
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/zKMRSLbQEqk/mqdefault.jpg)](https://www.youtube.com/watch?v=zKMRSLbQEqk)

#### Figma embed

Figma embeds are automatically resized to comfortable fit into the visible screen area.

```html
<div class="figma-embed">
<iframe width="450" height="1000" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FHggAJoHhLXPH0oZQEr1D4D%2FBitcoin-Design-Guide%3Fnode-id%3D166%253A0%26viewport%3D1714%252C3489%252C1%26scaling%3Dmin-zoom" allowfullscreen></iframe>
</div>
```

<div class="figma-embed">
<iframe width="450" height="1000" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FHggAJoHhLXPH0oZQEr1D4D%2FBitcoin-Design-Guide%3Fnode-id%3D166%253A0%26viewport%3D1714%252C3489%252C1%26scaling%3Dmin-zoom" allowfullscreen></iframe>
</div>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```

[^1]: https://bitcoin.design "Footnote with a caption"