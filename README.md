## Native iOS App using NYTimes Most Popular API

A simple iOS Native app developed in Swift to hit the The NY Times Most Popular Articles (Most Viewed) API and show a list of articles, that shows details when items on the list are tapped (a typical master/detail app).

## Demonstrations

Covers the following:
* Object Oriented Programming Approach 
* Unit Tests 
* UI Test 
* Generic and simple code 

App Features:
* Supports Split View (Landscape orientation)
* Auto layout with Dynamic Cell Resizing
* Supports API Pagination 
* Dynamic Time Period Configuration 
* Dynamic Section Configuration 

## Installation

Pods are made available as part of repository, to facilitate simplicity in checkout and execution. Simply checkout and run the project.

## Build

To build using xcodebuild without code signing
```
xcodebuild clean build -workspace "NYTimes_By_Abdu.xcworkspace" -scheme "NYTimes_MostPopularArticles" CODE_SIGN_IDENTITY="" CODE_SIGNING_REQUIRED=NO
```





### Disclaimer

Although code quality can be subjective at times, and the approaches may not entirely be the best, I'll be happy to answer any questions  #cmiosdeveloper related to existing implementations as well as acknowledged areas which can potentially be further improved.

## General Notes/FAQ's

* Why a protocol for Network Controller?
This keeps the Structure flexible and independent of the networking SDK used. I used Alamofire in this example, however the structure is flexible enough to accomodate any other framework or custom classes.

* Why base64encoded the api-key?
To keep the implementation simple, not recommended for production usages (Best to keep the api key on a server proxy, or use encryption if at all it has to be kept in the code), hard-coding the api-key in plain text inside the code should be avoided at any cost.

* Why some classes have static methods but are not Singletons?
None of the classes in the current scope are maintaining any stateful functionality at the moment. (Although a session like state can be maintained for current offset etc under a single class, but with a 2-page application, viewcontroller handling this is simplest) Unless a class needs to maintains a state, using singleton only for static methods should be avoided.


## License

Copyright 2019 Abdul Nasir B A

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Contact
* [Linkedin](https://www.linkedin.com/in/abdulnasar/)

