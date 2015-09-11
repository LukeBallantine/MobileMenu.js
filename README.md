# MobileMenu.js

The Mobile Menu plugin scans an existing multi-level navigation menu and dynamically builds a dropdown list which 
navigates the user to the selected page on the select elements change event. It is true that there are a few other 
plugins out there that do this already, however most of them don’t seem to handle a menu that is more than 1 level deep.

These are the steps to get it working:

1) Make sure your navigation menu is in the format:

```html
<ul>
	<li><a href="/">Home</a></li>
	<li><a href="/services/">Services</a>
	<ul>
		<li><a href="/services/web-development/">Web Development</a></li>
		<li><a href="/services/online-marketing/">Online Marketing</a></li>
	</ul>
	</li>
	<li><a href="/contact-us/">Contact Us</a></li>
</ul>
```

2) Add the following scripts to your website:

```html
<script src="/js/jquery-1.6.js"></script>
<script src="/js/jquery-mobilemenu.js"></script>
```

3) Invoke the mobileMenu function on the empty dropdown list you wish to have populated:

```html
<script>
jQuery(document).ready(function($) {
  $("ddlMobileNav").mobileMenu({ ulsource : "#main-nav > ul", maxlevel : 4 });
});
</script>
```
The parameters you can specify for the mobileMenu function are:
ulsource
--------
The jquery selector referencing your unordered list.

maxlevel
--------
The maximum number of levels of the main navigation you wish to traverse.


