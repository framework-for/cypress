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

Cypress is a next generation testing tool that enables developers to easily test their web applications. Typically our users are developers or QA engineers building web applications using modern JavaScript frameworks. Cypress enables developers to write **end to end tests**, **integration tests**, and **unit tests** that run in the browser.

Cypress is both a local testing tool, *and* a service. Typically you'd use Cypress locally to write tests **every day** while you build your application. After integrating Cypress into your CI Provider you can have [our Dashboard](https://on.cypress.io/dashboard-features) record your test runs and see the results.

Cypress is most often compared to [**Selenium**](http://www.seleniumhq.org/); however Cypress is both fundamentally and architectually different. Cypress is not bound by the same restrictions as Selenium. Cypress enables you to write faster, more reliable tests and ultimately achieve **much more** test coverage. Cypress fundamentally shifts the way you can test and build your web applications.

## Features
- **Familiar Tools:** built on tools such as [**Mocha**](https://mochajs.org/), [**Chai**](http://chaijs.com/), [**Sinon**](http://sinonjs.org/), and [**Electron**](https://electron.atom.io/)
- **Extensive APIs:** offers over 80+ commands to drive the browser
- **Network Stubbing:** enables you to stub out your backend and mock edge cases
- **Developer Focused:** helps you test every day using your typical development workflow
- **Screenshots / Videos:** automatically records on failures and during headless runs
- **Obvious Errors:** see exactly *what* went wrong so you understand what command failed and *why*
- **Dev Tools / Debugger:** use every developer tool you're used to while you test
- **Time Travel Snapshots:** time travel to every command with the ability to walk back through every test
- **Fast Setup:** get up and running with no additional installation required
- **Blazing Fast Runs:** tests run as fast as your server is capable of delivering content
- **Automatic ES2015 Transpilation:** write modern code with zero configuration

## Our Mission

Cypress is built on the best open source technologies, and naturally we fully embrace open source. It's essential for us to be successful. Our services will always be **optional**, and Cypress itself will always work indepedently of them. Our [Dashboard](https://on.cypress.io/dashboard-features) even runs Public Projects for free - just like [Github](https://github.com/), [TravisCI](https://travis-ci.org/), [CircleCI](https://circleci.com) and other developer tools you know and love.

Our mission is to build a thriving, open source ecosystem that enhances productivity, makes testing a fun enjoyable experience, and generates developer happiness. We hold ourselves accountable to champion a testing process **that actually works**. We expect our [documentation](https://on.cypress.io) to be simple, approachable, not presumptious, and enable you to fully understand not just the **what** but the **why**.

We want to help developers build a new generation of modern applications faster, better, and without the stress and anxiety associated with managing tests and their eventual failures.

We know that in order for us to be successful, that we must enable, nurture and provide a clear path to success for our users. Your test code is an investment into Cypress, and it will never be coupled to us as a company or team. Your code will always run independently and be free from needing us to exist.

We believe testing needs a lot of love, and we are here to foster a tool, service, and community that everyone can learn and benefit from. We're here solving the hardest pain points that every developer working on the web identifies with. We hope that you'll join us in making Cypress a lasting community that helps everyone win.

# Why Cypress?

The way we develop web applications has completely transformed over the last 5 years. The existing testing tools were built for a web that is long gone. When we try to test modern application using old tools, it doesn't work. Over and over again, we find that developers struggle with the following challenges:

- [Project Setup](#project-setup)
- [Writing Tests](#writing-tests)
- [Management](#management)

## Project Setup

Developers often complain how difficult it is to start testing their projects. Oftentimes setup requires a considerable amount of configuration. Setup involves configuring many different tools, installing various browser drivers and writing a lot of boilerplate to get to the first test.

With Cypress, you can write your first passing test in **under 5 minutes**.

Cypress comes fully baked with every tool you need and just works out of the box. It can launch headed browsers and **even run headlessly** without a single additional installation step.

Cypress comes with ES2015 support out of the box and is built on top of:

- [Mocha](https://mochajs.org/)
- [Chai](http://chaijs.com/)
- [Sinon](http://sinonjs.org/)

We provide you both a full GUI experience and offer a programatic [CLI tool](https://docs.cypress.io/docs/cli) to interact with Cypress.

When you [add your first project](https://docs.cypress.io/docs/projects#section-adding-a-new-project), we automatically seed it with example test code and provide you with a fully opinionated project structure.

![project-setup](https://cloud.githubusercontent.com/assets/1268976/23642100/5983acec-02c6-11e7-8951-48cd40cb294b.gif)

## Writing Tests

Relying on [Webdriver's](http://www.seleniumhq.org/projects/webdriver/) architecture often leaves developers struggling to write effective tests. When writing tests, we typically find that:

- Traditional e2e tests run incredibly slow
- Tests are difficult to write
- When errors happen its difficult to debug the root cause
- Stack traces in the terminal are mostly worthless
- You do not have access to Dev Tools
- Tests you do write are oftentimes inconsistent and flaky
- You have very little control over your application

All of these problems stem from the gap between the testing process and the development process. Tests are often written **after** a feature has been implemented. It can sometimes take **longer** to write a passing test for a feature than it took to actually build it!

We've spent years building Cypress to overcome these challenges by rewriting the entire testing architecture and creating a familiar environment in which the developer can build their application and test at **the same time**.

Cypress runs orders of magnitudes faster, provides you the ability to debug your application using the Dev Tools you're already familiar with, and enables you to control the environment of your application just like a unit test.

This enables you (the developer) to actually TDD features as you build them. Instead of manually refreshing the browser and hacking on code - you can iteratively write a partially incomplete test to automate the browser getting to the feature you're working on. As you complete the feature, you can finish the test which means you essentially get the test "for free".

The early adopters of Cypress who've recognized this process have seen a tremendous boost in productivity. Developers end up getting **more** done in a day, in addition to having well factored and tested code.

We fundamentally believe in developer happiness. We've created hundreds of error messages that attempt to explain in simple terms what went wrong. Oftentimes when developers see error messages they are confusing, and result in being "dead ends". We've done our very best (and are always improving) trying to hint, nudge, and explain how to best approach writing and running your tests.

![writing-tests](https://cloud.githubusercontent.com/assets/1268976/23642090/4b1decee-02c6-11e7-8c5c-ac6a0842ae9b.gif)

## Management

With the existing testing tools - after you've spent days, weeks, or even months building up a fleet of tests - you will often run them in CI (Continuous Integration).

The problem we find here is that due to the architecture problems of Selenium, it is nearly impossible to manage these tests. They often fail for "no good reason", and while it is possible - getting screenshots, videos, and logs of what happened takes a lot of work. Without these, debugging failing tests is nearly impossible and it's where time and productivity is lost.

Cypress comes fully baked with video and screenshot support. A video will always be created when you run headlessly, and screenshots will automatically be taken on failure (or when you've manually told us to take one).

We also enable you to **record your test runs** on our [Dashboard](https://on.cypress.io/dashboard). This is a service we've built that gives you easy access to see and share your recorded runs.

Our Dashboard is attempting to solve some of the hardest challenges of managing tests in CI. We are working towards:

- giving you live access to your CI runs
- providing you all network requests / responses you can inspect later
- [providing you logs of **everything** that happened inside of the browser](https://github.com/cypress-io/cypress/issues/448)
- analytics which can tell you details about the overall health of your tests
- an intelligent "diff" of a test which failed today but passed previously
- cross browser support with automatic integration into Sauce Labs + Browser Stack
- screenshot diff'ing for visual regression testing

![dashboard](https://cloud.githubusercontent.com/assets/1268976/23642018/0a8c46c6-02c6-11e7-82b5-2c1690b7dbf3.gif)

# Key Differences

Let's investigate some of the key differences between Cypress and other testing tools.

## A new paradigm

Contracts between client + server. Total control. Unit test like. Less e2e, more integration. Bypass your UI. Take shortcuts. Precision.

**Do not think of Cypress as a 1:1 replacement for Selenium.**

With Cypress you have a **choice** of how to write your tests. You can write "pure" e2e tests which are similar to what you'd write in Selenium. But you can also do much - much more.

Use cases:

- importing your react components and calling methods on them programmatically (unit testing)

We have a lot of recipes showing what Cypress can do.

## Testing Pyramid

Just like a balanced diet, the testing pyramid recommends 3 primary layers of testing.

1. E2E tests
2. Integration tests
3. Unit tests

**E2E tests**
Typically Selenium. It drives the browser like a real user. Your application does what it does. You have very little control. You "act" like a user. Want to test a chat application with 5 users talking in a group? You need 5 different browsers all connected to the same server and sharing state. These tests are fundamentally unscalable and we recommend these as little as possible.

Test the critical paths of your application without any kind of stubbing. This ensures the contract between your backend and frontend services are correct.

If you had a test suite of 1000 tests, no more than about 25-50 of these should be e2e.

There is literally **always** a better, more practical, and reliable way to get teh same amount of value and coverage, but write a faster, tighter test.

**Integration tests**
This is the bread and butter of Cypress. We want you to go out and visit your application, and drive it - but take **as many shortcuts as possible**.

After you've written your login tests above - DO NOT USE YOUR UI TO LOG IN. Simply stitch together the seams of the login experience. In other words, bypass your UI and make the actual request that causes the user to login.

Another approach is to stub out your server altogether and just "trick" your application into thinking it's logged in. This may be by setting something in local storage, a cookie, or by stubbing a function such as a 3rd party oauth lib.

Now you won't be repeating the same UI actions over and over again (which creates no additional value).

This enables you to test the specific feature without the baggage or ceremony of everything it takes to reach that specific state.

Now you can use Cypress to do things like stub network traffic. You could force your API to send you the data you want - you can even build features **without** even having an API at all! This literally enables you to build the frontend and make decisions on the data without it even existing.

Now we can easily do things like test "empty view", test "pagination views" without ever talking or touching our database.

An entire host of e2e problems are avoided and you retain all of the control.

YOU MUST FIND THE SEAMS.

While we make things easy - don't forget Cypress is a progammers tool. You'll need to write code - although you'll find that you don't need to write complex code or actually do a lot of programming.

By following along best practices we will help guide you to write simple, effective tests.

Testing is both an art and a science and it can take awhile before you learn how to be deconstruct your application and tease apart the seams which will enable you to write better, faster tests.

## Debuggability

If you're coming from Selenium / Webdriver you might expect errors to look this like:

<img src="https://cloud.githubusercontent.com/assets/1268976/23825052/a9c1a2b2-0650-11e7-91c3-07ef5ddf9c3d.png" width="75%" />

What's wrong with this error? Well, stack traces in the terminal are essentially useless. Browsers are enormously complex objects, and their behavior cannot possibly be boiled down to a single error (which is just a string of text).

Do you have any idea why this element isn't visible?

These are all valid potential answers:

- You wrote your selector wrong
- Your app just hasn't rendered yet
- Something in your Javascript code is throwing an error
- A network request failed earlier (?)
- A network request is currently in flight
- There is a real regression and a legitimate error

The whole problem is that you cannot easily figure this out.

You're often left wondering:
- is something **really** wrong?
- did I write my test code properly?
- or are my tests just **flaky** for no good reason?

At Cypress, we've built **everything** around solving this fundamental problem. We strive to provide you everything so that you can quickly understand **what** and more importantly **why** something failed.

We've done this by:

- Writing hundreds of custom error messages in plain english
- Referencing you to external documentation for complex errors
- Creating a dashboard to show you your recorded test runs
- Enabling Dev Tools access while tests run
- Adding support for `debugger` in either test code **or** app code
- Snapshotting and time traveling through all commands
- Providing a GUI such as indicating number of elements found for a selector
- Clicking on commands to see additional bits of information
- Logging page events such as XHR's, form submissions, page loads, URL changes

Even when you are testing headlessly and you see an error in the console it'll be much friendly and provide you a lot more data.

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
