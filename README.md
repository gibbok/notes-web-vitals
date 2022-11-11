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

Used when:
- Access performance at page level
- Can be used by non developers who do not use Lighthouse

Do not use:
- If you are already using Lighthouse

### Lighthouse 

Lighthouse is an open-source (Lab tool), automated tool for improving the quality of web pages. 
It can run on developer machine in Chome devoper tools or it is possible to automate running Lighthouse for every commit, viewing the changes, and preventing regressions
https://github.com/GoogleChrome/lighthouse-ci

Lighthouse can synthetically measure the Core Web Vitals metrics, Lab data which is collected from a controlled environment, rather than actual users. Unlike RUM data, lab data can be collected from pre-production environments and therefore incorporated into developer workflows and continuous integration processes. Examples of tools that collect synthetic data are Lighthouse and WebPageTest.

https://developer.mozilla.org/en-US/docs/Web/Performance/Rum-vs-Synthetic


Lighthouse user flows.
It is a tools which also allow developers to script interaction flows for performance testing beyond page startup.
https://web.dev/lighthouse-user-flows/

Lighthouse-CI
https://github.com/GoogleChrome/lighthouse-ci
Tool that runs Lighthouse during project builds and deploys to assist with performance regression testing. It presents a Lighthouse report along with pull requests, and tracks performance metrics over time.

Used when:
- finding performance improvement opportunities during development in both local and staging environments.
- where performance regression testing is needed to preserve good user experiences.

Do not use when:
- Not developers are involved
- is not a substitute for field data

### Performance APIs
There are many monitoring services. If you do want to roll your own monitoring system, take a look at the performance APIs, mainly PerformanceNavigationTiming and PerformanceResourceTiming, but also PerformanceMark, PerformanceMeasure, and PerformancePaintTiming.

### Web Vitals Extension

https://github.com/GoogleChrome/web-vitals-extension

A Chrome extension to measure metrics can be used by anyone in any role to assess a page's Core Web Vitals at all points of the page lifecycle.

Basic tools should be supplemented with Lighthouse.

### The performance tab in Chrome's DevTools 

The performance tab is a lab tool that profiles all page activity during startup or a recorded time period. It offers deep insight into everything it observes across dimensions such as network, rendering, painting and scripting activity, as well as a page's Core Web Vitals.

Use it:
- During development
- Provide only lab data

### CrUX

The Chrome User Experience Report (also known as the Chrome UX Report, or CrUX for short) is a dataset that reflects how real-world Chrome users experience popular destinations on the web.

CrUX data is collected from real browsers around the world, based on certain browser options which determine user eligibility ( a segment of real Google Chrome users from millions of websites.). A set of dimensions and metrics are collected which allow site owners to determine how users experience their sites.

The data collected by CrUX is available publicly through a number of tools and is used by Google Search to inform the page experience ranking factor.

Use when:

- you gather your own field data
- Though CrUX represents a subset of Chrome users, it's helpful to compare your website's field data to see how it aligns with its CrUX data

Do not use:

- Small websites
- Not ideal tool to be used during development

### Site Speed reports

The Site Speed reports show how quickly users are able to see and interact with content, it is accesible using Google Analytics.

https://support.google.com/analytics/answer/1205784?hl=en#zippy=

### Google Search Console Tools

Formerly Google Webmasters, provide online tool to measure metrics such search traffic and performance inclucing Vitals.
https://search.google.com/search-console/about

Use for:
- Developer and no developers
- Access group of similar pages
- Based on CrUX

### Google Analytics

For collecting own field data, there may be an opportunity for you to use the web-vitals library to send Web Vitals collected in the field to Google Analytics and use the web-vitals-report tool. The primary advantage of using web-vitals-report is that it simplifies analysis and visualization of field data by using an existing and widely-used analytics product.

### Key Terms

#### Lab data

Describes how hypothetical users may experience your website.

#### Real User Monitoring (RUM)

Field data describes how real users actually experienced your website.

Notes: The best dataset for assessing website performance in the field is the one you build, this depends on the size of your organization, and whether you want to pay for a third-party solution or create your own. Paid solutions will almost certainly measure Core Web Vitals (and other performance metrics). In large organizations with significant resources, this may be the preferred method. Google's web-vitals library will help you gather all Web Vitals. However, you'll be responsible for how that data is reported, stored, and analyzed.

## Docs:

https://web.dev/vitals-tools/

https://web.dev/vitals-measurement-getting-started/

https://github.com/GoogleChromeLabs/web-vitals-report

https://github.com/GoogleChrome/web-vitals-extension
