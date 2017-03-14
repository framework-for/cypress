<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/1268976/20607953/d7ae489c-b24a-11e6-9cc4-91c6c74c5e88.png"/>
</p>
<p align="center">
  <a href="https://on.cypress.io/changelog">Changelog</a> |
  <a href="https://on.cypress.io">Documentation</a> |
  <a href="https://github.com/cypress-io/cypress/projects">Roadmap</a>
</p>

<h3 align="center">
  Automated testing for the modern web
</h3>

<p align="center">
  Cypress is a next generation testing tool that helps developers write tests while building apps.
</p>

# Contents

- [Overview](#overview)
  - [Features](#features)
  - [Our Mission](#our-mission)
- [Why Cypress?](#why-cypress)
  - [Project Setup](#project-setup)
  - [Writing Tests](#writing-tests)
  - [Management](#management)
- [Key Differences](#key-differences)
  - [A New Paradigm](#a-new-paradigm)
  - [Testing Pyramid](#testing-pyramid)
  - [Debuggability](#debuggability)
  - [Flakiness](#flakiness)
  - [Control](#control)
  - [Network Stubbing](#network-stubbing)
  - [Videos / Screenshots](#videos--screenshots)
  - [Architecture](#videos--screenshots)
  - [Trade Offs](#trade-offs)
- [Further Reading](#further-reading)

# Overview

Welcome to Cypress: the next-generation testing tool for front-end professionals!

Typically, our users are developers or QA engineers building web applications using modern JavaScript frameworks. Cypress enables us to write **end to end tests**, **integration tests**, and **unit tests**, all of which run in the browser.

Cypress is at once an open source local testing tool *and* a value-added service for continuous integration. At first, we use Cypress to write tests **every day** as we build our application locally (we can even use TDD if we prefer). Later, once we've integrated Cypress with our CI Provider, the [Cypress Dashboard](https://on.cypress.io/dashboard-features) records our test runs and clearly presents the results (so we never have to ask "Why did this fail?")

Cypress is most often compared to [**Selenium**](http://www.seleniumhq.org/); however Cypress is both fundamentally and architecturally different. Cypress is not bound by the same restrictions as Selenium. Cypress enables us to write faster, more reliable tests that achieve **much more** test coverage. Cypress fundamentally shifts the way we test and build web applications.

## Features
- **Familiar Tools:** built on the shoulders of such giants as [**Mocha**](https://mochajs.org/), [**Chai**](http://chaijs.com/), [**Sinon**](http://sinonjs.org/), and [**Electron**](https://electron.atom.io/)
- **Extensive APIs:** offers over 80+ commands to intuitively drive the browser
- **Network Stubbing:** easily mock edge cases; or, isolate from the back-end completely
- **Developer Focused:** plugs directly into our existing development workflow
- **Screenshots / Videos:** great, visual feedback for failures and headless runs
- **Obvious Errors:** see exactly *what* went wrong and, more importantly, *why*
- **Dev Tools / Debugger:** we can use all of our favorite developer tools while we test
- **Time Travel Snapshots:** time travel to any command; step back through every test
- **Fast Setup:** get up and running with no additional installation required
- **Blazing Fast Runs:** tests run as fast as our server can deliver the content
- **ES2015 Friendly:** write modern code with zero configuration

## Our Mission

Cypress is built on best-of-breed, industry-standard technologies, which naturally means we fully embrace open source. It's essential for us to be successful. Our paid services will always be **optional** and Cypress itself will always work independently of them. Our [Dashboard](https://on.cypress.io/dashboard-features) even runs Public Projects for free - just like [Github](https://github.com/), [TravisCI](https://travis-ci.org/), [CircleCI](https://circleci.com) and other developer tools we all know and love.

Our mission is to build a thriving, open source ecosystem that enhances productivity, makes testing an enjoyable experience, and generates developer happiness. We hold ourselves accountable to champion a testing process **that actually works**. We expect our [documentation](https://on.cypress.io) to be simple and approachable, enabling the reader to fully understand not just **what**, but **why**.

We want to help developers build a new generation of modern applications faster, better, and without the stress and anxiety associated with managing tests and their eventual, inevitable failures.

We know that in order for us to be successful we must enable, nurture, and provide a clear path to success for our users. Every line of test code is an investment in the Cypress ecosystem, it will never be coupled to us as a company or a team. Tests written in Cypress-the-application will run completely independently of Cypress-the-company, *always*.

We believe testing needs a lot of love, and we are here to foster a tool, a service, and a community that everyone can learn and benefit from. We're solving the hardest pain points shared by every developer working on the web. We believe in this mission and hope that many will join us to make Cypress a lasting community that helps everyone win.

# Why Cypress?

The way we develop web applications has completely transformed over the last 5 years. The existing testing tools were built for a web that is long gone. When we try to test modern application using old tools, it doesn't work. Over and over again, we struggle with the following challenges:

- [Project Setup](#project-setup)
- [Writing Tests](#writing-tests)
- [Management](#management)

## Project Setup

Developers often complain how difficult it is to start testing their projects. Often, setup requires considerable configuration of many different tools, installing various browser drivers, and writing boilerplate to get to the first test.

With Cypress, we get to our first passing test in **under 5 minutes**.

Cypress comes fully baked with every tool we need and Just Works right out of the box. It can launch headed browsers and **even run headlessly** without a single additional installation step.

Cypress comes with ES2015 support out of the box and is built on top of:

- [Mocha](https://mochajs.org/) rock-solid and configurable test runner
- [Chai](http://chaijs.com/) versatile assertion library
- [Sinon](http://sinonjs.org/) toolbox of spies, stubs, mocks, etc

We provide a full GUI experience and a programmatic [CLI tool](https://docs.cypress.io/docs/cli) to interact with Cypress.

When [adding our first project](https://docs.cypress.io/docs/projects#section-adding-a-new-project), Cypress automatically seeds it with example test code and a fully opinionated project structure.

![project-setup](https://cloud.githubusercontent.com/assets/1268976/23642100/5983acec-02c6-11e7-8951-48cd40cb294b.gif)

## Writing Tests

Relying on [Webdriver's](http://www.seleniumhq.org/projects/webdriver/) architecture often leaves developers struggling to write effective tests. When writing tests, we typically find that:

- Tests are unreasonably difficult to write
- Tests are painfully slow to run
- When errors happen, it's difficult to discern the root cause
- Stack traces in the terminal are frequently worthless
- We do not have access to Dev Tools
- Tests are often inconsistent and flaky
- We have little control over our application under test

These problems stem from the gap between the testing process and the development process. Tests are often written **after** a feature has been implemented. It can take **longer** to write a passing test for a feature than it took to actually build the feature itself!

In order for Cypress to overcome these challenges, we've spent years rewriting the entire testing architecture and creating a familiar environment in which the developer can build their application and the tests that drive it **at the same time**. (We believe in it so much that we've built Cypress itself this way!)

Cypress can run orders of magnitude faster, provides us the ability to debug our applications using the Dev Tools we're already familiar with, and enables us to control our application's environment just like a unit test. This enables an innovative kind of front-end TDD flow for features *as we build them*: instead of manually refreshing the browser and hacking on code, we iteratively build up a test in tandem with the feature. First, we use Cypress as an automation tool, driving the application itself to the feature we're working on. As the details of the feature arise, we encode them into the test, ensuring correctness as we work. Finally, when we lean back and look over the feature we get a strange and wonderful sense that we got the test "for free".

The early adopters of Cypress who've recognized this process have seen a tremendous boost in productivity. Developers end up getting **more** done in a day, in addition to having well-factored and well-tested code.

We fundamentally believe in developer happiness. As a result, we've created hundreds of custom error messages that attempt to explain in simple terms what went wrong. Usually, when a developer first sees a new error message, it can be confusing and too often leads to "dead ends". We've done our very best (and are always improving) at hinting, nudging, and explaining how to best approach writing and running tests.

![writing-tests](https://cloud.githubusercontent.com/assets/1268976/23642090/4b1decee-02c6-11e7-8c5c-ac6a0842ae9b.gif)

## Management

Now that we've spent all this time building up a fleet of tests -- or perhaps because we've got many collaborators and need to coordinate -- we turn to CI (Continuous Integration) to ease the burden of ensuring they pass every time anyone commits new code.

The problem we find here is that, due to the architecture problems of Selenium, it is nearly impossible to manage these tests. They often fail for "no good reason" and we're left scrambling to figure out how to extract useful artifacts like screenshots, videos, and logs of what happened. This takes a lot of work! But without these, debugging failing tests is nearly impossible, leading to wasted time and lost productivity.

Cypress comes fully baked with video and screenshot support. A video is always created when we run headlessly, and screenshots are automatically taken on failure (as well as on-demand when our test code asks for them).

Cypress also enables us to seamlessly **upload and share our test runs** through the [Dashboard](https://on.cypress.io/dashboard). This service provides easy access to see and share recorded runs.

Our Dashboard is attempting to solve some of the hardest challenges of managing tests in CI. We are working towards:

- providing live access to CI runs
- providing all network requests / responses for inspection
- [providing logs of **everything** that happened inside of the browser](https://github.com/cypress-io/cypress/issues/448)
- analytics which provide insight about the overall health of our tests
- an intelligent "diff" of a test which failed today but passed previously
- cross-browser support with automatic integration into Sauce Labs + Browser Stack
- screenshot diff'ing for visual regression testing

![dashboard](https://cloud.githubusercontent.com/assets/1268976/23642018/0a8c46c6-02c6-11e7-82b5-2c1690b7dbf3.gif)

# Key Differences

Let's investigate some of the key differences between Cypress and other testing tools.

## A New Paradigm

Contracts between client + server. Total control. Unit test like. Less e2e, more integration. Bypass the UI. Take shortcuts. Be precise.

**Do not think of Cypress as a 1:1 replacement for Selenium.**

With Cypress, we have a **choice** about how to we write our tests. We can write "pure" e2e tests, which are similar to what we've done in the past with Selenium. But we can also do **much, much more**.

Use cases:

- importing our react components and calling methods on them programmatically (unit testing)
- short-circuiting our authentication flow when it isn't the system-under-test (huge speed boosts)
- mocking/stubbing XHRs completely (SPAs where the front-end is a stand-alone app)

We have a lot of [recipes showing what Cypress can do](https://github.com/cypress-io/cypress-example-recipes).

## Testing Pyramid

Just like a balanced diet, the testing pyramid recommends 3 primary layers of testing.

1. End-to-End Tests
2. Integration Tests
3. Unit Tests

### End-to-End Tests

End-to-end tests are what we typically do with Selenium. It drives the browser like a real user. The application does what it does and we have very little control. The tests "act like a user". Want to test a chat application with 5 users talking in a group? 5 separate browsers are needed, all connected to the same server and sharing state. **These tests are fundamentally unscalable and we recommend these as little as possible**.

Test the critical paths of the application without any kind of stubbing. This ensures the contract between the back-end and front-end services match up.

The pyramid suggests that these tests should be in shortest supply. In a test suite of 1000 tests for example, no more than about 25-50 of these should be e2e.

There is **always** a better, more practical, and more reliable way to get the same value and coverage while writing a faster, tighter test.

### Integration Tests

This is the bread and butter of Cypress. We still want to visit our application and drive it like a user - but we'll take **as many shortcuts as possible**.

A great example is authentication. We'll certainly write some tests the exercise the login functionality itself, but once that is done we want to avoid repeating those steps for every test. Repeating for emphasis: **WE DO NOT USE THE UI TO LOG IN**. Instead, we simply stitch together the seams of the login experience. In other words, bypass the UI and make the actual request that causes the user to log in.

Another approach is to stub out the server altogether and "trick" the application into thinking it's logged in. This might be done by setting a value in local storage or a cookie, or by stubbing a function such as a 3rd-party OAuth library.

Now we aren't repeating the same UI actions over and over again with each test (which creates no additional value but certainly slows things down!) We can test specific features without the baggage and ceremony of driving the app into a specific state via its UI for each test.

Cypress can also stub network traffic, giving us unprecedented control of the seam between the client and server. We can make the back-end return whatever data we want, for example when the API is in flux, or before the API even exists at all! (The Cypress team itself leverages this workflow to build up the experience and application flow we desire before ever writing a line of back-end/API code.)

Now we can easily do things like test our "empty" views and "pagination" views without ever sending a request or touching a database.

An entire host of e2e problems are avoided and we retain complete control.

SEEK THE SEAMS

While Cypress makes things easy, it is still a programmer's tool. We know we will be writing code to achieve our goals, but we are continually surprised by how little complexity is necessary. By following the best practices, we can achieve simple, declarative, and effective tests.

Testing is both an art and a science, and Cypress brings new concepts to the table as well. We know it takes time to deeply understand this new paradigm and let go the patterns of the past which no longer serve us. Cypress enables a new workflow and we have to learn to deconstruct our applications in new ways, teasing apart the seams to enable better, faster tests.

## Debuggability

If you're coming from Selenium / Webdriver you might expect errors to look this like:

<img src="https://cloud.githubusercontent.com/assets/1268976/23825052/a9c1a2b2-0650-11e7-91c3-07ef5ddf9c3d.png" width="75%" />

Browsers are enormously complex objects, and their behavior is difficult to be explained in a single error (which is just a string of text).

Can you guess why the element above is not visible?

These are multiple potential answers:

- The selector was written incorrectly
- The app hasn't rendered yet
- There's an error being thrown in the app's JavaScript code
- A network request failed to respond and the element's visibility depends on it
- A network request is still in flight
- There is a real regression and a legitimate error

The problem with existing test frameworks is that it's difficult to find the source of test errors.

You're often left wondering:
- is something **really** wrong?
- did I write my test code properly?
- or are my tests just **flaky**?

At Cypress, we've built **everything** around solving this fundamental problem. We strive to provide you everything so that you can quickly understand **what** and more importantly **why** something failed.

We've done this by:

- Writing hundreds of custom error messages in plain English
- Referencing you to external documentation for complex errors
- Creating a dashboard to show you the recorded test runs
- Enabling Dev Tools access while tests run
- Adding support for `debugger` in either test code **or** app code
- Snapshotting and time traveling through all commands
- Providing a GUI that indicates the state of commands like the number of elements found for a selector
- Displaying additional commands information on click
- Logging page events such as XHR's, form submissions, page loads and URL changes

Even when you are testing headlessly and you see an error in the console it's friendlier and provides a lot more data.

Beyond just a friendly error, you'll also able to watch a video, see command logs, view screenshots, and soon you'll have [logs for literally everything that happened in the browser](https://github.com/cypress-io/cypress/issues/448) to help you track down a failure.

***

### Error Messages

<img src="https://cloud.githubusercontent.com/assets/1268976/23826334/81319bdc-0668-11e7-9801-f92d53ddc887.png" width="50%" />

<img src="https://cloud.githubusercontent.com/assets/1268976/23826333/81317fee-0668-11e7-896b-1b7f91de8b31.png" width="50%" />

***

### Complex Errors

<img src="https://cloud.githubusercontent.com/assets/1268976/21284187/5374b152-c3e2-11e6-9811-c79ead05930b.png" width="50%" />

<img src="https://cloud.githubusercontent.com/assets/1268976/12061262/4f9a252e-af4f-11e5-9139-9c8bdb08ae58.png" width="50%" />

***

### Debugger Support

**In test code:**

<img src="https://cloud.githubusercontent.com/assets/1268976/23826393/56d1adf4-0669-11e7-9612-a55ab59c5e4c.png" width="50%" />

**In app code:**

<img src="https://cloud.githubusercontent.com/assets/1268976/23826394/56d2be7e-0669-11e7-9b70-dbbc6cd55bda.png" width="50%" />

***

### GUI Indicators

**Page Events:**

![screen shot 2017-03-11 at 2 58 43 pm](https://cloud.githubusercontent.com/assets/1268976/23826595/ed3272ee-066c-11e7-8a65-e82b7d70658d.png)

**Number of elements found:**

![screen shot 2017-03-11 at 2 57 47 pm](https://cloud.githubusercontent.com/assets/1268976/23826557/6866da8c-066c-11e7-83fc-e3c22dcce767.png)

**Command Inspection / Time Travel:**

<img src="https://cloud.githubusercontent.com/assets/1268976/23826781/144e60e0-0672-11e7-995d-64e92bc43e65.gif" width="80%" />

## Flakiness

- Webdriver remote protocol is the problem
- Doesn't understand what's going on in the page
- Cypress innovative assertions to page state
- Never explicit waits
- Can modify its behavior in real time

## Control

- Native access to every object
- Spying / stubbing support
- Network traffic stubbing
- Waiting on request / responses
- Assertions on requests
- Edge case management
- Tighter control between the server + client

## Networking Stubbing

- Control webserver
- Build without even having a server

## Videos / Screenshots

- Headless video recording
- Screenshots when tests fail
- Hosted on our dashboard

## Architecture

Cypress is not built on **Selenium / Webdriver**. While it's possible we may use Webdriver for very specific tasks in the future, our automation layer is completely different.

Cypress ends up actually being the host application, while your application is tested **through** Cypress itself.

This means we run in the same run loop as your application - we can listen to events from your application and respond in real time. It's impossible for us to "miss" elements, we automatically know that your elements are animating, are disabled, are readonly, when your page is unloading and transitioning, when your page *hasn't* loaded yet, when network requests are being sent and when responses have come back.

Whereas Webdriver is a stateless API that shoots remote commands into the browser (thus making it a black box) - because Cypress is surrounding your application that puts us in a vastly superior position.

Cypress works as much as possible in regular Javascript, but can (and does) go outside of the Javascript sandbox for specific automation tasks.

This means we have the best of both worlds - if we want to synchronously query for elements we can - or if we want to talk to the browser's automation API's which are only exposed outside of Javascript we can do that too.

This gives us flexibility and we can yield that same choice and flexibility back to the developer.

## Trade Offs

- One superdomain per test
- One browser
- Some restrictions / less restrictions
- More control
- Security restrictions
- Not for crawling the web
- Not really for existing production applications
- Not all API's have been implemented
- No cross browser support
- No native events (yet)
- Developer / QA engineer focused (must understand your app)

# Further Reading

Now that you have an idea of where we're going with Cypress, let's dive in!

Link | Description
:--- | :---
[Documentation](https://on.cypress.io) | Guides, API Commands, and lots of examples
[Changelog](https://on.cypress.io/changelog) | Notes for new Cypress versions
[Examples](https://on.cypress.io/all-example-apps) | Full example applications
[Recipes](https://github.com/cypress-io/cypress-example-recipes) | Specific tasks and approaches
[Roadmap](https://on.cypress.io/roadmap) | Upcoming major milestones we're working on
[Talks](https://www.cypress.io/explore) | Official conference talks, interviews, podcasts, and shows
[News](https://www.cypress.io/explore) | An unofficial list of 3rd party blogs and articles
