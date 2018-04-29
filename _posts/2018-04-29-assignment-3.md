---
layout: post
title: "Assignment 2"
date: 2018-03-26
---
The goal of the third assignment was to analyze the possibilities of writing a simple presentation in XML. Our task was to identify the basic elements of the presentation and design XML elements for their tagging. The priority was to focus on the reusability and to avoid redundancy. The elements have to be described using selected language - DTD, XSD or RELAX NG containing an explanation of the purpose of each element. In the language designed by us, we had to demonstrate the possibilities to create presentations according to the document type definition.

As a part of this assignment was this documentation uploaded on the github pages.

### HTML presentation:
- I used Bootstrap 4 for the styling combined with my own stylesheet .css file
- From the html.xsl document are created 1 + n files, in which n equals the number of pages in the input file
- The first page, which is created is the index file, containing list of links to all pages
- The first page is called the "Main page" and as for the others, their element's <title> is used combined with their position number

```xml
<xsl:choose>
    <xsl:when test="position()=1">
        <xsl:variable name="slideName" select="'Main page'"/>
        <xsl:value-of select="concat($slideNumber,'. ', $slideName)"></xsl:value-of>
    </xsl:when>
    <xsl:otherwise>
        <xsl:value-of select="concat($slideNumber,'. ', $slideName)"></xsl:value-of>
    </xsl:otherwise>
</xsl:choose>
```
- Also title on the front page and on all the other pages have different classes assigned, using this block of code:

```xml
<xsl:choose>
    <xsl:when test="parent::page/count(preceding-sibling::page) + 1!=1">
        <xsl:element name="h2">
            <xsl:attribute name="class">mb-5 mt-5 w-100 text-center</xsl:attribute>
            <xsl:apply-templates/>
        </xsl:element>
    </xsl:when>
    <xsl:otherwise>
        <xsl:element name="h1">
            <xsl:attribute name="class">text-center</xsl:attribute>
            <xsl:apply-templates/>
        </xsl:element>
    </xsl:otherwise>
</xsl:choose>
```
### PDF presentation:
- What was a real struggle for me for the pdf version of the presentation, was the nested list, which I accomplished finaly by selecting the nested list separatly from the usual and changing its attributes, only second level of list is supported

### Relax NG validation
- The Relax NG validation is quite simple
- Only second level of list is allowed
- everything, except for title or signature, have to be wrapped in a container
- every page have to have a title and at least one content
