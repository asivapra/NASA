<img src="https://worldwind.arc.nasa.gov/img/nasa-logo.svg" height="100"/>
<img src="http://nci.org.au/wp-content/uploads/2018/09/NCI-Australia-and-Text-website-2-2.png" style="width:300px"/>
<p>in partnership with the <a href="http://www.esa.int" target="_blank">European Space Agency</a></p>

# Web WorldWind - NCI version

[![Build Status](https://travis-ci.org/NASAWorldWind/WebWorldWind.svg?branch=develop)](https://github.com/asivapra/WebWorldWind/tree/develop)

## Introduction

NASA Web World Wind is a JavaScript-based SDK that can be customised to publish the GSKY Web Map Service as a web app. 
We have added the GEOGLAM and DEA layers as published at the following URLs.

1. https://gsky.nci.org.au/ows/geoglam

2. https://gsky.nci.org.au/ows/dea

## User Guide

## Technical Details

To be able to view from the web, the pages must reside on a webserver that is publicly accessible. The DEV environment
at NCI is behind firewalls and cannot run a web server that is publicly accessible. For this demo, the pages are
therefore hosted on the WebGenie server (https://www.webgenie.com/NCI_WorldWind). It is only a temporary location.

### Files

The /examples directory has several \*.html and \*.js files that can be adapted for various map services. We have 
adapted the following files for making the demo pages.

`/examples/WMS.html` => `/examples/geoglam.html` and `/examples/dea.html`

`/examples/WMS.js` => `/examples/geoglam.js` and `/examples/dea.js`

### Code Change

The salient code changes from the original are listed below. Cosmetic an text-only changes are not listed.

1. HTML Files: `geoglam.html` and `dea.html`

```<script data-main="*geoglam*" src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.17/require.min.js"></script>```

	- The value, "geoglam", for 'data-main' denotes "geoglam.js", which is the only JavaScript file required to be altered.

## ---------------------------------------------------------------------------------------------------------------------
3D virtual globe API for JavaScript, developed by NASA in partnership with ESA. Provides a geographic context, complete with terrain, 
for visualizing geographic or geo-located information in 3D and 2D. Web WorldWind provides high-resolution terrain and 
imagery, retrieved from remote servers automatically as needed. Developers can provide custom terrain and imagery.
Provides a collection of shapes for displaying and interacting with geographic data and representing a range of 
geometric objects.   

- [worldwind.arc.nasa.gov](https://worldwind.arc.nasa.gov) has setup instructions, developers guides, API documentation and more
- [Forum](https://forum.worldwindcentral.com) provides help from the WorldWind community
- [WebStorm](https://www.jetbrains.com/webstorm) is used by the NASA WorldWind development team

## Get Started

The Web WorldWind [Developer's Guide](https://worldwind.arc.nasa.gov/web) has a complete description of Web 
WorldWind's functionality. You'll also find there links to many Web WorldWind resources, including a user guide. The 
latest Web WorldWind release provides many simple examples showing how to use all of Web WorldWind's functionality.

## Building

[Install NodeJS](https://nodejs.org). The build is known to work with v6.9.2 (LTS).

- `npm install` downloads WorldWind's dependencies

- `npm run build` builds everything

- `npm run doc` generates the WorldWind API documentation

- `npm run test` runs WorldWind's unit tests

- `npm run test:watch` automatically runs WorldWind's unit tests when source code changes

## License

Licensed under the [Apache License, Version 2.0](https://apache.org/licenses/LICENSE-2.0).
