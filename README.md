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

Lighthouse can synthetically measure the Core Web Vitals metrics, Lab data which is collected from a controlled environment, rather than actual users. Unlike RUM data, lab data can be collected from pre-production environments and therefore incorporated into developer workflows and continuous integration processes. Examples of tools that collect synthetic data are Lighthouse and WebPageTest.

https://developer.mozilla.org/en-US/docs/Web/Performance/Rum-vs-Synthetic

### Performance APIs
There are many monitoring services. If you do want to roll your own monitoring system, take a look at the performance APIs, mainly PerformanceNavigationTiming and PerformanceResourceTiming, but also PerformanceMark, PerformanceMeasure, and PerformancePaintTiming.

### Web Vitals Extension
https://github.com/GoogleChrome/web-vitals-extension

A Chrome extension to measure metrics.

### CrUX

The Chrome User Experience Report (also known as the Chrome UX Report, or CrUX for short) is a dataset that reflects how real-world Chrome users experience popular destinations on the web.

CrUX data is collected from real browsers around the world, based on certain browser options which determine user eligibility. A set of dimensions and metrics are collected which allow site owners to determine how users experience their sites.

The data collected by CrUX is available publicly through a number of tools and is used by Google Search to inform the page experience ranking factor.

## Docs:

https://web.dev/vitals-tools/
https://web.dev/vitals-measurement-getting-started/
https://github.com/GoogleChromeLabs/web-vitals-report
https://github.com/GoogleChrome/web-vitals-extension
