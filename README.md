# MainPortfolioJS
Website used as a portfolio written in HTML, CSS and JavaScript

# Resources

Favicon

  - [Favicon Generator](https://favicon.io/favicon-generator/)
  - [Transparent Background](https://www.remove.bg/upload)
  - [Convert PNG to ICO](https://convertio.co/)

CDN
  - [CDN Libraries](https://cdnjs.com/libraries)
  - [SRI Hash](https://www.srihash.org/)

# Revision

Revisions made against **v0.7-beta.3** 

## SRI Hashes

All external imports for CSS (href) and JavaScript (src) are now validated using SRI hash. SRI is enforced using  crossorigin="anonymous" for all tags which contain external imports

## Isotope Integrity

Isotope CDN does not contain SRI hash. The SRI hash was generaed manually and the following import will occur instead:

	<script src="https://unpkg.com/isotope-layout@3.0.5/dist/isotope.pkgd.min.js" integrity="sha384-zEijsZ7v5U+8gaGEA+n4fHy97lqImaIXOAm9CB7vt+JHPXHkAhX9UzBxXW8BxiXF" crossorigin="anonymous"></script>
  
