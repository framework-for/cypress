<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/1268976/20607953/d7ae489c-b24a-11e6-9cc4-91c6c74c5e88.png"/>
</p>
<p align="center">
  <a href="https://on.cypress.io/changelog">Changelog</a> |
  <a href="https://on.cypress.io">Documentation</a> |
  <a href="https://github.com/cypress-io/cypress/projects">Roadmap</a>
</p>

<h3 align="center">
  Automated testing for the modern web.
</h3>

<p align="center">
  Cypress is a next generation testing tool that helps developers write automated tests for the web.
</p>

# Contents

- Overview
  - Features
  - Our Mission
- Why Cypress?
  - Project Setup
  - Writing Tests
  - Management
- Key Differences
  - A New Paradigm
  - Testing Pyramid
  - Debuggability
  - Error Handling
  - Flakiness
  - Control
  - Network Stubbing
  - Videos / Screenshots
  - Trade Offs
- Further Reading

# Overview

Cypress is a next generation testing tool which enables developers to easily test their appliations.  Typically our users are developers and QA engineers building modern applications using modern stacks in JavaScript frameworks. Cypress enables you to write **end to end tests**, **integration tests**, and **unit tests** which drive the browser - like how a real user would.

Cypress is both a local testing tool, *and* a service. You'll use Cypress to write your tests **every day** while you build your application. When you integrate Cypress into your CI Provider, you can have Cypress record your test runs and make the results available [on our Dashboard](https://on.cypress.io/dashboard-features).

Cypress is most often compared to **Selenium**; however Cypress is both fundamentally and architectually different. You are not bound by the same restrictions as Selenium, which enables you to think differently, write faster, more reliable tests and ultimately achieve **much more**. Cypress creates a new paradigm shift in the way you test and build your web applications.

### Features
- **Familiar Tools** we're built on such as **Mocha**, **Chai**, **Sinon**, and **Electron**
- **Extensive APIs** cover over 80+ commands which drive the browser
- **Networking Stubbing** enables you to stub out your backend and test all edge cases
- **Developer Focused** flow helps you test every day alongside your typical development workflow
- **Screenshot / Video** recording happens automatically on failures and during headless runs
- **Obvious Errors** describe exactly *what* went wrong so you understand what command failed and *why*
- **Dev Tools / Debugger** support means you can use everything you're used to while you test
- **Time Travel Snapshots** are taken on every command, giving you the ability to walk back through a test
- **Fully Baked** with batteries included means you get up and running with no additional installation required
- **Blazing Fast Runs** restart instantly and are completed as fast as your server is capable of delivering content
- **Automatic ES2015 Transpilation** allows you to write modern code with zero configuration

### Our Mission

Cypress is built on the best open source technologies, and naturally we fully embrace open source in order to be successful. Our Dashboard runs Public Projects for free - just like Github, TravisCI, CircleCI, and most other developer tools you know and love.

Open source, developer productivity and happiness. Create an ecosystem that thrives. Champion a testing process that is effective, fast, and consistent. Help developers build a new generation of modern applications faster, better, and without stress or anxiety.

Your tests will never live or die by us. They are yours, part of your source, your investment, and nothing will ever stop them from running.

To be successful you must enable, nurture and provide a path to success for users. We want you to build, extend, fix, support, and enhance Cypress. Testing needs a lot of love, and we are here to foster this into an ecosystem everyone can learn and benefit from.

# Why Cypress?

The way we develop web applications has completely transformed over the last 5 years. The existing testing tools were built for a web that is long gone. When we try to test modern application using old tools, it doesn't work. Over and over again, we find that developers struggle with the following challenges:

- Setup
- Writing
- Management

### Project Setup

Developers often complain how difficult it is to started testing their projects. Oftentimes setup requires a considerable amount of configuration, it involves cobbling together many different tools, installing various browser drivers, and writing a lot of boilerplate to get to the first test.

**With Cypress, we want you to go from nothing to your first passing test in under 5 minutes.**

Cypress comes fully baked with every tool you need and should "just work" out of the box. It can launch headed browsers and **even run headlessly** without a single additional installation step.

We've built on top of tools you're likely already familiar with and have designed our API's to leverage existing knowledge you likely already possess. We're not reinventing the wheel, we just trying to be the iPhone replacing morse code.

Cypress comes with ES2015 support out of the box and is built on top of:

- Mocha
- Chai
- Sinon

We provide you both a full GUI experience and offer a programatic CLI tool to interact with Cypress.

When you add your first project, we automatically seed it with example test code and provide you a fully opinionated project structure.

![project-setup](https://cloud.githubusercontent.com/assets/1268976/23642100/5983acec-02c6-11e7-8951-48cd40cb294b.gif)

### Writing Tests

Because of Webdriver's architecture, developers often struggle to write effective tests. Here we typically find that:

- traditional e2e tests run incredibly slow
- tests are difficult to write
- when errors happen its difficult to pinpoint the root cause
- stack traces in the terminal are mostly worthless
- you do not have access to Dev Tools
- tests you do write are oftentimes inconsistent and flaky
- you have very little control over your application

All of these problems manifest them by creating misalignment between the testing process and the development process. Tests are often written **after** a feature has been created. It can sometimes take **longer** to write a passing test for a feature than it took to actually build it!

We've spent years building Cypress to overcome these challenges by rewritting the entire testing architecture and creating a familiar environment in which the developer can build their application and test all at **the same time**.

Cypress runs orders of magnitudes faster, provides you the ability to debug your application using the Dev Tools you're already familiar with, and enables you to control the environment of your application just like a unit test.

This enables you (the developer) to actually TDD features as you build them. Instead of manually refreshing the browser and hacking on code - you can iteratively write a partially incomplete test to automate the browser getting to the feature you're working on. As you complete the feature, you can finish the test which means you essentially get the test "for free".

The early adopters of Cypress who've recognized this process have seen a tremendous boost in productivity. Developers end up getting **more** done in a day, in addition to having well factored and tested code.

We fundamentally believe in developer happiness. We've created hundreds of error messages that attempt to explain in simple terms what went wrong. Oftentimes when developers see error messages they are confusing, and result in being "dead ends". We've done our very best (and are always improving) trying to hint, nudge, and explain how to best approach writing and running your tests.

![writing-tests](https://cloud.githubusercontent.com/assets/1268976/23642090/4b1decee-02c6-11e7-8c5c-ac6a0842ae9b.gif)

### Management

With the existing testing tools - after you've spent days, weeks, or even months building up a fleet of tests - you will often run them in CI (Continuous Integration).

The problem we find here is that due to the architecture problems of Selenium, it is nearly impossible to manage these tests. They often fail for "no good reason", and while it is possible - getting screenshots, videos, and logs of what happened takes a lot of work. Without these, debugging failing tests is nearly impossible and it's where time and productivity goes to die.

Cypress comes fully baked with video and screenshot support. A video will always be created when you run headlessly, and screenshots will automatically be taken on failure (or when you've manually told us to one one).

We also enable you to **record your test runs** on our [Dashboard](https://on.cypress.io/dashboard). This is a service we've built which gives you easy access to see and share your recorded runs.

**This is just the tip of the iceberg.**

Our Dashboard is attempting to solve some of the hardest challenges of managing tests in CI. We are working towards:

- giving you live access to your CI runs
- providing you all network requests / responses you can inspect later
- providing you logs of **everything** that happened inside of the browser
- analytics which can tell you details about the overall health of your tests
- an intelligent "diff" of a test which failed today but passed previously
- cross browser support with automatic integration into Sauce Labs + Browser Stack
- screenshot diff'ing for visual regression testing

![dashboard](https://cloud.githubusercontent.com/assets/1268976/23642018/0a8c46c6-02c6-11e7-82b5-2c1690b7dbf3.gif)

# Key Differences

### A new paradigm

Contracts between client + server. Total control. Unit test like. Less e2e, more integration. Bypass your UI. Take shortcuts. Precision.

**Do not think of Cypress as a 1:1 replacement for Selenium.**

With Cypress you have a **choice** of how to write your tests. You can write "pure" e2e tests which are similar to what you'd write in Selenium. But you can also do much - much more.

Use cases:

- importing your react components and calling methods on them programmatically (unit testing)

We have a lot of recipes showing what Cypress can do.

### Testing Pyramid

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

### Architecture

Cypress is not built on **Selenium / Webdriver**. While it's possible we may use Webdriver for very specific tasks in the future, our automation layer is completely different.

Cypress ends up actually being the host application, while your application is tested **through** Cypress itself.

This means we run in the same run loop as your application - we can listen to events from your application and respond in real time. It's impossible for us to "miss" elements, we automatically know that your elements are animating, are disabled, are readonly, when your page is unloading and transitioning, when your page *hasn't* loaded yet, when network requests are being sent and when responses have come back.

Whereas Webdriver is a stateless API that shoots remote commands into the browser (thus making it a black box) - because Cypress is surrounding your application that puts us in a vastly superior position.

Cypress works as much as possible in regular Javascript, but can (and does) go outside of the Javascript sandbox for specific automation tasks.

This means we have the best of both worlds - if we want to synchronously query for elements we can - or if we want to talk to the browser's automation API's which are only exposed outside of Javascript we can do that too.

This gives us flexibility and we can yield that same choice and flexibility back to the developer.

# Further Reading

Now that you have an idea of where we're going with Cypress, let's dive in!

Link | Description
:--- | :---
[Documentation](https://on.cypress.io) | Guides, API Commands, and lots of examples
[Changelog](https://on.cypress.io/changelog) | Notes for new Cypress versions
[Examples](https://on.cypress.io/all-example-apps) | Full example applications
[Recipes](https://github.com/cypress-io/cypress-example-recipes) | Specific tasks and approaches
[Roadmap](https://on.cypress.io/roadmap) | Upcoming major milestones we're working on
[Talks](https://www.cypress.io/explore) | Conference talks, interviews, podcasts, and shows
