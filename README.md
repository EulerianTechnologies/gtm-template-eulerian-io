

# Eulerian IO Tracking

## Description

This Google Tag Manager Community template is available for the Eulerian.IO attribution service provided by Eulerian Technologies SAS (https://eulerian.com)

## Getting Started

* Register for free at https://eulerian.io
* Create a new subdomain on your DNS Provider following our instructions (recommended)
* The Eulerian IO tag template allow you to install up to 3 different tags:

### Page view
This call is trigered during web page loading or following specific actions. Use this tag to measure metrics associated to visitor's navigation on your website like : number of visits, bounce rate, time spent on site...

You might want to exclude pages which should not be tracked when using the All Pages trigger (product pages and transaction confirmation page).

### Product page View
Flags to Eulerian that a product has been seen.

You can exclude the page view tag triggering on your product pages in order to avoid counting twice page views.

### Transaction
Use this tag to collect and measure transactions happening on your website. This tag has to be triggered from the confirmation page.

You can exclude the page view tag triggering on your confirmation page in order to avoid counting twice page views.

## Documentation

### Eulerian Tracking Domain
Copy-paste your custom subdomain (e.g. 12345.mydomain.com) if you are installing Eulerian IO directly on your web domain.
If not, select your datacenter region (North America or Europe) to automatically connect to the correct Eulerian Server Domain.

### Page Paths and Page Names
You can set this to a specific string, but it is recommended to either use URL path or custom pagenames when tracking across multiple pages. Set the page path rewriting if you need to clean your website's url structure.

### Transaction ID
Use your own transaction ID system on Eulerian when flagging a new order. Be sure that this value is unique otherwise Eulerian won't count it.
By default, the platform is automatically generating a new transaction ID.

### Transaction Amount
Measure and attribute your transactions' generated revenue. 
By default, each transaction has fixed value amount of 1.

### Transaction Amount Currency
Set this option to automatically convert transactions happening in different currencies to your Eulerian.io's main currency. Specify the currency code you need to use (either a specific string or a custom variable)