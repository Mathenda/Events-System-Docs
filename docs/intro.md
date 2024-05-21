---
sidebar_position: 1
---

# [Not so] Quick start guide

Let's get you **up and running!**.

## Getting Started

To get started, go to our **[Official github](https://github.com/COS301-SE-2024/Events-System)**.

Or clone our repo using the **[github desktop app](https://desktop.github.com)**.

Create your clone using the following link:
```bash
  https://github.com/COS301-SE-2024/Events-System.git
```


Or using the **Github CLI**:
```bash
gh repo clone COS301-SE-2024/Events-System.
```

### What you'll need
:::tip[package manager]

For this project, we will be using npm, it comes with the installation of Node

:::
- [Node.js](https://nodejs.org/en/download/) version 20.0 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.
- [npm](https://www.npmjs.com/get-npm) (which comes with Node.s).
- [Nx CLI](https://nx.dev/latest/angular/getting-started/intro) globally using the command `npm install -g nx`.
- [Java JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) version 21 or above for the Spring backend.

## What's next?

With the repository cloned locally, let's install our dependencies!

1. Navigate to the root of the project directory.
  > ```bash
  > cd Events-System
  > ```
2. install npm dependencies.
  >```bash
  >npm install
  >```
3. install `@nrwl/angular` as a dev dependency.
  > ```bash
  > npm install --save-dev @nrwl/angular
  > ```
4. install `nx@latest` globally.
  > ```bash
  > npm install --global nx@latest
  > ```
5. Serve the Site locally.
  > ```bash
  > nx serve
  > ```
:::danger[Troubleshooting]

if you run into an error similar to: The current directory isn't part of an Nx workspace.

please run the following command:
```bash
  cd Events-System
```
:::
:::danger[Troubleshooting]
if you run into an error similar to: command nx unrecognized

please make sure npm is set in your PATH environment variable.
:::
:::danger[Troubleshooting]
if you run into an error similar to:  cannot be loaded because running scripts is disabled on this system

please make sure to run powershell as administrator and run:
```bash
  Set-ExecutionPolicy -ExecutionPolicy Unrestricted
```
:::
:::tip[ON success]

NX will serve the site to [localhost](http://localhost:4200) and you can view the site in your browser.

:::

