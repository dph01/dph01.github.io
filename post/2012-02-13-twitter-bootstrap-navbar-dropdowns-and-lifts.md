---
title:  Bootstrap Navbar Dropdowns and Lift's Menu Builder
date: '2012-02-13'
description:
categories: code
tags: [scala, lift]
layout: 
permalink: 'twitter-bootstrap-navbar-dropdowns-and-lifts'
---


<p>Here's announcing a little utility I wrote to convert Lift's Menu.builder output into a nav bar with drop downs styled with Twitter's Bootstrap libraries.</p>
<p>Using this utility it's easy to generate a nav bar from your SiteMap that looks like:
<a href="{{urls.media}}/tbnav.png"><img width="500" src="{{urls.media}}/tbnav.png"></a>
</p>
<p>In particular, the features I'm looking to recreate here are:</p>
<ul>
<li>The nav-bar sits at the top, with the user navigation options (e.g. Login, logout, etc) and held over to the right. Once the user is logged in the&nbsp;Logout, Change Password, etc options are on a drop-down menu whose root value is the name of the logged-in user.</li>
<li>The man nav options&nbsp;are held over the the left.</li>
<li>An arbitrary number of the main nav options may be menu drop-downs and are easily configured using SiteMap 'submenu's</li>
</ul>
<p>The utility is available to download <a href="https://github.com/dph01/lift-TBUtils">https://github.com/dph01/lift-TBUtils</a></p>
<p>An example project using the library is available for download here: <a href="https://github.com/dph01/lift-TBNavbarTemplate">https://github.com/dph01/lift-TBNavbarTemplate</a>.&nbsp;</p>
<p>You can see a running version of this application at <a href="http://www.damianhelme.com/tbnav">www.damianhelme.com/tbnav</a></p>
<p>To create this nav bar, the menus are defined in Boot.scala by:</p>
<p><script src="https://gist.github.com/1817391.js?file=gistfile1.scala"></script></p>
<p>The menus are split left and right by defining two LocGroups: 'main' are the menu items held over the left, &amp; 'user' are the menu items held to the right. Note that because we're using the Login and SignUp Locs that comes with ProtoUser, we set the LocGroup in our User object (User.scala):</p>

<script src="https://gist.github.com/1817453.js"> </script>

<p>The nav bar is created in the html by wrapping the Menu.builder snippet with a call to TBNav.menuToTBNav:</p>

<script src="https://gist.github.com/1817530.js"> </script>

<p>Further info on using the TBNav utility is on the github page&nbsp;<a href="https://github.com/dph01/lift-TBUtils">https://github.com/dph01/lift-TBUtils</a>.</p>
<p>Please leave comments/thoughts/suggestions/questions etc!</p>
  
