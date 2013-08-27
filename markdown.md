# Markdown

Markdown is a lightweight syntax of markup for plain text documents.
It allows us to add semantics and style to our documents without overpowering them with code and angle brackets.

Markdown can easily be converted to HTML and its tags match those found in HTML—there is a one-to-one mapping.

## Files

Markdown files are simply plain text files.
But often the extension of the file is changed to `.md` to signify Markdown syntax.

## Syntax

For paragraphs in Markdown there is no visible syntax,
just write lines of text and separate them by a blank line.
Markdown will automatically convert text with blank lines between into paragraphs.

	This is the first paragraph.
	
	This is the second paragraph of text.

To make something italic, surround it in a single set of asterisks.
To make something bold, surround it in double asterisks.

	Some words are *italic* and some words are **bold**.

Headings are denoted using a hash symbol in front:

	# Heading level 1
	## Heading level 2
	### Heading level 3

Lists are created by putting dashes in front of lines of text:

	- List item 1
	- List item 2
	- List item 3

To add links there is a little more syntax:

	[Link this text](http://url-to-link-to.com/)

To add images, use a syntax similar to links:

	![Image alt attribute](http://url-to-image.com/image.png)

To add horizontal rules, use three dashes:

	This is a paragraph.
	
	---
	
	This is another paragraph, separated by a horizontal rule.

And finally, GitHub supports to-do lists in Markdown files using the following format:

	- [ ] Thing to do
	- [ ] Another thing to do
	- [x] Thing that’s already done

*GitHub will even convert those to checkboxes in specific locations.*

**Read the [syntax documentation](http://daringfireball.net/projects/markdown/syntax) for lots more.**

## Use

One of the most common uses for Markdown files is Readmes.
You’ll notice that GitHub will render your Markdowned Readme file and present it in a styled view.
Just name your Readme `README.md` and GitHub will do the rest.

Another really common use is content preparation for responsive websites.
It’s a really good way to organize and understand the structure of content without forcing HTML upon your authors.

Some Markdown processors are even aware of [YAML Front Matter](http://jekyllrb.com/docs/frontmatter/), that can allow authors to add extra metadata to their documents.

## Resources & tutorials

- <http://en.wikipedia.org/wiki/Markdown>
- <http://daringfireball.net/projects/markdown/>
- <http://daringfireball.net/projects/markdown/basics>
- <http://daringfireball.net/projects/markdown/syntax>

## Apps

- [Dingus](http://daringfireball.net/projects/markdown/dingus)
- [Markdrop](http://www.markdrop.com/)
- [IA Writer](http://www.iawriter.com/)
- [Markded](http://markedapp.com/)
