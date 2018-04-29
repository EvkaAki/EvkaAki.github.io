---
layout: post
title: "Assignment 2"
date: 2018-03-26
---


The goal of the second assigment was to modify a document (preferably your bachelor thesis) from original format (Microsof Word, OpenOffice, LaTeX,..) to DocBook format and generating the final document in PDF. The document should have between 10 and 15 pages.

### The required control structures are:

+ standard text division to chapter, subchapter, subsubchapter, attachment, generated content
+ highlighting words, highlighting text breaks or numbering
+ links to other parts of your own document, or URL links
+ footnote
+ list of the literature and resources used, including their quotes in the text,
+ insert images and tables, links to them in text; a list of pictures and tables in the opening or closing text,
+ creating a register of concepts with terms

### What is where used in my project:
My original bachelor thesis was written in LaTeX. I will supply you with a PDF version of it.
+ text is divided to two chapters, which are further divided into subchapters and subsubchapters
+ list of content is automatically generated
+ highlighting was at most used in glossary, (__bold__ and _cursive_), but also in other parts of the document
+ cross reference is used in the introduction:

```xml
        <xref linkend="slovensko"/>
    <title  xml:id="slovensko">Slovakiana</title>    
```
+ I have used one footnote that describes what interoperability means
+ list of literature is placed on the end of the document and the citations are exactly o that places, where are in my original bachelor thesis
+ there is only one image inserted (and centered just like original), because there is also only one image in the original document
+ I have used both ordered lists and ordered lists many times thru the whole document
+ I don't have any tables in the original document, therefore I didn't included them here by force
+ Glossary is placed at the end of the document. The fact is, I have already explained almost every specific word in the thesis before, therefore I have chosen dozen of word that are not as usual used as other and put them into glossary.
+ I have changed the text indent, because I my original document is this way.
+ I have deleted the picture on the first page and changed margin of the institute line...and other minor changes in the document.
