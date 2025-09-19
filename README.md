
# Eulerian Marketing Platform for Google Tag Manager (GTM) Client-Side

## Description

This Google Tag Manager Community template is available for the Eulerian Marketing Platform provided by Eulerian Technologies SAS (https://eulerian.com)

The **dataLayer** used is the one described in the official documentation of the [Google Tag Manager Solution](https://developers.google.com/tag-platform/tag-manager/datalayer)

For server-side integration please check the appropriate [GTM Server-Side plugin](https://github.com/EulerianTechnologies/gtm-ss-eulerian-analytics)


### Documentation

If you don't already have an account, you can try our freemium platform through [Eulerian.IO](https://www.eulerian.io) to create a free account & declare your website, this allow you to have access to the trackingDomain.

1. go to you google tagmanager instance
2. go to the "Templates" section
3. look for the Eulerian Marketing Platform - GTM template in the gallery
4. create new template
5. the template is imported you just need to configure with the proper subdomain from the third-party tracking url

   5.1 example : if you tracking domain is : `https://et1.eulerian.net` the **trackingDomain** is **et1.eulerian.net**
   
   5.2 example : if you tracking domain is : `https://io1.eulerian.net` the **trackingDomain** is **io1.eulerian.net**

   5.3 example : if you tracking domain is : `https://sdf475.eulerian.io` the **trackingDomain** is **sdf475.eulerian.io**

6. save the template
7. trigger the template with custom page_view / remove_from_cart / add_to_cart / view_item / purchase / generate_lead.
8. publish the modifications -> you are now **live** !

### Which events are mapped

#### global mapping

The following global parameters are always provided to each call sent to us as long as they exists in the original datalayer :
- **currency** mapped to **currency**
- **user_id** mapped to **uid**

For each call we auto-copy all additionnal parameters of the event prefixed by **gtm-** for non-standard keys.

#### page_view

Standard call done

#### purchase

A transaction is registered in this case :
- **transaction_id** mapped to **ref**
- **value** mapped to **amount**
- **items** mapped to product array & product params are prefixed by **ga-**
  
#### add_to_cart

Products listed in the **items** array are added to the current cart.

#### remove_from_cart

Products listed in the **items** array are removed from the current cart.

#### view_item

Product page is viewed and the first result of the items array is sent to Eulerian.

#### generate_lead

A lead is registered in this case :
- **transaction_id** mapped to **ref**, if not available a random ref is created
- **value** mapped to **amount**
- **items** mapped to product array & product params are prefixed by **ga-**

#### custom events

Custom events not listed above are directly sent to actions/goals for further processing in the platform.

### MULTI-EVENTS

As GTM can trigger multiple events and hence our tag it can result in multiple calls on our end that can inflate the stats.

To avoid this make sure :
- you only trigger the Eulerian GTM SS only for the event you want to track
- avoid multi-event call on a single page : page_view -> view_item -> user_engagement for example only trigger on view_item if exists for example.


### SUPPORT

We provide limited support through our free offering, if your setup is more complex we can provide consulting expertise and/or work with your expert agencies of your choice.
This means that the current plugin works for most cases but not all cases, so please understand your own setup and make sure it makes sense regarding what we are collecting so that you can take the most of our platform. Enjoy !

## License

Apache 2.0
