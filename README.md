Twitter-Bootstrap-Cheat-Sheet
=============================

Twitter Bootstrap Cheat Sheet


Twitter BootStrap Cheat Sheet
How to add in static html pages
<link rel="stylesheet/less" href="/path/to/bootstrap.less">
<script src="/path/to/less.js"></script>
How to add in Rails Pages
http://railsapps.github.com/twitter-bootstrap-rails.html
//= require jquery
//= require jquery_ujs
//= require bootstrap
//= require_tree .
Requires HTML5 doctype
Add in every html doctype
1. <!DOCTYPE html>
2. <html lang="en">
3. ...
4. </html>
Typography and links
Within the scaffolding.less file
● Remove margin on the body
● Set background-color: white; on the body
● Use the @baseFontFamily, @baseFontSize, and@baseLineHeight attributes as our typographyic 
base
● Set the global link color via @linkColor and apply link underlines only on :hover
Default grid system1. <div class="row">
2. <div class="span4">...</div>
3. <div class="span8">...</div>
4. </div>
class="row"  -----------------  to create row 
To nest your content, just add a new .row and set of .span* columns within an existing .span* column.
Fluid rows  (Default 940px grid system)
Make any row fluid simply by changing .row to .row-fluid. 
1. <div class="row-fluid">
2. <div class="span12">
3.   Level 1 of column
4.   <div class="row-fluid">
5.     <div class="span6">Level 2</div>
6.     <div class="span6">Level 2</div>
7.   </div>
8. </div>
9. </div>
Layouts Basic templates to create webpages
Fixed layout <div class="container">
The default and simple 940px-wide centered layout for just about any website or page provided by a 
single <div class="container">. 
1. <body>
2. <div class="container">
3.   ...4. </div>
5. </body>
Fluid layout <div class="container-fluid">
<div class="container-fluid"> gives flexible page structure, min- and max-widths, and a left-hand 
sidebar. It's great for apps and docs.
Responsive design Media queries for various devices and 
resolutions
Requires meta tag
To ensure devices display responsive pages properly, include the viewport meta tag.
1.<meta name="viewport" content="width=device-width, initial-scale=1.0">
Lists
Unordered  ---- <ul>
Unstyled  ----  <ul class="unstyled">
Ordered ----  <ol>
Description  ---- <dl>
Horizontal description  ---- <dl class="dl-horizontal">
Inline
Wrap inline snippets of code with <code>.
Basic block
Use <pre> for multiple lines of code. Be sure to escape any angle brackets in the code for proper 
rendering.Google Prettify
Take the same <pre> element and add two optional classes for enhanced rendering.
1.<p>Sample text here...</p>
1.<pre class="prettyprint
2.    linenums">
3. &lt;p&gt;Sample text here...&lt;/p&gt;
4.</pre>
You may optionally add the .pre-scrollable class which will set a max-height of 350px and 
provide a y-axis scrollbar.
Table markup
Tag Description
<table> Wrapping element for displaying data in a tabular format
<thead> Container element for table header rows (<tr>) to label table columns
<tbody> Container element for table rows (<tr>) in the body of the table
<tr> Container element for a set of table cells (<td> or <th>) that appears on a single row
<td> Default table cell
<th> Special table cell for column (or row, depending on scope and placement) labels
Must be used within a <thead>
<caption> Description or summary of what the table holds, especially useful for screen readers
Table options
Name Class Description
Default None No styles, just columns and rows
Basic .table Only horizontal lines between rowsBordered .table-bordered Rounds corners and adds outer border
Zebrastripe
.table-striped Adds light gray background color to odd rows (1, 3, 5, etc)
Condense
d
.table-condensed Cuts vertical padding in half, from 8px to 4px, within all td and th
elements
Get a little fancy with your tables by adding zebra-striping—just add the .tablestriped class.
Condensed table
Make your tables more compact by adding the .table-condensed class to cut table cell padding in half 
(from 8px to 4px).
1.<table class="table table-condensed">
2. …
3.</table>
Bordered table
Add borders around the entire table and rounded corners for aesthetic purposes.
1.<table class="table table-bordered">
2. …
3.</table>
1. <table class="table table-striped table-bordered table-condensed">
2. ...
3. </table>
Four types of forms
Bootstrap provides simple markup and styles for four styles of common web forms.
Name Class Description
Vertical 
(default)
.form-vertical (not 
required)
Stacked, left-aligned labels over controls
Inline .form-inline Left-aligned label and inline-block controls for 
compact style
Search .form-search Extra-rounded text input for a typical search aesthetic
Horizontal .form-horizontal Float left, right-aligned labels on same line as 
controls
1. <form class="well">
2. <label>Label name</label>
3. <input type="text" class="span3" placeholder="Type something…">
4. <span class="help-block">Example block-level help text here.</span>
5. <label class="checkbox">
6.   <input type="checkbox"> Check me out
7. </label>
8. <button type="submit" class="btn">Submit</button>
9. </form>
Inline form
Add .form-inline to finesse the vertical alignment and spacing of form controls.
1.<form class="well form-inline">
2. <input type="text" class="input-small" placeholder="Email">
3. <input type="password" class="input-small" placeholder="Password">
4. <label class="checkbox">
5.   <input type="checkbox"> Remember me
6. </label>
7. <button type="submit" class="btn">Sign in</button>
8.</form>
Example markup
Given the above example form layout, here's the markup associated with the first input and control group. 
The .control-group,.control-label, and .controls classes are all required for styling.
Checkboxes and radios
Up to v1.4, Bootstrap required extra markup around checkboxes and radios to stack them. Now, it's a 
simple matter of repeating the <label class="checkbox"> that wraps the<input type="checkbox">.
Inline checkboxes and radios are also supported. Just add.inline to any .checkbox or .radio and you're 
done.
Inline forms and append/prepend
To use prepend or append inputs in an inline form, be sure to place the .add-on and input on the same 
line, without spaces.Form help text
To add help text for your form inputs, include inline help text with <span class="help-inline"> or a help 
text block with<p class="help-block"> after the input element
Buttons
Button class="" Description
Default btn Standard gray button with gradient
Primary btn btn-primary Provides extra visual weight and identifies the primary action in a set 
of buttons
Info btn btn-info Used as an alternative to the default styles
Success btn btn-success Indicates a successful or positive action
Warning btn btn-warning Indicates caution should be taken with this action
Danger btn btn-danger Indicates a dangerous or potentially negative action
Inverse btn btn-inverse Alternate dark gray button, not tied to a semantic action or use
Multiple button sizes 
Fancy larger or smaller buttons? Add .btn-large, .btn-small, or .btn-mini for two additional sizes.
Disabled state
For disabled buttons, add the .disabled class to links and the disabled attribute for <button> elements.
Icons Graciously provided by Glyphicons
How to use
Bootstrap uses an <i> tag for all icons, but they have no case class—only a shared prefix. To use, place 
the following code just about anywhere:
1.<i class="icon-search"></i>
There are also styles available for inverted (white) icons, made ready with one extra class:1.<i class="icon-search icon-white"></i>
Button groups
Use button groups to join multiple buttons together as one composite component. Build them with a 
series of <a> or<button> elements.
Dropdowns in button groups
Heads up! Buttons with dropdowns must be individually wrapped in their own .btn-group within a .btntoolbar for proper rendering.
1. <div class="btn-toolbar">
2. <div class="btn-group">
3.   ...
4. </div>
5. </div>
1. <div class="btn-group">
2. <button class="btn">1</button>
3. <button class="btn">2</button>
4. <button class="btn">3</button>
5. </div>
Button dropdowns
Similar to a button group, our markup uses regular button markup, but with a handful of additions to refine 
the style and support Bootstrap's dropdown jQuery plugin.
1.<div class="btn-group">
2. <a class="btn dropdown-toggle" data-toggle="dropdown" href="#">
3.   Action
4.   <span class="caret"></span>
5. </a>
6. <ul class="dropdown-menu">
7.   <!-- dropdown menu links -->
8. </ul>
9.</div>
Works with all button sizes
Button dropdowns work at any size. your button sizes to .btn-large, .btn-small, or 
.btn-mini.Nav, tabs, and pills Highly customizable list-style navigation
Basic tabs
Take a regular <ul> of links and add .nav-tabs:
Basic pills
Take that same HTML, but use .nav-pills instead:
Stackable Make tabs or pills vertical
How to stack 'em
As tabs and pills are horizontal by default, just add a second class, .nav-stacked, to make them 
appear vertically stacked.
1.<ul class="nav nav-tabs nav-stacked">
2. ...
3. </ul>
1. <ul class="nav nav-pills nav-stacked">
2. ...
3. </ul>
1. <ul class="nav nav-list">
2. ...
3. <li>
4.   <a href="#">
5.     <i class="icon-book"></i>
6.     Library
7.   </a>
8. </li>
9. ...
10. </ul>
Tabbable nav Bring tabs to life via javascript
To make tabs tabbable, create a .tab-pane with unique ID for every tab and wrap them in .tab-content.Fade in tabs
To make tabs fade in, add .fade to each .tab-pane.
For right or left aligned tabs, wrap the .nav-tabs and .tab-content in .tabbable.
Tabs on the bottom
1. <div class="tabbable tabs-below">
2. <div class="tab-content">
3.   ...
4. </div>
5. <ul class="nav nav-tabs">
6.   ...
7. </ul>
8. </div>
Tabs on the left
1. <div class="tabbable tabs-left">
2. <ul class="nav nav-tabs">
3.   ...
4. </ul>
5. <div class="tab-content">
6.   ...
7. </div>
8. </div>
Tabs on the right
1.<div class="tabbable tabs-right">
2. <ul class="nav nav-tabs">
3.   ...
4. </ul>
5. <div class="tab-content">
6.   ...
7. </div>
8.</div>
Navbar
Navbar scaffolding
The navbar requires only a few divs to structure it well for static or fixed display.
1.<div class="navbar">
2. <div class="navbar-inner">3.   <div class="container">
4.     ...
5.   </div>
6. </div>
7.</div>
Nav links
Nav items are simple to add via unordered lists.
1. <ul class="nav">
2. ...
3. <li class="divider-vertical"></li>
4. ...
5. </ul>
Fixed navbar
Fix the navbar to the top or bottom of the viewport with an additional class on the outermost div, .navbar.
1. <div class="navbar navbar-fixed-top">
2. ...
3. </div>
1. <div class="navbar navbar-fixed-bottom">
2. ...
3. </div>
You can easily add dividers to your nav links with an empty list item and a simple class. Just add this 
between links:
1. ul class="nav">
2. ...
3. <li class="divider-vertical"></li>
4. ...
5. </ul>
Component alignment
To align a nav, search form, or text, use the .pull-left or.pull-right utility classes. Both 
classes will add a CSS float in the specified direction.
Brand nameA simple link to show your brand or project name only requires an anchor tag.
1. <a class="brand" href="#">
2. Project name
3. </a>
Forms in navbar
To properly style and position a form within the navbar, add the appropriate classes as shown below. For 
a default form, include.navbar-form and either .pull-left or .pull-right to properly align it.
1.<form class="navbar-form pull-left">
2. <input type="text" class="span2">
3.</form>
.navbar-search to the form and .search-query
For a more customized search form, add .navbar-search to the form and 
.search-query to the input for specialized styles in the navbar.
1.<form class="navbar-search pull-left">
2. <input type="text" class="search-query" placeholder="Search">
3.</form>
Breadcrumbs
Why use them
Breadcrumb navigation is used as a way to show users where they are within an app or a site, but not for 
primary navigation. Keep their use sparse and succinct to be most effective
Markup
HTML is your standard unordered list with links.
1.<ul class="breadcrumb">
2. <li>
3.   <a href="#">Home</a> <span class="divider">/</span>
4. </li>
5. <li>
6.   <a href="#">Library</a> <span class="divider">/</span>
7. </li>
8. <li class="active">Data</li>
9.</ul>
Multicon-page paginationWhen to use
Ultra simplistic and minimally styled pagination inspired by Rdio, great for apps and search results. The 
large block is hard to miss, easily scalable, and provides large click areas.
Stateful page links
Links are customizable and work in a number of circumstances with the right class. .disabled for 
unclickable links and.active for current page.
Flexible alignment
Add either of two optional classes to change the alignment of pagination links: .paginationcentered and .pagination-right.
Pager For quick previous and next links
About pager
The pager component is a set of links for simple pagination implementations with light markup and even 
lighter styles. It's great for simple sites like blogs or magazines.
Optional disabled state
Pager links also use the general .disabled class from the pagination.
Default example
By default, the pager centers links.
● Previous
● Next
1.<ul class="pager">
2. <li>
3.   <a href="#">Previous</a>
4. </li>
5. <li>
6.   <a href="#">Next</a>
7. </li>
8.</ul>
Aligned links
Alternatively, you can align each link to the sides:
● ← Older
● Newer →
1.<ul class="pager">
2. <li class="previous">
3.   <a href="#">&larr; Older</a>
4. </li>
5. <li class="next">
6.   <a href="#">Newer &rarr;</a>
7. </li>8.</ul>
Inline labels Label and annotate text
Labels Markup
Default <span class="label">Default</span>
Success <span class="label label-success">Success</span>
Warning <span class="label label-warning">Warning</span>
Important <span class="label label-important">Important</span>
Info <span class="label label-info">Info</span>
Inverse <span class="label label-inverse">Inverse</span>
Badges Indicators and unread counts
About
Badges are small, simple components for displaying an indicator or count of some sort. They're 
commonly found in email clients like Mail.app or on mobile apps for push notifications.
Available classes
Name Example Markup
Default 1 <span class="badge">1</span>
Success 2 <span class="badge badge-success">2</span>
Warning 4 <span class="badge badge-warning">4</span>
Important 6 <span class="badge badge-important">6</span>
Info 8 <span class="badge badge-info">8</span>Inverse 10 <span class="badge badge-inverse">10</span>
Hero unit
1. <div class="hero-unit">
2. <h1>Heading</h1>
3. <p>Tagline</p>
4. <p>
5.   <a class="btn btn-primary btn-large">
6.     Learn more
7.   </a>
8. </p>
9. </div>
Alerts:
.alert
alert-message
alert-block
alert-heading
alert alert-error
alert alert-success
alert alert-info
Progress bars For loading, redirecting, or action status
progress
1. <div class="progress">
2. <div class="bar"
3.      style="width: 60%;"></div>
4. </div>
progress
progress progress-striped
progress progress-striped active
active progress-stripedWells
Use the well as a simple effect on an element to give it an inset effect.
class="well
Close icon
Use the generic close icon for dismissing content like modals and alerts.
<button class="close">&times;</button>
Using bootstrap-modal
1. <div class="modal hide" id="myModal">
2. <div class="modal-header">
3.   <button type="button" class="close" data-dismiss="modal">×</button>
4.   <h3>Modal header</h3>
5. </div>
6. <div class="modal-body">
7.   <p>One fine body…</p>
8. </div>
9. <div class="modal-footer">
10.   <a href="#" class="btn" data-dismiss="modal">Close</a>
11.   <a href="#" class="btn btn-primary">Save changes</a>
12. </div>
13. </div>
Dropdowns bootstrap-dropdown.js
1. <ul class="nav nav-pills">
2. <li class="active"><a href="#">Regular link</a></li>
3. <li class="dropdown" id="menu1">
4.   <a class="dropdown-toggle" data-toggle="dropdown" href="#menu1">
5.     Dropdown
6.     <b class="caret"></b>
7.   </a>
8. <ul class="dropdown-menu">
9.     <li><a href="#">Action</a></li>
10.     <li><a href="#">Another action</a></li>11.     <li><a href="#">Something else here</a></li>
12.     <li class="divider"></li>
13.     <li><a href="#">Separated link</a></li>
14.   </ul>
15. </li>
16. ...
17. </ul>
Markup
Just add data-dismiss="alert" to your close button to automatically give an alert close 
functionality.