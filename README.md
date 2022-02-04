# system-design-react-code-examples
A curation of code examples and in depth technical implementation approaches to solve the common frontend system design issues in React.

---
### Target Audience 
1) intermediate developers wishing to get better technical understanding 
2) developers exploring how to do handle technical things in their own projects.

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
- [1](https://www.alibabacloud.com/blog/front-end-performance-optimization-with-accelerated-compositing-part-1_594194)
- [SSR-based Optimization of Double 11 Virtual Venue – A More Complex Rendering Architecture](https://www.alibabacloud.com/blog/ssr-based-optimization-of-double-11-virtual-venue-a-more-complex-rendering-architecture_596970?spm=a2c65.11461447.0.0.5c88790bSaSVAr)
- [2](https://www.alibabacloud.com/blog/front-end-performance-optimization-with-accelerated-compositing-part-2_594195?spm=a2c65.11461447.0.0.5c88790bSaSVAr)

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
- Tech stack
- Search Engine Optimization
- CI/CD
- User Experience
- A/B testing
- MVP planning
- Server Side Architecture
- Security
- State Management
- Internationalization
- E2E testing
- Tools Integration
- Authentication & Authorization
- Quality Assurance & Control
- User role management

---

### Low Level Design

- Code/Folder architecture
- Desktop/Mobile first approach
- System breakdown
- Component Design
- Form development
- Storage management
- API Design
- Instrumentation
- Design system
- Routing management
- CSS optimizations
- Lazy loading of modules
- Accessibility
- Image optimizations
- Pagination, Debouncing, Throttling
- Performance: FCP, LCP, TTI, CLS
- Versioning
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
- Server Side Rendering
    * SSR (https://survivejs.com/webpack/output/server-side-rendering/)
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
    - Is your application Canvas (or SVG) heavy? (Figma, Draw.io)
    - Is your application webRTC heavy? (Video streaming)

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
- Identify QPS (Queries per second)
- Discuss about Load testing/Stress testing
- Inject analytics in application (ex: Google analytics, Sentry, NewRelic)
- Analytics data helps us to scale the system

<br>

**SEO (Search Engine Optimization)**
- Crawling
- Use of Heading tags
- Semantic tags
- Site Ranking
- Sitemap
- Meta Keywords
- Organic approach vs Inorganic approach
- Use of alt tags
- 301 Redirects (bad for SEO)
- Robots.txt
- Open graph protocol (https://ogp.me/) for social graph

<br>

**Component Based Design**
- Component wise deployment cycle (CI/CD)
- Monolith vs Microservice architecture
- Micro Frontend (independent dev & deployment for scalability)
 * Topcoder Platform Microfront Earn App - [code](https://github.com/topcoder-platform/micro-frontends-earn-app/tree/responsive)
- Static components vs Dynamic components 
- IFrame/Shell approach

<br>

**State Management**
- How to maintain state through the application?
- How to manage users' data?
- State management Libraries (Redux, Flux, NgRX)
    * Redux-saga
        * Example Codebase
    * RxJS
    * Redux Thunk

<br>

**Handling APIs**
- Polling (Short and Long)
- Web Sockets (Real-time) (ex: chat, shared editors)
- Batch requests
- GraphQL
- Caching GET APIs (Middleware concepts to cache response)
- Server-Sent Events (SSE)
- Gracefult handling 
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

<br>

**Instrumentation**
- Measurement and tracking are key for a stable system
- Monitoring
- Error logging (for tracing)
- Debugging
- Logs/Track all events happened in the application
- Implement Analytics (GA)
- Sentry (to capture errors)
- Newrelic (to detect failures)

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
- Web Vitals (FP, LCP, CLS, etc)
- Lighthouse / PageSpeed Insights
- Fast Loading (Initial load should be fast)
    * [List of things to consider for fast load times](https://web.dev/fast/)
- Smooth Operations (Loading indicators / Light/Smooth/Meaningful animations (to avoid jerks in transitions) / Splash screens) - (dialog with light animations)
- Animation directions should be the same (dialog coming from bottom should close in bottom) - (smooth animation should be added in sidebars for better UX)
- Animation between data fetching(APIs request)
- Discuss about Caching - ex: API, resource cache (Browser cache / Memory / CDN / Disk Cache)
- Pagination vs Infinite Scroll
  * [Implementing pagination](https://dev.to/potouridisio/the-only-pagination-you-ll-ever-need-1-2-3-4-5-4il5)
  * 
- Meaningful animation
- Micro interactions
- React specific issues
    * Fixing Wasterd Rendering, Caching expensive operation results, Reducing bundle sizes, Lazy loading components - [video](https://www.pluralsight.com/courses/optimize-performance-react) [code](https://github.com/hendrikswan/pluralsight-react-performance)
    * Checking Extra Renders - [code](https://github.com/Lemoncode/react-hooks-by-example/tree/master/18-why-did-you-update)
    * [Optimizing React Performance - 12 Tools and Tips](https://www.keycdn.com/blog/react-performance)

<br>

**Internationalization (i18n) / Localization (i10n)**
- Localization
- Numeric, date and time formats
- Singular &  Plurals
- Use of currency
- Keyboard usage
- Symbols, icons and colors
- Text and graphics vary with different languages and religions, may be subject to misinterpretation or viewed as insensitive
- Varying legal requirements

<br>

 **Accessibility**
- Alt attributes
- Aria-labels
- Multi-device support, slow network speed
 * [Adaptive Loading](https://addyosmani.com/blog/adaptive-loading/) - [Code](https://github.com/GoogleChromeLabs/adaptive-loading)
- Color contrast, semantics tags

<br>

**Security**
- MITM
- XSS
- CSRF
- Clickjacking
- Content Security Policy (CSP)
- CORS
- SSL Testing 
    * Deep analysis of the configuration of any SSL web server on the public Internet -[Testing your SSL web server](https://www.ssllabs.com/ssltest/analyze.html)
- Security Headers  
     * Analyzing HTTP response headers for sanity(https://securityheaders.com) - [Example of good report](https://securityheaders.com/?q=https%3A%2F%2Fgodje.nl%2F)

 - 

<br>

**Quality assurance and control**
- Stable products are successful
- Specify standards - Code level / Artifacts level / Asset level
- Git Hooks (pre commit hooks, husky)
- Linters / Static Analyzers
- Unit testing
- Workflow testing (User level flows) (Tools - Cypress)
- Integration testing
- Automation suite
- Cross browsers testing
- Cross platform testing

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

<br>

**NFR (Non Functional Requirement)**
- Discuss about CI/CD (Docker, Pipeline)
<br>

---

### License

This repository is MIT licensed. [Read more](./LICENSE)
