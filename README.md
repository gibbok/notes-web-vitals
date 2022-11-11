# Notes on Web Vitals


## Web Vitals

Web Vitals is an initiative by Google to provide unified guidance for quality signals that are essential to delivering a great user experience on the web.

## Core Web Vitals

Core Web Vitals are subset of Web Vitals that apply to all web pages, with the aim to measure:

- loading
- interactivity
- visual stability

## Important metrics

|     | Description              | Measures            | Good results        |
|-----|--------------------------|---------------------|---------------------|
| LCP | Largest Contentful Paint | Loading performance | <= 2.5 seconds      |
| FID | First Input Delay        | Interactivity       | <= 100 milliseconds |
| CLS | Cumulative Layout Shift  | Visual stability    | 0.1                 |  

Other useful metrics:

- Time to First Byte (TTFB)
- First Contentful Paint (FCP) 


## Tools

### Web-vitals API
Simple JS library to make API call and collect data:
https://github.com/GoogleChrome/web-vitals

We can access the data collected using using:
Search Console's Core Web Vitals report https://support.google.com/webmasters/answer/9205520

### PageSpeed Insights (PSI)

Online toll used to create reports on the user experience of a page on both mobile and desktop devices. The tool provides suggestions.
Needs to be hacked for site behind authentication.

### Lighthouse 

Lighthouse is an open-source, automated tool for improving the quality of web pages. 
It can run on developer machine in Chome devoper tools or it is possible to automate running Lighthouse for every commit, viewing the changes, and preventing regressions
https://github.com/GoogleChrome/lighthouse-ci


## Docs:

https://web.dev/vitals-tools/
https://web.dev/vitals-measurement-getting-started/
https://github.com/GoogleChromeLabs/web-vitals-report
https://github.com/GoogleChrome/web-vitals-extension
