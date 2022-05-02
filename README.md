# MainPortfolioJS
Website used as a portfolio written in HTML, CSS and JavaScript

# Webserver revision

During production configuration consider setting up the web server to support HTTP/2

	curl -I <domain-name>
	
	
[HTTP or HTTP/2](https://stackoverflow.com/questions/36940691/how-do-i-know-if-my-website-is-being-served-over-http-or-http-2)

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


