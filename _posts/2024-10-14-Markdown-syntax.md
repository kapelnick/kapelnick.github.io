**Markdown Syntax**:

To make a phrase _italic_ in Markdown, you can surround words with an underscore (`_` ). For example, `_this_` word would become _italic_.

Similarly, to make phrases **bold** in Markdown, you can surround words with two asterisks ( `**` ). This will `**really**` get your point across.

For the final exercise in this lesson, we're going to make some words _bold_ **_and_** _italic_. In general, it doesn't matter which order you place the asterisks or underscores. Place the asterisks `**_on the outside_**`, just to make it more legible.

To make headers in Markdown, you preface the phrase with a hash mark (`#`). You place the same number of hash marks as the size of the header you want. For example, for a header one, you'd use one hash mark (`# Header One`), while for a header three, you'd use three (`### Header Three`).

There are two different link types in Markdown, but both render the exact same way.

The first link style is called an _inline link_. To create an inline link, you wrap the link text in brackets ( `[ ]` ), and then you wrap the link in parenthesis ( `( )` ). For example, to create a hyperlink to www.github.com, with a link text that says, Visit GitHub!, you'd write this in Markdown: `[Visit GitHub!](`[www.github.com](http://www.github.com)`)`.

The other link type is called a _reference_ link. As the name implies, the link is actually a reference to another place in the document. Here's an example of what we mean:

     Here's [a link to something else][another place].

     Here's [yet another link][another-link].

     And now back to [the first link][another place].

     [another place]: www.github.com

     [another-link]: www.google.com

Images also have two styles, just like links, and both render the exact same way. The difference between links and images is that images are prefaced with an exclamation point ( `!` ).

The first image style is called an _inline image link_. To create an inline image link, enter an exclamation point ( `!` ), wrap the alt text in brackets ( `[ ]` ), and then wrap the link in parenthesis ( `( )` ). (Alt text is a phrase or sentence that describes the image for the visually impaired.)

For example, to create an inline image link to https://octodex.github.com/images/bannekat.png, with an alt text that says, Benjamin Bannekat, you'd write this in Markdown: 

`![Benjamin Bannekat](`[https://octodex.github.com/images/bannekat.png](https://octodex.github.com/images/bannekat.png)`)`.

For a reference image, you'll follow the same pattern as a reference link. You'll precede the Markdown with an exclamation point, then provide two brackets for the alt text, and then two more for the image tag, like this: `![The founding father][Father]` At the bottom of your Markdown page, you'll define an image for the tag, like this: `[Father]:` [http://octodex.github.com/images/founding-father.jpg](http://octodex.github.com/images/founding-father.jpg).

If you need to call special attention to a quote from another source, or design a pull quote for a magazine article, then Markdown's _blockquote_ syntax will be useful. A blockquote is a sentence or paragraph that's been specially formatted to draw attention to the reader. To create a block quote, all you have to do is preface a line with the "greater than" caret (`>`).

There are two types of lists in the known universe: unordered and ordered. That's a fancy way of saying that there are lists with bullet points, and lists with numbers.

To create an unordered list, you'll want to preface each item in the list with an asterisk ( `*` ). Each list item also gets its own line.

All right! That's how you write an unordered list. Now, let's talk about ordered ones. An ordered list is prefaced with numbers, instead of asterisks.

Occasionally, you might find the need to make a list with more depth, or, to _nest_ one list within another. Have no fear because the Markdown syntax is exactly the same. All you have to do is to remember to indent each asterisk _one space more_ than the preceding item.

To create this sort of text, your paragraph must start on a line all by itself underneath the bullet point, and it must be indented by at least one space. For example, the list above looks like this in Markdown:

1. Crack three eggs over a bowl.

 Now, you're going to want to crack the eggs in such a way that you don't make a mess.

This is what's known as a _hard break_; what our poetry asks for is a _soft break_. You can accomplish this by inserting two spaces _after_ each new line. This is not possible to see, since spaces are invisible, but it'd look something like this:

Do I contradict myself?··

Very well then I contradict myself,··

(I am large, I contain multitudes.)

Each dot ( `·` ) represents a space on the keyboard.
