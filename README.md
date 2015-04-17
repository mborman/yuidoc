YUIDoc-asp
======

YUI's JavaScript Documentation engine.

[![npm Version](https://img.shields.io/npm/v/yuidocjs.svg?style=flat-square)](https://www.npmjs.org/package/yuidocjs)
[![Build Status](http://img.shields.io/travis/yui/yuidoc.svg?style=flat-square)](https://travis-ci.org/yui/yuidoc)
[![Dependency Status](https://img.shields.io/david/yui/yuidoc.svg?style=flat-square)](https://david-dm.org/yui/yuidoc)

[![Build Status](https://travis-ci.org/mborman/yuidoc-asp.png)](https://travis-ci.org/mborman/yuidoc-asp)

[![npm Version](https://img.shields.io/npm/v/yuidoc-asp.svg?style=flat-square)](https://www.npmjs.org/package/yuidoc-asp)
[![Build Status](http://img.shields.io/travis/mbormani/yuidoc-asp.svg?style=flat-square)](https://travis-ci.org/yui/yuidoc-asp)
[![Dependency Status](https://img.shields.io/david/mborman/yuidoc-asp.svg?style=flat-square)](https://david-dm.org/yui/yuidoc-asp)

Overview
--------

YUIDoc-asp is a fork of YUIDoc that has been tweaked so it can recognize the comment syntax 
required in VBScript. This fork is an exact copy of YUIDoc except it will recognize the
following comment pattern:

    ''/**
    '' * This is an example function
    '' * @method testForAwesome
    '' * @param testValue {string} a value to test
    '' * @return `true` when awesome is in abundance
    '' */
    Function testForAwesome(testValue)
      ' detect awesome
    End Function

**Note:** The above function _rarely_ returns true... remember, we are talking about ASP here.
But as long as myself and others are burdened with maintaining legacy ASP code we might as well
have decent documentation that blends perfectly with our other documentation.

**Format explained:**  
VBScript does not have a block comment. It only supports line comments using an apostrophe 
as the comment marker. To make it work, the standard YUI doc comment is placed within a VBScript
comment. Additionally the VBScript comment character (the apostrophe) causes issues with
the code syntax highlighter (visible is you view the source from the documentation). Using
two apostrophes at the start of each line "corrects" the code highlight. The code higlighter
thinks the apostrophes open and close a string literal. If you only use one apostrophe the
highlighting will toggle between string highlight and code highlight as it encounters each
single apostrophe meant as a comment marker.

YUIDoc itself is a [Node.js](http://nodejs.org/) application used at build time to
generate API documentation for JavaScript code. YUIDoc is comment-driven and supports a wide
range of JavaScript coding styles. The output of YUIDoc is API documentation formatted as a
set of HTML pages including information about methods, properties, custom events and
inheritance for JavaScript objects.

YUIDoc was originally written for the YUI Project; it uses YUI JavaScript and CSS in the
generated files and it supports common YUI conventions like Custom Events. That said,
it can be used easily and productively on non-YUI code.

Installation
------------

    npm install -g yuidoc-asp

Documentation
-------------

* [User Guides](http://yui.github.io/yuidoc/)
* [Change Logs](https://github.com/yui/yuidoc/releases)
* [API Docs](http://yui.github.io/yuidoc/api/)
* [Mailing List](https://groups.google.com/forum/#!forum/yuidoc)

Contributing
------------

This project is not intended to be very actively devloped. 

License
-------

This software is free to use under the Yahoo Inc. BSD license. See the [LICENSE file](LICENSE) for license text and copyright information.
