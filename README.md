# agendaCreator 

Planning tool for a new semester. 
The loop will create a number of similar agendas in the mardown format.

Idea: genrate the markdown agendas via the loop. Fill in the lesson details.
Add bibliographies.

At the end of the semester creating a compiled version with literature and other sources will be relatively easy.

* agenda - improved by Occam's razor to a oneliner.
* loop - the first version with cunning loops.

## Run agendas

You can run the bash file like this in a terminal window

  ./agendas

The result is somethink like this in the folder */output*:

~~~~
crea001.md
crea002.md
crea003.md
crea004.md
crea005.md
crea006.md
crea007.md
crea008.md
crea009.md
crea010.md
crea011.md
crea012.md
crea013.md
crea014.md
crea015.md
~~~~

# The agendas

The agendas will look somewhat like this, 
depending on how you edit template.md

~~~~
# Day x

## The text: [@HTMLCSS] kap. x

## Agenda

* 09:00 - 10:00 Presence. 
* Pause 
* 10:20 - 11:30
* Frokost
* 12:00 - 13:00
* Pause
* 13:15 - 14:30

## Exercise

## Before next lesson read: [-@HTMLCSS] kap. X
~~~~

The file is also an example of how you format a markdown file.

## Pandoc

With pandoc you can compile the file to many fileformats such as:

* .odt
* .pdf (requires Latex)
* .html
* .tex
* and even (oh horror and gnashing of teeth) ... .docx

The line containing [@HTMLCSS] will add a book from the bibliography.
HTMLCSS is the shorthand name given in the bibliographer file:

~~~~
@Book{HTMLCSS,
  Author         = {Ullman, Larry},
  Title          = {P{HP} for the {W}eb},
  Publisher      = {Peachpit Press},
  year           = 2011
}
~~~~


## Compile pandoc

Here's how to compile pandoc with bibliography and table of contents (toc):

  # pandoc myText.md --bibliography=bogliste.bib -o test.pdf
