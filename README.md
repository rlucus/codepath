# codepath
Codepath Security Course Assignments

# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Content Injection Vulnerability in WordPress
  - [ ] Summary: A flaw in the Wordpress REST API allows anyone to modify the contents of a post or page.
  https://blog.sucuri.net/2017/02/content-injection-vulnerability-wordpress-rest-api.html
    - Vulnerability types: Gives the attacked complete access to Page/Post content. Can be used to execute persistent secondary XSS and CSRF attacks.
    - Tested in version: 4.7
    - Fixed in version: 4.7.2
  - [ ] GIF Walkthrough: (<img src="https://github.com/rlucus/codepath/raw/master/inject/inject.gif">)
  - [ ] Steps to recreate: The site must be using permalinks and 4.7 or 4.7.1. Run the python script with the URL, post ID, and new post content.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. Persistent Cross-Site Scripting CVE-2015-3440
  - [ ] Summary: 
  https://www.exploit-db.com/exploits/36844/
    - Vulnerability types: Persisstent XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: <img src="https://github.com/rlucus/codepath/raw/master/comment_xss/comment_xss.gif">
  - [ ] Steps to recreate: Post a comment with a XSS payload. The script must be filled with atleast 64kb of data in order to bypass the filter.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. User Enumeration CVE-2017-5487
  - [ ] Summary: 
    - Vulnerability types: User Enumeration
    - Tested in version: 4.6
    - Fixed in version: 4.7.1
  - [ ] GIF Walkthrough: (<img src="https://github.com/rlucus/codepath/raw/master/user_enum.gif">)
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)


## Assets

All scripts and files available in git repo.

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- [Exploit Database] (https://www.exploit-db.com/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Ryan Lucus]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
