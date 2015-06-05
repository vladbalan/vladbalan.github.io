---

title: Markdown syntax test
layout: default

---
[TOC]

# H1: The quick brown fox jumped over the lazy dog

## H2: The quick brown fox jumped over the lazy dog

### H3: The quick brown fox jumped over the lazy dog

#### H4: The quick brown fox jumped over the lazy dog

##### H5: The quick brown fox jumped over the lazy dog

###### H6: The quick brown fox jumped over the lazy dog

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1: The quick brown fox jumped over the lazy dog
======

Alt-H2: The quick brown fox jumped over the lazy dog
------

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~


1. First ordered list item
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

   To have a line break without a paragraph, you will need to use two trailing spaces.  
   Note that this line is separate, but within the same paragraph.  
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses


[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com


Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"


Inline `code` has `back-ticks around` it.


```javascript
Template.Main.events({
    'submit .contact-form': function(e) {
        e.preventDefault();

        var input = {
            name: 'Jon Doe' // $(e.target).find('[name=name]').val()
            , email: 'bla@bla.bla' // $(e.target).find('[name=email]').val()
            , message: 'Test message' // $(e.target).find('[name=message]').val()
        }
        
        var valid = emailRegex.test(input.email) && !_.isEmpty(input.name) && !_.isEmpty(input.email) && !_.isEmpty(input.message);

        if (valid) {
            Meteor.call('message', input, function (err, result) {
                if (err) {
                    console.error('Error sending message: ' + err.reason);
                } else {
                    console.info('Message Sent Successfully. Thank You!');
                }
            });
        }
    }
});
```
 
```php
public function fetch()
{
    return [
        'name' => $this->getName($this->controllerName),
        'collection' => $this->getCollection(),
        'resource' => $this->getResource(),
        'model' => $this->getModel(),
        'namespace' => $this->getNamespace()
    ];
}

/**
 * Format the name of the controller.
 *
 * @return string
 */
private function getName()
{
    return ucwords($this->controllerName); // LessonsController
}
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

```css
#bottom_page ul p{
    padding: 0 14px;
    line-height: 34px;
    margin-bottom: 0;
    display: inline;
    float: left;
    border-right: 1px solid rgba(0, 0, 0, 0.15);
}

em {
    color: #777777;
}

.post_content pre {
    border: 1px solid #ddd;
    background-color: #eef;
    padding: 0 .4em;
}

.post_content ul,
.post_content ol {
    margin-left: 1.35em;
}

```

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

