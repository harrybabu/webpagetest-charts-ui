#Webpagetest Charts UI
This is a chart UI built on top of [webpagetest-charts-api](https://github.com/trulia/webpagetest-charts-api) and all the data and chart types that
it exposes. Goal is to make it easy to quickly analyze WPT results.  Display charts to see trends
and some local data, but always link off to the WPT page for full data. Don't wanna rebuild WPT.

## Installation

1. Get [webpagetest-charts-api](https://github.com/trulia/webpagetest-charts-api) up and running first.

1. clone this repo

1. `WPT_API="http://where-your-wpt-api-is-running:port" npm start`

1. Visit the app and port and you should see a list of available tests.

If things get weird You can get into debug mode with:

`DEBUG=wpt-ui* npm start` and it'll talk to you some.

Once everything is working well wrap it up in [forever](https://www.npmjs.com/package/forever) or [pm2](https://www.npmjs.com/package/pm2) or whatever you want to keep it up and running.

## What's it look like?

### Main Page
lists the available tests suites the app is currently running.  Imagine a nice list on a webpage :-)

### Suite Page
Shows charts for all of the tests in the suites.  Chart datapoints are
clickable, so that you can see exactly what's going on. This example only has one chart, but
more would populate here if the suite had more tests. This UI is better served by smaller
suites.

![suite](http://static.trulia-cdn.com/images/webpagetest-charts/webpagetest-charts-ui.png)

### Datapoint Page
A summary of the WPT results for that datapoint.  You can page through these
results, or click through to the full WPT test page to get even more data.

![datapoint](http://static.trulia-cdn.com/images/webpagetest-charts/webpagetest-charts-ui-datapoint.png)

## TODO
1. chage the UI to better display a suite that has lots of tests