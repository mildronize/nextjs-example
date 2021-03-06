fix bug for next-js example following [https://github.com/zeit/next.js/issues/4863](https://github.com/zeit/next.js/issues/4863)

[![Deploy to now](https://deploy.now.sh/static/button.svg)](https://deploy.now.sh/?repo=https://github.com/zeit/next.js/tree/master/examples/with-loading)
# Example app with page loading indicator

## How to use

### Using `create-next-app`

Execute [`create-next-app`](https://github.com/segmentio/create-next-app) with [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) or [npx](https://github.com/zkat/npx#readme) to bootstrap the example:

```bash
npx create-next-app --example with-loading with-loading-app
# or
yarn create next-app --example with-loading with-loading-app
```

### Download manually

Download the example:

```bash
curl https://codeload.github.com/zeit/next.js/tar.gz/canary | tar -xz --strip=2 next.js-canary/examples/with-loading
cd with-loading
```

Install it and run:

```bash
npm install
npm run dev
# or
yarn
yarn dev
```

Deploy it to the cloud with [now](https://zeit.co/now) ([download](https://zeit.co/download))

```bash
now
```

## The idea behind the example

Sometimes when switching between pages, Next.js needs to download pages(chunks) from the server before rendering the page. And it may also need to wait for the data. So while doing these tasks, browser might be non responsive.

We can simply fix this issue by showing a loading indicator. That's what this examples shows.

It features:

* An app with two pages which uses a common [Header](./components/Header.js) component for navigation links.
* Using `next/router` to identify different router events
* Uses [nprogress](https://github.com/rstacruz/nprogress) as the loading indicator.
