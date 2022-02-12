# system-design-react-code-examples
A curation of code examples and in depth technical implementation approaches to solve the common frontend system design issues in React.

---
### Target Audience 
1) advanced beginner/intermediate developers wishing to get better technical understanding 
2) developers exploring how to do handle technical things in their own projects.
3) for my own reference as I need something like this for my own learning.

---
### Philosophy

The philosophy behind this endeavour is to document as much as possible a practical guide as possible someone looking to level-up fast/ implement things. 

> “Talk is cheap. Show me the code.”
> — Linus Torvalds

---

- [Engineering Design](#engineering-design)
- [High Level Design](#high-level-design)
- [Low level Design](#low-level-design)

---

### Architecture Deep dive

- [Rebuilding our tech stack for the new Facebook.com](https://engineering.fb.com/2020/05/08/web/facebook-redesign/)
- [Front-End Performance Optimization with Accelerated Compositing Part 1 ](https://www.alibabacloud.com/blog/front-end-performance-optimization-with-accelerated-compositing-part-1_594194)
- [Front-End Performance Optimization with Accelerated Compositing Part 2 ](https://www.alibabacloud.com/blog/front-end-performance-optimization-with-accelerated-compositing-part-2_594195)
- [SSR-based Optimization of Double 11 Virtual Venue – A More Complex Rendering Architecture](https://www.alibabacloud.com/blog/ssr-based-optimization-of-double-11-virtual-venue-a-more-complex-rendering-architecture_596970?spm=a2c65.11461447.0.0.5c88790bSaSVAr)
- [React Philosophies](https://github.com/mithi/react-philosophies)
- [idiomatic.js](https://github.com/rwaldron/idiomatic.js)
- [Client-Side Architecture Basics](https://khalilstemmler.com/articles/client-side-architecture/introduction/)
- [CSS Triggers](https://csstriggers.com/)
- [The Web Browser Internals](https://www.madhusagar.org/The-Web-Browser-Internals/)

---

### Engineering Design

- Team size
- User base
- Knowledge base
- Compliance/Governance
- User/Client expectations
- Open source vs proprietary
- Documentation / PRD
- Future Roadmaps

---

### High Level Design

- Platform identification
- SPA vs MPA
- SSR, SSG, CSR
- [Tech stack](https://10up.github.io/Engineering-Best-Practices/react/)
- Search Engine Optimization
- CI/CD
- User Experience
- [A/B testing](https://philipwalton.com/articles/performant-a-b-testing-with-cloudflare-workers/)
- MVP planning
- Server Side Architecture
- Security
- State Management
- Internationalization - [example](https://pgjones.dev/tozo/frontend/i18n/)
- E2E testing
- Tools Integration
- Authentication & Authorization
- Quality Assurance & Control
- User role management - [example](https://github.com/atulmy/crate/tree/master/code/web/src/modules/auth)

---

### Low Level Design

- Code/Folder architecture
    * [Example - #2 in this blogpost](https://javascript.plainenglish.io/7-steps-to-modernize-and-optimize-your-react-app-466cbea51b8f)
- Desktop/Mobile first approach
- System breakdown
   * [Atomic Design](https://bradfrost.com/blog/post/atomic-web-design/)  
- [Component Design](https://overreacted.io/writing-resilient-components/#writing-resilient-components)
- Form development
- Storage management
   * Using localForage (https://github.com/localForage/localForage)
   * redux-persist - [code](https://github.com/Th3Wall/react-crwn-cothing-ecom) 
- API Design
   * Example pattern- [code](https://github.com/oldboyxx/jira_clone/blob/master/client/src/shared/utils/api.js)
- Instrumentation
- Design system
- Routing management
- [CSS optimizations](https://developer.mozilla.org/en-US/docs/Learn/Performance/CSS) - [Code-splitting](https://lihautan.com/css-code-splitting/)
- [Lazy loading of modules](https://web.dev/fast/#lazy-load-images-and-video)
- [Accessibility](https://www.w3.org/WAI/tips/developing/)
- [Image optimizations](https://web.dev/fast/#optimize-your-images)
- [Pagination](https://dev.to/potouridisio/the-only-pagination-you-ll-ever-need-1-2-3-4-5-4il5), [Debouncing, Throttling](https://codeburst.io/throttling-and-debouncing-in-javascript-b01cad5c8edf)
- [Performance](https://developer.mozilla.org/en-US/docs/Web/Performance): FCP, LCP, TTI, CLS
- [Versioning](https://github.com/pirelenito/git-revision-webpack-plugin#plugin-api)
- Unit testing

---

### High Level Design details

<br>

**Product Requirement Document (PRD) / Design Document**
- Identify Scope/Requirement
- Review your understanding with stakeholders

<br>

**Discuss about Design/Wireframe**
- Think like an architect.
- We should not consider team bandwidth, capacity and time.
- Discuss about Edge cases.
- Robustness: Handle SPOF (Single Point of Failure) ex: Monitoring, Logging

<br>

**Identify Business**
- Is it B2B (business-to-business)?
- Is it B2C (business-to-consumer)?
- Is it Internal Product?
- Is it Customer facing product?

<br>

**Identify Platform**
- Desktop
- Mobile
- Tablet

<br>

**Identify Users (Know your audience)**
- Conduct surveys
- Discuss about Location and Devices
- Internet speed
- End Users knowledge base (ex: Technical user)
- Pilot Product (sometimes to understand audience)

<br>

**Identify Design Approach**
- Responsive vs Adaptive design
- Desktop first vs Mobile first

<br>

**Identify APIs**
- Rest APIs / Graph APIs / RPC
- JSON / Protocol buffers

<br>

**Role based management**
- Large system needs roles based access and permissions
- Authentication and Authorization
- Read/Write/View Permissions
- Discuss about Routes/Component access

<br>

**Identify Right Platform (compare frameworks based on the use case)**
- Single Page Applications (Unsuitable for Blogs/News based products)
    - No reloading of a page at navigation
    - No SEO
- Multi Page Applications
    - Reloading of a page at every page navigation.
- Progressive Web Applications
    - Provides offline support and native like functionality.
    - [Examples of PWA](https://github.com/hemanth/awesome-pwa)
- Server Side Rendering
    * [SSR](https://survivejs.com/webpack/output/server-side-rendering/)
    - Better SEO
- Important points to discuss:
    - Are users on mobile?
    - Is SEO needed?
    - Is SPA enough?
    - Is PWA enough? (Service worker, Web Worker)
    - Compare SSR / SSG / CSR
    - Any Pricing model? (optional) - Subscriptions based, Paid APIs 
    - Will my app be Frontend heavy? (or backend heavy)
    - Do I have resources for this skill?
    - Is your application Canvas (or SVG) heavy? (Figma, Draw.io) - [example](https://github.com/rrag/react-stockcharts-examples2)
    - Is your application webRTC heavy? (Video streaming) -[example](https://github.com/OpenVidu/openvidu-call-react)

<br>

**Identify User Flow**
- Discuss vision of a product.
- Do we need to build from scratch or we can leverage some existing functionalities
- Discuss about authentication and authorization (Google auth / OAuth)
- Interact with the Product manager to understand the scope before designing the application.
- Discuss happy scenarios.
- Discuss edge cases.
- Discuss failing scenarios

<br>

**Identify MVP (Minimum Viable Product)**
- Problem -> Solution -> Build MVP -> MVP to Customers
- Discuss MVP phase with product manager
- Discuss roadmaps and divide product in milestones
- After MVP release there can be a slight change in design/approach to make the product better

<br>

**Volume of Operations**
- Discuss about the end users of the product
   * Observe the data in something like Google Analytics for split by device/location/OS etc in production later.
- Identify QPS (Queries per second)
   * Monitor throughput of the web server/ web application server - [benchmark for reference](https://www.techempower.com/benchmarks/#section=data-r20&hw=ph&test=fortune)
- Discuss about Load testing/Stress testing
    * Use something like [Locust](https://locust.io/)/[boomer](https://github.com/myzhan/boomer)
- Inject analytics in application (ex: Google analytics, Sentry, NewRelic)
   * For cost-effectiveness instead of using ready-made solution, can define our events, using Kafka to stream the events to a backend server and use a Grafana dashboard if required.
- Analytics data helps us to scale the system

<br>

**[SEO (Search Engine Optimization)](https://github.com/marcobiedermann/search-engine-optimization)**
- Crawling
- Use of Heading tags
- Semantic tags - [HTML Reference](https://htmlreference.io/) - [Example](https://github.com/joelhooks/joelhooks-com/blob/main/src/components/SEO.js)
- Site Ranking
- Sitemap
- Meta Keywords - [Example](https://github.com/slaterbbx/borrellis.bakery/blob/7bf72923972f274a0dec69cb9fc59fbec1f3d576/src/components/seo.js#L13)
- Organic approach vs Inorganic approach
- Use of alt tags
- 301 Redirects (bad for SEO)
- Robots.txt - [Example](https://github.com/peterpeterparker/tietracker/blob/main/public/robots.txt)
- Open graph protocol (https://ogp.me/) for social graph - [Example](https://github.com/gabroun/malikgabroun/blob/master/src/components/Seo.js)

<br>

**Component Based Design**
- Component wise deployment cycle (CI/CD)
- Monolith vs Microservice architecture
   * Microservice example - [live](https://kachkaev.ru/) - [code](https://gitlab.com/kachkaev/website-frontend/)
- [Micro Frontend (independent dev & deployment for scalability)](https://blog.bitsrc.io/how-we-build-micro-front-ends-d3eeeac0acfc)
    * Topcoder Platform Microfront Earn App - [code](https://github.com/topcoder-platform/micro-frontends-earn-app/tree/responsive)
- Static components vs Dynamic components 
- IFrame/Shell approach 
   * [AppShell approach](https://github.com/GoogleChromeLabs/sw-precache/tree/master/app-shell-demo)
   * [IFrame approach](https://blog.bitsrc.io/best-practices-in-using-iframes-with-react-6193feaa1e08)

<br>

**State Management**
- How to maintain state through the application?
- How to manage users' data?
- State management Libraries (Redux, Flux, NgRX)
-   * Redux Architecture
       * [Scalable Redux architecture for React Projects with Redux-Saga and Typescript](https://itnext.io/scalable-redux-architecture-for-react-projects-with-redux-saga-and-typescript-f6afe1dece9b)
       * [10 Tips for Better Redux Architecture](https://medium.com/javascript-scene/10-tips-for-better-redux-architecture-69250425af44)
       * [React/Redux: pitfalls and best practices](https://tech.bedrockstreaming.com/react-redux-pitfalls-and-best-pratices/)
    * Redux-saga
        * Example Codebase -[react-crwn-cothing-ecom](https://github.com/Th3Wall/react-crwn-cothing-ecom)
    * RxJS
        * [Example recipes](https://www.learnrxjs.io/learn-rxjs/recipes)
        * [Basic example using redux-observable](https://github.com/simonhorlick/react-redux-observable-example)
        * [Better example](https://github.com/mitsuruog/react-redux-observable-typescript-sample)
    * Redux Thunk

<br>

**Handling APIs**
- Polling (Short and Long)
- Web Sockets (Real-time) (ex: chat, shared editors)
    * Displaying live orderbook using websocket - [code](https://github.com/fibo/order-book)
- Batch requests
- GraphQL
- Caching GET APIs (Middleware concepts to cache response) - [guide](https://roadmap.sh/guides/http-caching)
- Server-Sent Events (SSE) - [guide](https://germano.dev/sse-websockets/)
- Graceful handling(eg. X number of retries before giving up(linear, exponential backoff etc) 
- Error Handling
    * error handling with async/await pattern - [See the section Async Logic and Side Effects](https://redux.js.org/usage/writing-logic-thunks#async-logic-and-side-effects)
- Others
    * [Handle API calls using async await with the useEffect hook](https://javascript.plainenglish.io/handling-api-calls-using-async-await-in-useeffect-hook-990fb4ae423 )
    * [How to use async function in React hooks useEffect](https://javascript.plainenglish.io/how-to-use-async-function-in-react-hook-useeffect-typescript-js-6204a788a435)

<br>

**Optimizing Images**
- Add alt attributes (Images should be descriptive for SEO)
- Load images based on screen size (img srcset)
- Image compression (ex: JPEG 2000) 
    * [Webpack guide](https://lawrencewhiteside.com/courses/webpack-beyond-the-basics/optimizing-asset-files-with-compression/)
- Image sitemaps
- Use SVGs for generic dimensions (in case of stretching of images)
- Discuss about image Sprites for icons
- Discuss about progressive images (ex: Medium.com)
    * [Using blurhash](https://github.com/woltapp/blurhash)

<br>

**Instrumentation**

- Measurement and tracking are key for a stable system 
- Monitoring - [code](https://github.com/philipwalton/blog/tree/main/functions/log) 
- Error logging (for tracing)] - [Using Google Analytics](https://github.com/philipwalton/blog/blob/main/articles/the-ga-setup-i-use-on-every-site-i-build.md#error-tracking)
- Debugging - [Custom Tracking](https://github.com/philipwalton/blog/blob/main/articles/the-ga-setup-i-use-on-every-site-i-build.md#tracking-custom-data)
- Logs/Track all events happened in the application - [code]()
- Implement Analytics (GA) - [this](https://github.com/elgorditosalsero/react-gtm-hook) 
- Sentry (to capture errors) - example - [code](https://github.com/AjayPoshak/blubus/blob/master/client/index.js)
- Newrelic (to detect failures) - [doc](https://docs.newrelic.com/docs/browser/browser-monitoring/installation/install-browser-monitoring-agent) 

<br>

**Versioning of artifacts**
- Artifacts tracking (ex: Confluence)
- Rollback & backup mechanisms

<br>

**Performance Optimization Techniques**
- Webpack to optimized/compressed pages (Code splitting)
     * [Code splitting](https://hackernoon.com/effective-code-splitting-in-react-a-practical-guide-2195359d5d49)
     * [Gzip Compression](https://www.keycdn.com/support/enable-gzip-compression)
     * [Brotli Compression](https://www.fastfwd.com/improve-http-compression-with-brotli/)
    
- Using Web workers
   * [React and Web Workers](https://levelup.gitconnected.com/react-and-web-workers-c9b60b4b6ae8)
   * Example - [code](https://github.com/peterpeterparker/tietracker/tree/main/public/workers)
- [Web Vitals (FP, LCP, CLS, etc)](https://10up.github.io/Engineering-Best-Practices/performance/#core-web-vitals)
- Lighthouse / PageSpeed Insights - [website having 100 score](https://github.com/philipwalton/blog)
- Fast Loading (Initial load should be fast)
    * [List of things to consider for fast load times](https://web.dev/fast/)
    
- Smooth Operations (Loading indicators / Light/Smooth/Meaningful animations (to avoid jerks in transitions) / Splash screens) - (dialog with light animations)
    * Example using react-spring - [code](https://codesandbox.io/embed/7mqy09jyq)
    * [Going jank free - Achieving 60 FPS smooth websites](https://murtada.nl/blog/going-jank-free-achieving-60-fps-smooth-websites)
    
- Animation directions should be the same (dialog coming from bottom should close in bottom) - (smooth animation should be added in sidebars for better UX)
    * Example using react-spring - [code](https://codesandbox.io/embed/morr206pv8)
    * [How To Implement Smooth Scrolling in React](https://www.digitalocean.com/community/tutorials/how-to-implement-smooth-scrolling-in-react)
- Animation between data fetching(APIs request)
    * Skeletal loaders 
         * [Example](https://www.npmjs.com/package/react-loading-skeleton) 
         * Example - [Live](https://fakeflix.th3wall.codes/) -  [code](https://github.com/Th3Wall/Fakeflix)
    * [Using blurhash](https://github.com/woltapp/blurhash)
- Discuss about Caching - ex: API, resource cache (Browser cache / Memory / CDN / Disk Cache)
    * [Guide](https://roadmap.sh/guides/http-caching)
- Pagination vs Infinite Scroll
    * [Implementing pagination](https://www.pluralsight.com/courses/react-managing-large-data-sets)
    * [Implementing infinite scroll](https://www.pluralsight.com/courses/react-managing-large-data-sets)
- Meaningful animation
    * Fakeflix - [example](https://fakeflix.th3wall.codes/) - [code](https://github.com/Th3Wall/Fakeflix)
    * Using framer motion - [live](https://ecom-crwn-clothing.herokuapp.com/)- [code](https://github.com/Th3Wall/react-crwn-cothing-ecom)
- [Micro interactions](https://userguiding.com/blog/microinteraction/)
- React specific issues
    * Fixing Wasterd Rendering, Caching expensive operation results, Reducing bundle sizes, Lazy loading components - [video](https://www.pluralsight.com/courses/optimize-performance-react) [code](https://github.com/hendrikswan/pluralsight-react-performance)
    * Checking Extra Renders - [code](https://github.com/Lemoncode/react-hooks-by-example/tree/master/18-why-did-you-update)
    * [Optimizing React Performance - 12 Tools and Tips](https://www.keycdn.com/blog/react-performance)
    * [Render Performance Optimization With React](https://weareadaptive.com/2020/04/09/render-performance-optimization-react/)

<br>

**Internationalization (i18n) / Localization (i10n)**
- Localization
- Numeric, date and time formats
- Singular &  Plurals
- Use of currency
- Keyboard usage - [example](https://codesandbox.io/s/8x6kzj7zmj?file=/components/List.js)
- Symbols, icons and colors
- Text and graphics vary with different languages and religions, may be subject to misinterpretation or viewed as insensitive
- Varying legal requirements

<br>

 **Accessibility**
- Alt attributes
- Aria-labels - [example code](https://github.com/JasonTarka/a11y-examples)
- Multi-device support, slow network speed
   * [Adaptive Loading](https://addyosmani.com/blog/adaptive-loading/) - [Code](https://github.com/GoogleChromeLabs/adaptive-loading)
- Color contrast, semantics tags - [See this](https://10up.github.io/Engineering-Best-Practices/tools/#a11y-testing)

<br>

**Security**
- MITM
- [XSS](https://auth0.com/blog/cross-site-scripting-xss/)
- CSRF
   * [Content-Security-Policy in Express apps](https://ponyfoo.com/articles/content-security-policy-in-express-apps#to-get-started-let-s-use-report-only )
- Clickjacking
- [Content Security Policy (CSP)](https://www.pluralsight.com/courses/defeating-cross-site-scripting-content-security-policy)
- CORS
- SSL Testing 
    * Deep analysis of the configuration of any SSL web server on the public Internet -[Testing your SSL web server](https://www.ssllabs.com/ssltest/analyze.html)
- Security Headers  
     * Analyzing HTTP response headers for sanity(https://securityheaders.com) - [Example of good report](https://securityheaders.com/?q=https%3A%2F%2Fgodje.nl%2F)
     * badssl - https://badssl.com/

 - Other Tools
   * [HTTP/2 test](https://tools.keycdn.com/http2-test)
   * [HTTP Header Checker](https://tools.keycdn.com/curl)
   * [Website Speed Test](https://tools.keycdn.com/speed)
   * [Performance Test](https://tools.keycdn.com/performance)
   * [Check Font type](https://type-scale.com/)
   * [What Does My Site Cost?](https://whatdoesmysitecost.com/)
   * [HTML5 Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/HTML5_Security_Cheat_Sheet.html)
   * [Production Best Practices: Security](https://expressjs.com/en/advanced/best-practice-security.html)
   * [Web Application Vulnerabilities Index](https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/)

<br>

**Quality assurance and control**
- Stable products are successful
- Specify standards - Code level / Artifacts level / Asset level
    * Code level - Git
    * Artifacts level - Artifactory
    * Asset level - Git/ Blob storage(S3 etc)/CDN 
- Git Hooks (pre commit hooks, husky)
-   * Example - [code](https://gitlab.com/kachkaev/website/-/blob/master/package.json)
-   * Example - [code](https://github.com/philipwalton/blog/blob/main/.husky/pre-commit)
- Linters / Static Analyzers
    * Example - [code](https://github.com/philipwalton/blog/blob/main/.eslintrc)
    * Example - [code](https://github.com/thenewboston-developers/Website/blob/development/.eslintrc.json)
- Unit testing
    * Mocking React Hooks - Example - [blog](https://www.richardkotze.com/coding/mocking-react-hooks-unit-testing-jest) - [code](https://github.com/rkotze/starwars-react-app-tests)
    * React Hooks Testing Library - https://github.com/testing-library/react-hooks-testing-library
    * React Testing Library example - [code](https://fullstackopen.com/en/part5/testing_react_apps)
    * Code accompanying "Testing React with Jest and Testing Library" course on Udemy - [Code](https://github.com/bonnie/udemy-TESTING-LIBRARY)
    * Testing Library - thenewboston website - [live](https://github.com/thenewboston-developers/Website) - [code](https://github.com/thenewboston-developers/Website)
    * React Jest example - [code](https://github.com/securingsincity/react-jest-example)
    * Async testing - [code](https://codesandbox.io/s/react-ts-unit-test-example-kmubx?file=/src/hooks/useStepper/useStepper.test.tsx)
- Workflow testing (User level flows) (Tools - Cypress)   
    * Cypress has a demo real world app that uses best practices - [code](https://github.com/cypress-io/cypress-realworld-app)
    * Artsy.net - [code](https://github.com/artsy/force/tree/main/cypress)
- Integration testing
    * e2e integration test using Mocha and Pupppeteer - [code](https://github.com/anishkny/realworld-e2e-test)
- Automation Suite
    * Using webdriver IO that allows using sauce,browserstack etc - [code](https://github.com/philipwalton/blog/blob/main/wdio.conf.cjs)

- Cross browsers testing
    * Cypress demo app - [code](https://github.com/cypress-io/cypress-realworld-app/blob/develop/bitbucket-pipelines.yml)
    * [Here is how you detect the browser using both JavaScript and CSS](https://medium.com/weekly-webtips/here-is-how-you-detect-the-browser-in-use-in-both-javascript-and-css-bcb5a6458379)
    * [Automated cross browser unit testing](https://github.com/philipwalton/blog/blob/main/articles/learning-how-to-set-up-automated-cross-browser-javascript-unit-testing.md)
- Cross platform testing
    * Cypress demo app - [code](https://github.com/cypress-io/cypress-realworld-app/blob/develop/bitbucket-pipelines.yml)
   
<br>

**Governance**
- Controlling the workflows and protecting the assets
- UX Design -> Developers -> Product Managers -> UX Designing -> QA
- Code level governance - like PRs approval (sets standard in your team)
    * [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- Artifacts/Assets level governance (before go live)
- like Product Manager approval, Stakeholders approvals

<br>

**Experiment based release cycle**
- Experiment flag, which can help in the release cycle
 
  Example : In a recent codebase I worked, we had a flag in the frontend codebase that was enabled/disabled based on the response received from API(in turn , API routes in node.js server were handled in 2 ways : 1) the server code read the values based on the server configuration(ENV values) for that particular deployment 2)actual backend that had its configuration as well) affecting the user experience and user journey.

<br>

**NFR (Non Functional Requirement)**
- Discuss about CI/CD (Docker, Pipeline)
   * Alexander Kachkaev's personal website has a good pipeline setup - see [code](https://gitlab.com/kachkaev/website)
<br>

---

### Codebases + Guides Worth Mentioning Here
* Artsy.net - (https://github.com/artsy/force/)
* thenewboston - (https://github.com/thenewboston-developers/Website)
* fakeflix - (https://github.com/Th3Wall/Fakeflix)
* CRWN Clothing - (https://github.com/Th3Wall/react-crwn-cothing-ecom)
* algorithm-visualizer - (https://github.com/algorithm-visualizer/algorithm-visualizer)
* spotify-clone-client - (https://github.com/JL978/spotify-clone-client)
* The Front-End Checklist - (https://github.com/thedaviddias/Front-End-Checklist)
* Engineering Best Practices - Many sections serve as a good reference - (https://10up.github.io/Engineering-Best-Practices/)
* Zero to production web apps - [code](https://pgjones.dev/tozo/frontend/aims/)

### Boilerplate Code
* [Setup with Node.js web application server acting as a Backend for Frontend](https://github.com/react-boilerplate/react-boilerplate)
* [Next.js setup](https://github.com/UnlyEd/next-right-now)
* [React, Redux, Redux-saga,Styled components boilerplate](https://github.com/gilbarbara/react-redux-saga-boilerplate)
* [SSR boilerplate](https://github.com/cullenjett/react-ssr-boilerplate/)
* [Boilerplate (seed) project for creating web apps with React.js, GraphQL.js and Relay](https://github.com/kriasoft/react-firebase-starter)
* [Boilerplate and tooling for web application development based on React (ReactJS), Redux, Babel, Webpack, CSS Modules, PostCSS, Browsersync, React Hot Loader and optimized for CDN hosting in Firebase](https://github.com/koistya/react-static-boilerplate)
* [Universal React Starter](https://github.com/rkotze/universal-react-starter)
* [New York Times kyt based starterkit](https://github.com/nytimes/kyt)
* [Create React App - Simple Redux Typescript Boilerplate](https://github.com/hammondan/react-redux-typesript-boilerplate)
* [Create React App - react redux redux-saga ant-design tailwind-css boilerplate](https://github.com/dospolov-archive/react-redux-saga-antd-tailwind-boilerplate)

### License

This repository is MIT licensed. [Read more](./LICENSE)
