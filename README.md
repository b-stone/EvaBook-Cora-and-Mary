# Cora and Mary

An example of using pandoc and markdown to create pdf's ready to publish on Amazon's CreateSpace.

This framework is currently built around the creation of a pdf that will stay within the required margins presented by CreateSpace here:

https://www.createspace.com/Products/Book/InteriorPDF.jsp

## Requirements

This setup uses pandoc: http://johnmacfarlane.net/pandoc/ to output the content of the book in various formats (primarily pdf).

As such, it requires _pandoc_ to be installed on your machine. 

For _Mac_, homebrew has an install.

     brew install pandoc

That got most of it working for me.

It also uses Latex. Specifically, the XeLatex engine. 

### Note on Chapter Titles

Cora and Mary has no chapter titles. Instead, I used a single '#' to denote a header - and the latex template is setup to automatically number the headers. So, I just get a big number for a chapter title in the final pdf (which is what I wanted cause of how many chapters there are). 

## Running

To create the pdf, simple call:

    make pdf

Your pdf should be in the out/ directory. 

Check out the Makefile for other output options. Some of which have additional requirements to install.

If you hit an error, its probably because of a missing font or Latex package. You will need to modify the latex template to make it work.

## Latex Template

The latex template used for the book can be found in:

     _layouts/pdf-template.txt

Here you can customize to your heart's content. The size of the book and the margins will be something you want to consider - as well as the font and font size. I think the margins look pretty good for the 5.5 x 8.5 book size - but you may disagree. And if you want a different book size, then you probably want different margins. 

