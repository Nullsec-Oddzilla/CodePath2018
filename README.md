# CodePath2018
Files used for my training in the 2018 CodePath course.

# Project 7 - WordPress Pentesting

Time spent: 10 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: This XSS exploit uses a flaw in how WP truncates posts to evade filters and execute XSS script.
    - Vulnerability types: Stored XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: <img src="https://github.com/Nullsec-Oddzilla/CodePath2018/blob/master/XSSDemo_1.gif" width="800">
  - [ ] Steps to recreate: 
	1.)Create post (as normal user) with XSS script in the markup
	2.)Insert 64kb of text inside these tags. This will cause the system to truncate the code, which reveals the flaw.
	3.)Reload the page, or view recent page as admin. The XSS script will fire when loaded.
  - [ ] Affected source code:
    - [Link 1](https://wpvulndb.com/vulnerabilities/7945)
    - [Link 2](https://klikki.fi/adv/wordpress2.html)

## Assets

I created a txt file to save a large block of characters to copy and oaste for the exploit, as well as ensure the data was over 64kb. 

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

I originally encountered quite a bit of difficulty as I had an issue with Vagrant. Despite what version number I entered in the WPDistillery config file, Vagrant would install a more recent build. Vagrant would actually claim it was downloading WP 4.2, and then 4.2.19 would be installed. I eventually found a solution for this issue when I read a thread posted by a classmate who had the same issue in the CodePath message boards. However I did spend a large amount of time prior to this trying to troubleshoot the issue. Due to this and a limited timeframe, I am only submitting 1 exploit at the time with more to be added soon.

## License

    Copyright [2018] [Kevin Simmons] <-- Unsure of what to put here?

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
