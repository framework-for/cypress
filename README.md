<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/1268976/20607953/d7ae489c-b24a-11e6-9cc4-91c6c74c5e88.png"/>
</p>
<p align="center">
  <a href="https://on.cypress.io/changelog">Changelog</a> |
  <a href="https://on.cypress.io">Documentation</a> |
  <a href="https://github.com/cypress-io/cypress/projects">Roadmap</a>
</p>

<h3 align="center">
  Testing, the way it should be.
</h3>

<p align="center">
  Cypress is a next generation testing tool that helps developers write automated tests for the web.
</p>

# Contents

- Overview
  - Why Cypress?
  - Goals
- In Action
  - Talks
  - Videos
- Architecture
  - Differences
  - Debuggability
  - Error Handling
  - Preventing Flake
  - Javascript Events
- Repos
- FAQ
  <!-- - Is Cypress publicly available? -->
  <!-- - Is Cypress Open Source? -->
  <!-- - Is this a commercial project? -->
  <!-- - What kind of projects work well? -->
  <!-- - What kind of projects don't work so well? -->
  <!-- - Can I run this on my CI Server? -->
  <!-- - Does Cypress support cross browser testing? -->
- Roadmap
- Examples
- Contributing
- Legal

# Overview

Cypress is a testing tool written entirely in Javascript that focuses on developers building modern applications. Cypress is used by developers to write **end to end** and **integration tests** which drive the browser - like how a real user would.

Cypress is most often compared to **Selenium**; however Cypress is both fundamentally and architectually different. You are not bound by the same restrictions as Selenium, which enables you to think differently, write faster, more reliable tests and ultimately achieve **much more**.

### Features
- **Familiar Tools** we've built on such as **Mocha**, **Chai**, **Sinon**, and **Electron**.
- **Extensive APIs** cover over 80+ commands which drive the browser.
- **Networking Stubbing** means that you can stub out your backend and test more situations
- **Developer Focused** flow helps you test every day alongside your typical development workflow
- **Screenshot / Video** recording happens automatically on failures and during headless runs
- **Obvious Errors** describe exactly *what* went wrong so you understand what command failed and more importantly *why*
- **Dev Tools / Debugger** support means you can use everything you're used to while you test
- **Time Travel Snapshots** are taken on every command, giving you the ability to walk back through a test
- **Blazing Fast Performance** means that tests rerun instantly and as fast as your server is capable of delivering content

## Why Cypress?

We believe that the current state of the testing ecosystem is broken. Over and over again, we find that developers struggle with the following challenges:

- Setup
- Writing
- Management

### Project Setup

Developers find it hard just to get started testing their projects. Oftentimes this requires a tremendous amount of configuration, it involves cobbling together many different tools, installing various browser drivers, and writing a ton of boilerplate to get to the first test.

Cypress comes fully baked with everything you need to start testing. Our goal is for you to go from nothing to your first passing test in under 5 minutes.

### Writing Tests

Once you've gone through the pain of setup, you have to actually drive the browser and automate its actions.

#### Management

After tests are written, they are continuously run in CI (Continuous Integration). That means when they fail, you need to understand why as quickly as possible. Due to the architecture problems of the way that Selenium Webdriver works, your tests will likely be flaky and fail for no good reason. In addition to that, it will be difficult to even see or understand what caused the failure.

- Cypress Service
- Recording Videos
- Screenshots
- Logging (which we'll get to later)

## History

# Architecture

## Differences

## Debuggability

## Error Handling

## Flakiness

## Javascript Events

# Frequently Asked Questions

## When will Cypress be publicly available?

As of writing this (Dec, 2016) Cypress has been in active development for over 2.5 years.
