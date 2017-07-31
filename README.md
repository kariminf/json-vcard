# jsonVCard

[![Project](https://img.shields.io/badge/Project-json-VCard-FDEE00.svg)](https://kariminf.github.io/json-vcard/)
[![Version](https://img.shields.io/badge/Version-0.3.0-FDEE00.svg)](https://github.com/kariminf/json-vcard/releases)
[![License](https://img.shields.io/badge/License-Apache_2.0-FDEE00.svg)](http://www.apache.org/licenses/LICENSE-2.0)

When you want to create a VCard (CV website), you have to put your information into a static HTML file (if you don't want a server based one).
Then, if you want to change the design, sometimes changing CSS is not enough; you have to change HTML too.

So, this project meant to:
* Create a client side VCard
* Separate information and design.
* Create many themes

As consequences:
* The application can be hosted widely and doesn't need any special
* The page is built locally and dynamically in the user side
* The themes can be changed easily without


The goal of this project is:
* Generate dynamically a CV from a json file, without being forced to generate static webpages everytime you modify an information.
* Modify the style of your CV using a template and a stylesheet.

See a demo [here](https://kariminf.github.io/jsonVCard/)

## How it works

By introducing information inside a json file ("vcard.json"), you can generate a Vcard webpage (CV).
This can be done using javascript ("jsonvcard.js") which is called as follows:
```html
<html>
<head>
  <meta charset="UTF-8">
  <title>Test portfelio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <script type="text/javascript" src="jsonvcard.js" ></script>
</head>
<body>
</body>
</html>
```
The json file ("jsoncard.js") must be in the same folder as the script ("jsonvcard.js").
It contains information about the one for whom we want to generate a CV.
This is an enumeration of the different entries:
* theme: contains information about the theme used to present the page
  * name: the name of the theme
  * style: the style applied to this theme

* perso: personal information
  * name: the first name
  * family: the last name
  * photo: a link to profile photo
  * birthday: birthday in the format "yyyymmdd"
  * email: a list of email addresses
  * tel: a list of phone numbers
  * web: web-page link
  * address: the address of your home or office
  * title: Your current title
  * bio: a link to an HTML file containing a little biography

* social: social networks such as "facebook", "twitter", "linkedin"and "gplus"

* exp: a list of experiences, where each contains these information:
  * from : a date formated as "yyyymmdd"
  * to: a date formated as "yyyymmdd"
  * job: the job title
  * org: where did you work
  * resp: responsibilities which is a list of strings
  * desc: a link to a description of the job

* educ: a list of education experiences, where each one contains:
  * from : a date formated preferably as "yyyymmdd"
  * to: a date formated preferably as "yyyymmdd"
  * inst: the institution
  * desc: a link to a description of the studies

* pub: a list of publications, where each one contains:
  * title: publication title
  * publisher: the publisher
  * date: date of publication as "yyyymmdd"
  * url: a link to the publication
  * authors: a list of authors
  * desc: a link to a description of the publication

* skill: a list of skills
  * title: the name of the skill
  * mark: a number from 1 to 10 expressing how experienced you are

* lang: a list of natural languages, where each contains
  * name: the language's name
  * read: a number from 1 to 10 expressing your capacity of reading
  * write: a number from 1 to 10 expressing your capacity of writing
  * ustnd: a number from 1 to 10 expressing your capacity of understanding

For Javascript methods, check [this YuiDoc generated documentation](docs/index.html)
## Credits

* Me: for may hair became as white as snow programming this
* [Zlatko Najdenovski](https://www.iconfinder.com/zlaten): for the social media icons called  
[logotypes](https://www.iconfinder.com/iconsets/logotypes), licenced under [CC-BY-3.0](https://creativecommons.org/licenses/by/3.0/)
* https://commons.wikimedia.org/wiki/File:Phone_icon_rotated.svg

## License

Copyright (C) 2016-2017 Abdelkrime Aries

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
