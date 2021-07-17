# resume-pandoc

LaTeX resume template for Pandoc based on John Bokma's resume-pandoc repository
https://github.com/john-bokma/resume-pandoc

## Snippets
I have written the script `compilemd` for generating tailored resumes using snippets.
These can be included your markdown files using the following syntax

~~~
incsnip example_content/summary/summary1.md
~~~

I've included an example cv to show usage of incsnip and YAML within the file.

To compile markdown from snippets, use:

~~~
tools/compilemd example_cv.md compiled/md/example_cv.md
~~~

To create the PDF, use:

~~~
tools/mdtopdf compiled/md/example_cv.md compiled/pdf/example_cv.pdf
~~~

For a more convient way to complete both of these steps at once, use:

~~~
./compile example_cv.md
~~~


## YAML Meta Block

name
 : the name on the resume.

keywords
 : keywords to be added to the PDF file.

left-column
 : a list of lines you want in the left column, directly under the name
   on the first page.

right-column
 : a list of lines you want in the right column, directly under the
   name on the first page.

fontsize
 : default `10pt`.

fontenc
 : default `T1`.

urlcolor
 : used in PDF, default `blue`.

linkcolor
 : used in PDF, default `magenta`.

numbersections
 : number sections, default off. Can also be controlled using the
 `pandoc` option `-N, --number-sections`.

name-color
 : the SVG name of the font color used for your name on the
 resume. For example `DarkSlateGray`. Note that this option
 also changes the font used for your name to bold and sans serif.

section-color
 : the SVG name of the font color used for sections. For example
 `Tomato`.  Note that this option also changes the section font to
 bold and sans serif.

Regarding the last two options: if you just want to change the font to
sans serif bold you can just use the color `black`.

# Example PDF

See [example](https://github.com/Nan0Scho1ar/resume-pandoc/blob/master/compiled/pdf/example_cv.pdf)

# Credits

- John Bokma for creating the LaTeX pandoc template.
- Jason R. Blevins for making the LaTeX resume example that inspired this
  template.
- Christoph Frings and Andrew for their help with description list; reference
  [enumitem: multiline label with text following label - TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/questions/323903/enumitem-multiline-label-with-text-following-label).
