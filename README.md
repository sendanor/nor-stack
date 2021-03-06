[![view on npm](http://img.shields.io/npm/v/nor-stack.svg)](https://www.npmjs.org/package/nor-stack)
[![npm module downloads](http://img.shields.io/npm/dt/nor-stack.svg)](https://www.npmjs.org/package/nor-stack)
[![Dependency Status](https://david-dm.org/sendanor/nor-stack.svg)](https://david-dm.org/sendanor/nor-stack)
<!--- [![Build Status](https://travis-ci.org/sendanor/nor-stack.svg?branch=master)](https://travis-ci.org/sendanor/nor-stack) -->
<!--- [![Coverage Status](https://coveralls.io/repos/github/sendanor/nor-stack/badge.svg?branch=master)](https://coveralls.io/github/sendanor/nor-stack?branch=master) -->

nor-stack
=========

Meta package which contains the centralized documentation and possible help utilities for our Node.js software stack

Sendanor Cloud Platform
-----------------------

![Component Architecture](docs/Components.png "Components")

Using this package
------------------

Although this package is actually -- at the moment -- possible to install and require, ***we do not suggest using it that way***.

This package is published as centarilized [documentation wiki](https://github.com/sendanor/nor-stack/wiki) for all of the projects.

We might publish CLI tool or other help utilities in the future.

Ideal Web Action Flow Model
---------------------------

This is our vision of ideal structure for web actions.

![Flow Model](docs/IdealWebAppRequestFlow.png "Web Action Flow Model")

Each step is a processing point in the life cycle of a request. Initiated first 
at the browser (or client) and going all the way to the database server (if 
necessary).

Green boxes are code executed in compatible JavaScript/Browserify/Node.js 
environment. The proxy might not have support for it but might have 
configuration to skip some files (like static files) and pass them directly 
back to the browser.

Each step can register code to be executed in a future step (including in the 
browser!). If there is no code to be executed, the shortest route will be used 
-- which means deeper layers can be skipped and the latency of the request 
will be significantly reduced.

Commercial Support
------------------

You can buy commercial support from [Sendanor](http://sendanor.com/software).
