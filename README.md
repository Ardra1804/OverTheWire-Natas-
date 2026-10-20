# OverTheWire-Natas-
About the Project

This repository documents my journey through the OverTheWire Natas wargame, where I explored basic web application security concepts by solving practical challenges.

Instead of relying only on theoretical explanations, I investigated web pages, inspected their source code, used browser developer tools, and explored publicly accessible server files to understand how information can be exposed through improper security practices.

This project is part of my learning journey for cybersecurity and the COEP CyberCell induction process.

Platform: OverTheWire Natas
Focus: Web Security, Information Disclosure, HTML Source Inspection, Browser Developer Tools, and Web Server Configuration

Objectives

Understand how web applications can unintentionally expose sensitive information.

Learn to inspect HTML source code and browser developer tools.

Understand the difference between hiding an interface feature and securing the underlying resource.

Explore how publicly accessible files can reveal information about a website.

Learn the security implications of source-code comments, directory listings, and crawler directives.

Develop a systematic approach to solving web-security challenges.

Tools and Technologies

OverTheWire Natas

Web browser

Browser Developer Tools

HTML source inspection

robots.txt

Browser-based file and resource inspection

Challenges and Learning

1. Inspecting Web Page Source Code

Objective: Investigate the web page to locate information needed to proceed to the next level.

Approach:

I inspected the source code of the initial Natas page using the browser's developer tools. While examining the HTML, I found information that was not displayed directly in the normal page interface.

Concept learned:

HTML source code can contain comments, embedded data, or other information that is not visible when a user simply views the rendered page.

Security lesson:

Sensitive information such as passwords, API keys, and internal configuration details should never be embedded in publicly delivered HTML or JavaScript.

2. Investigating a Page with Restricted Right-Click

Objective: Continue inspecting a web page even though the usual right-click interaction was disabled.

Approach:

The page restricted right-clicking, which prevented me from using the normal context-menu workflow. I used the browser's developer tools to inspect the page and investigate the information available to the browser.

Concept learned:

Disabling right-click is only a user-interface restriction. It does not prevent users from inspecting the HTML and resources that their browser receives.

Security lesson:

Client-side restrictions should not be treated as security controls. Sensitive data must be protected by server-side access controls rather than by disabling browser interactions.

3. Finding Information in a Publicly Accessible File

Objective: Investigate the files and resources associated with a web page to locate information required by the challenge.

Approach:

I discovered a users.txt file within the files directory associated with the page and examined its contents. The file contained information that helped me progress to the next level.

Concept learned:

Files that are publicly accessible through a web server can expose information to anyone who knows or discovers their location.

Security lesson:

Files containing credentials or other sensitive information should not be stored in publicly accessible directories. Servers should enforce appropriate authentication and authorization.

4. Discovering a Resource Through robots.txt

Objective: Investigate website crawler directives to identify additional resources.

Approach:

I navigated to the website's robots.txt file and inspected its contents. The directives provided clues about paths that were not intended to be crawled by search engines. I followed the relevant clue and discovered a publicly accessible file containing information needed for the challenge.

Concept learned:

The robots.txt file communicates crawler preferences. Its Disallow directives request that compliant crawlers avoid specified paths, but they do not prevent direct access to those paths.

Security lesson:

robots.txt must not be used to protect confidential resources. Sensitive files and endpoints require proper access control.

Key Security Concepts

Information Disclosure

Information disclosure occurs when a system reveals data that should not be available to unauthorized users. Examples include exposed credentials, sensitive source-code comments, and publicly accessible configuration files.

Client-Side Versus Server-Side Security

Client-side restrictions, such as disabling right-click, control browser interactions but do not provide reliable protection for information already delivered to the browser.

Server-side authentication and authorization are necessary to control access to sensitive resources.

Source Code Inspection

Inspecting HTML and browser-loaded resources helps developers and security testers understand how a web application works and identify information that should not be exposed.

Web Server File Exposure

Files placed inside publicly accessible web directories may be retrieved directly through a browser. Sensitive files should be stored outside public web roots or protected using suitable server-side controls.

Crawler Directives

The robots.txt file is useful for communicating crawling preferences. It is not an access-control mechanism, and its contents may reveal paths that deserve further security review.

What I Learned

How to inspect HTML source code using browser developer tools.

Why disabling right-click does not prevent source inspection.

How publicly accessible files can expose sensitive information.

How robots.txt works and why it should not be used to protect confidential resources.

How to investigate clues methodically rather than relying only on the visible webpage.

Why sensitive information must be protected through server-side security controls.

References

OverTheWire Natas

MDN Web Docs — HTML

MDN Web Docs — Browser Developer Tools

Google Search Central — robots.txt Introduction

AI Assistance

ChatGPT was used to help organize the write-up and clarify web-security concepts. The challenge-solving experiences described here are based on my own work. I reviewed the explanations and am responsible for understanding the concepts documented in this repository.

Conclusion

The Natas wargame helped me understand that information visible or accessible through a web application can reveal weaknesses even when it is not displayed directly on the page.

These exercises introduced me to practical web-security investigation and highlighted the importance of protecting sensitive information through proper server-side security controls.
