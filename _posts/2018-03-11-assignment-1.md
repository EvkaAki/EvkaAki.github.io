---
layout: post
title: "Assignment 1"

---

<!-- date: 2018-03-11  -->
Static webpage using technologies: Git + GitHub Pages + Jekyll + Markdown. Usage of the potential of the static generator Jekyll and it's templating options.
### There has to be used:

+ at least 5 variables
+ collections or data files
+ at least 5 filters or tags
+ at least 1 plugin (besides pagination)


### Evaluation:
+ Structural level of the website (good using of the potential of the tool jekyll)– max 4p
+ Meaningful content of the website (meaningful content, including documentation of the implementation) – max 1p
+ Frontend level (how the website look, overal consistency) – max 0.5p
+ Status of the project in Gihub – max 0.5p

### What is where used in my project:
+ _variables_ are used almost in every page, but all of the projects pages contain more than 5, for example in *bachelorThesis.md* are these
1. layout: project
2. language: laravel
3. title: "Multimedia content in the education process"
4. start_date: 2017-09-02
5. end_date: 2018-04-31
6. subject: bp1
7. number_of_credits: 9
+ I have two different _collections_ used in the project: projects and hobbies.
+ I have used _where_, _date_to_string_ and _date: "%Y"_ filter and number of _tags_ for example in the projects _index.md_ is this for loop:

![code](/assets/code.png "code")


first, it assign only those project implemented in _laravel_ to the "p" variable, the I iterate within this array using for loop. I use if and else statements to determine where to put a comma in the list. ( forloop.rindex outputs how many item are left)
+ I have periodically committed this project to GitHub, you can access the project using link in the footer.
+ I have used jemoji plugin, which can be seen almost on every page of the website
+ There has been used 4 different layouts witch are: {% for layout in site.layouts %}{% if  forloop.rindex == 1 %} {{layout.name}}.{% else %}  {{layout.name}},{% endif %}{% endfor %} (this line is also writen in code, you can see it in _2018-03-11-assigment-1.md_ line 39-40)
