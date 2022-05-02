# MainPortfolioJS
Website used as a portfolio written in HTML, CSS and JavaScript

# Webserver revision

During production configuration consider setting up the web server to support HTTP/2

	curl -I <domain-name>
	
	
[HTTP or HTTP/2](https://stackoverflow.com/questions/36940691/how-do-i-know-if-my-website-is-being-served-over-http-or-http-2)

# CDN Import Versions
## CSS
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
	<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.8/css/all.css" integrity="sha384-3AB7yXWz4OeoZcPbieVW64vVXEwADiYyAEhwilzWsLw+9FgqpyjjStpPnpBO8o8S" crossorigin="anonymous">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/fancybox/3.2.5/jquery.fancybox.min.css" integrity="sha512-jrDXSF9AvYxucIemk/2r7ntYBCMYWlNwl9D+DeL+3CxpbWC+JEwU3FTGFFLKm62s1ybn9hO5BImk6z0vTV3jdA==" crossorigin="anonymous" referrerpolicy="no-referrer" />

## JavaScript
Placed in <head> tag:
	
	<script src="https://code.jquery.com/jquery-3.6.0.min.js" integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>

Placed at bottom of <body> tag:
	
	<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
	<script src="https://unpkg.com/isotope-layout@3.0.5/dist/isotope.pkgd.min.js" integrity="sha384-zEijsZ7v5U+8gaGEA+n4fHy97lqImaIXOAm9CB7vt+JHPXHkAhX9UzBxXW8BxiXF" crossorigin="anonymous"></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/fancybox/3.2.5/jquery.fancybox.min.js" integrity="sha512-GtU3C24wUoqw9549QI/9K3/JVLHIVqdwdDVkEkaX8umZS7TGEaBFUSBJe6tU6/VAc20z9BkYN3Yw2Jov7pUrqQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
	
## GitHub
  - [Superslides](https://github.com/nicinabox/superslides)
  - [Owl Carousel v2.3.3](https://owlcarousel2.github.io/OwlCarousel2/docs/started-welcome.html)

# Resources

Favicon

  - [Favicon Generator](https://favicon.io/favicon-generator/)
  - [Transparent Background](https://www.remove.bg/upload)
  - [Convert PNG to ICO](https://convertio.co/)

CDN
  - [CDN Libraries](https://cdnjs.com/libraries)
  - [SRI Hash](https://www.srihash.org/)

jQuery Vulnerabilities
  - [jQuery Vulnerabilities](https://snyk.io/vuln/npm:jquery)

# Revision

Revisions made against **v0.7-beta.3** 

## SRI Hashes

All external imports for CSS (href) and JavaScript (src) are now validated using SRI hash. SRI is enforced using  crossorigin="anonymous" for all tags which contain external imports

## Isotope Integrity

Isotope CDN does not contain SRI hash. The SRI hash was generaed manually and the following import will occur instead:

	<script src="https://unpkg.com/isotope-layout@3.0.5/dist/isotope.pkgd.min.js" integrity="sha384-zEijsZ7v5U+8gaGEA+n4fHy97lqImaIXOAm9CB7vt+JHPXHkAhX9UzBxXW8BxiXF" crossorigin="anonymous"></script>
  
## jQuery
### CDN Location
CDN Library moved from code.jquery.com to ajax.googleapis.com

### Version

Moved from jQuery 3.3.1 to jQuery 3.6.0.


