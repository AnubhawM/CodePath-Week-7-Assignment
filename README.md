# CodePath-Week-7-Assignment
Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) WordPress 4.2 Cross Site Scripting
  - [X] Summary: When making a comment, if its size is greater than 64 kB, it will be truncated. This affects the HTML that will be generated on the page. Due to this, an XSS attack can be possible.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: <img src='https://github.com/AnubhawM/CodePath-Week-7-Assignment/blob/master/XSS1.gif' width='' alt='Video Walkthrough' />
  - [X] Steps to recreate: 
  
  Enter the following as a comment:
  < a title='x onmouseover=alert(unescape(/hello%20world/.source))
style=position:absolute;left:0;top:0;width:5000px;height:5000px
 AAAAAAAAAAAA...'></a>
 
 
 Note: The "AAA..." needs to be greater than 64 kB.
  - [ ] Affected source code:
    
2. (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: This exploit is all about placing a malicious script in a comments box to obtain cookie information.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: <img src='https://github.com/AnubhawM/CodePath-Week-7-Assignment/blob/master/XSS3.gif' width='' alt='Video Walkthrough' />
  - [X] Steps to recreate: Type <script>while(1){alert(document.cookie);}</script> in a comment.
  - [ ] Affected source code:
  
  
    
3. (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [X] Summary: The filename of an uploaded image is not not sanitized. Leveraging this, if the filename has a malicious script in it, it will execute when viewed.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [X] GIF Walkthrough: <img src='https://github.com/AnubhawM/CodePath-Week-7-Assignment/blob/master/XSS2.gif' width='' alt='Video Walkthrough' />
  - [X] Steps to recreate: Upload an image with a malicious script in the title of the file. When the page containing the image is loaded, the script within the title will execute. 
  - [ ] Affected source code:
  
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

No assets were used.

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

I had a LOT of trouble getting Vagrant to work. Kali simply would not work. So doing this assignment was extremely difficult not because of the actual challenges, but because I had so many issues setting up the pentesting environment. Once I could get my environment stable enough, doing the assignment tasks wasn't too difficult.
## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
