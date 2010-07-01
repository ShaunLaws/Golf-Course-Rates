##Summary

The "golf_course_rates" module is based on the "rates" module (muchos gracias for your excellent work, Paul Huntsberger) and creates a CCK widget named "Golf Course Rates Field" that allows you to make a compound CCK field for use in your content types. This Compound Field Contains the following fields:

Date Range (text field)
Rate (text field)

NOTE: None of these fields can be deleted or ignored by the Form API. However, you can use form_alter to turn them into hidden fields, please do not unset() them.

You can then use this CCK field in your regular display, or use views to create any type of output you wish using the views theme system.

You can also use the golf_course_rate_display.tpl.php to add in any necessary extra information, or use a _preprocess hook to change variables, add custom logic, etc.

This module was built with the intention to be a starting point for developers to have a more intuitive interface that normalizes to CCK standards, which is probably what you are using on your content types anyways.

RECOMMENDED: It is also Recommended that you use the Vertical Tabs Module, as this allows you to have a cleaner interface when viewing these complex and sometimes numerous entries in one field. My advice is to create a Field Group Named "Golf Course Rates" and keep your golf_course_rates field in there.

##Notes on Compatibility
This module has been tested with the latest release of Drupal, which is 6.17 and the latest version of the Content Module (CCK) 6.26. I can confirm this works on Drupal Core 6.14 and later, but please use the latest version of CCK so you don't run into trouble. I don't see why this wouldn't work with earlier versions of Drupal Core and CCK. No support is currently offered for this module.

NOTE: This will NEVER be legacy ported to Drupal 5, I am truly sorry, but I don't want to maintain two separate versions of Drupal that are becoming out of date. Currently, I am unable to pledge that I will start a Drupal 7 branch.

##Dependencies

Content Module
Jquery 1.2.6

##Limitations

This module does not automatically format a rate table, you must handle that portion yourself, and create the table however you wish, preferably with theme('table' … )

##Road Map (To Do's)

1. Add in a _table formatter that automatically handles a Rate Table Output so you don't have to mess about with Views themeing to get the desired result.

2. Add in better views support? Not quite sure what else I can do… any suggestions are welcomed!

3. Add in a way to hide unwanted fields.