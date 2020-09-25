# PhosWeb
Web Programming as Easy as 1-2-3

The World Wide Wed has undergone tremendous changes since its inception in ...

http://info.cern.ch/hypertext/WWW/TheProject.html

From the first humble plain text web page at info.cern.ch, to today's literally billions of pages delivered to users' mobile devices and desktop computers, the web is truly the most significant technological presence in human societies, succeeding the roles of the television. 

It is powering the biggest tech companies, led by the top 5 we collectively coin as MAGA+F (Microsoft Apple Google Amazon Facebook), employing millions of programmers world wide, lifting a whole generation of people from poverty, some of them now leading the likes of MAGA+F.

Yet, the complexities introduced in the tools in programming the web have also grown exponentially, creating the danger of worsening global Marxist class struggles, as the likes of MAGA+F (and their employees) pull themselves apart in terms of income and influence from the rest of the mortals.

It is against this background that we ___discovered___ several fundamental techniques now collectively known as __Phosway__, which we hope may address the worsening class struggles, by creating the _Free Software Revolution 2.0_.


## Modifying the Contents of Any Web Page

Let us illustrate what we plan to do with PhosWeb, a component of Phosway, before continuing to explore the far reaching effects of Free Software Revolution 2.0.

1. A typical tutorial on web application development in 2020 may look like this:

- https://www.softwaretestinghelp.com/single-page-application-using-angularjs/

We took a random example from the Internet to illustrate the unnecessary complications with "modern" web applicatoin development tools, when compared to PhosWeb, consisting of a collection of fundamental technologies which greatly trim the unnessary fat.

2. Figure 1 is the result of a web page using Microsoft's LinkedIn as template whose contents have been modified, using the data from a JSON file shown below:

- Figure 1
<img src="https://github.com/udexon/PhosWeb/blob/master/img/LinkedIn.png" width=600>

- Table 1
```
~/devel/PhosWeb/auth$ cat PhosGraph/chat_foxy_20200923_093011 
20200923_093011 foxy {"name":"who am i","age":"born 1982",
"city":"Kuala Lumpur","specialty":"Hainan Chicken Rice","fees":"MYR 100 / hour"}
```

3. This is part of a project called "MasakNet", where "Masak" is the Malay word for "cooking". The aims of this project inclulde:

- to help the people who are cooking at home (due to the current COVID19 pandemic lockdown), to sell and deliver the food to nearby customers.
- to arrange expert chefs to conduct cooking classes, online or off line, to train the people who are cooking at home.

The data in table 1 were added to the HTML file `olt.html` in figure 1 using the following commands (table 2), whose output is shown in figure 2:

- Table 2
```
~/devel/PhosWeb/auth$ php phos.php \
: echo ON ECHO bv: ec: \; \
: w_db ix: olt.html fgh: dup: 3 pick: geid: 0 i: dup: 3 pick: sit: . . . . \; \
: r_db fi: 0 i: gjs: 0 i: jd: \; \
: next_id apop: dup: 4 pick: swap: i: 3 pick: 2 pick: geid: 0 i: dup: \
2 pick: sit: st: nl: ot: echo nl: esp: esp: nl: st: nl: nl: \; \
PhosGraph/chat_foxy_20200923_093011 r_db dup: ak: apop: dup: 3 pick: swap: i: \
ol7.html fgh: dup: 3 pick: geid: 0 i: dup: 3 pick: sit: \
ot: sp: echo nl: echo nl: nl: st: nl: swap: . swap: . st: nl: swap: \
next_id next_id next_id next_id nl:
```

- Figure 2
<img src="https://github.com/udexon/PhosWeb/blob/master/img/dom_mod.png" width=600>

4. We used `simplehtmldom`, a PHP library to modify the contents of `olt.html`.

- https://simplehtmldom.sourceforge.io/manual.htm#section_quickstart

The documentation page seemed to have had little maintainence. As such, we have copied the critical section on finding DOM element by `id` here, together with a screenshot of the documentation page:

- Table 3
```php
// Find all element which id=foo
$ret = $html->find('#foo');
```

In fact, this function returns an array containing exactly ONE element, matching the specified `id`. As such, the comment `Find all element` seems to be both grammatically incorrect and technically problematic.

- Figure 3
<img src="https://github.com/udexon/PhosWeb/blob/master/img/simple_html_dom.png" width=600>

5. We wish to congratulate readers for your patience to read up to this point, as it is inevitable for us to explain the various technical issues with code samples from several seemingly unrelated sources. We wish to highlight that "mainstream" documentation on HTML and DOM have been written in certain ways that obscure the fundamental design and structure of HTML and DOM that we are revealing here:

- (a) HTML is a tree.
- (b) (a) is evident when DOM elements are viewed in the Inspector tab in browser developer tools (press `F12` or right-click "Inspect element" on an element in a web page) (figure 4).

- Figure 4
<img src="https://github.com/udexon/PhosWeb/blob/master/img/DOM_Inspector.png" width=600>

- (c) In figure 2, for example, a DOM element as shown below:

```html
<li class="t-16 t-black t-normal inline-block" id="city">Kuala Lumpur</li>
```
has the following properties, which form part of a tree:
```
tag: li
class: "t-16 t-black t-normal inline-block"
id: "city"
inntertext: Kuala Lumpur
```
- (d) ANY element CAN have `id` property. BUT adding `id` property is a choice left to the programmer.
- (e) `id` is the easiest way to retrieve (access) a DOM element, e.g. JavaScript `getElementById()` function. The PHP function above is apparently derived from the JavaScript function.


6. In a typical web page like Microsoft LinkedIn profile page, as with most other web pages, the `id` property is not fully populated.

When id was absent, we may access the DOM elements using tag name, then add `id`. This involves searching through an array of elements return by the initial search, as illustrated below.

- https://simplehtmldom.sourceforge.io/manual.htm#section_find

- Figure 5
<img src="https://github.com/udexon/PhosWeb/blob/master/img/find_tag.png" width=600>

- Figure 6
<img src="https://github.com/udexon/PhosWeb/blob/master/img/LinkedIn_TagName.png" width=600>
