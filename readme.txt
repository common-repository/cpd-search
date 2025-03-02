=== CPD Search ===
Contributors: rossigee
Tags: commercial, property, database, search, office, shop, restaurant, retail, industrial, warehouse
Requires at least: 3.6
Tested up to: 4.7.5
Stable tag: 3.3.9

Thin layer to provide custom themes and plugins with access to CPD's commercial property database.

== Description ==

Acts as a thin layer between your UK commercial property estate agent's WordPress theme, and CPD's powerful commercial property search engine, with comprehensive details of the latest properties across the UK. In effect, this plugin allows your developers to add an extensive UK commercial property search facility to your website. Designed as a simple set of PHP classes, and an AJAX/JSON handler to help your page handlers capture and process your visitor's search criteria, results, contact details and their clipboard. The end goal is that an e-mail is sent to you and your visitor, containing the short-list of properties they are interested in.

== Installation ==

You need to develop or customise your WordPress theme with custom 'page-*.php' pages that handle the functionality required in your particular use case, but having those pages make calls to the CPD REST API, via the utility functions provided by this plugin.

In short, you need to create at least one custom page each for your property search form, search results, details view, and clipboard results view. More detailed documentation is forthcoming, along with a demonstration theme that you can download and play with to see how it works, and use in whole or part to augment similar functionality in your own theme.

Be sure to put a valid CPD application token into the 'CPD Search' configuration page found in the WordPress admin area, until 'Settings -> 'CPD Search'.

Support available by e-mail <support at cpd.co.uk>

== Changelog ==

= 3.3.9 =
* Add installation and user guide documentation.
* Stop sending 'X-CPD-Context' headers, which are no longer necessary.

= 3.3.8 =
* Return 'false' instead of exception on resetting password of unknown e-mail address.

= 3.3.7 =
* Add distinct 'sizeDescriptionSqFt' method for presenting size in sqft.

= 3.3.6 =
* Fix 401 response when unregistered visitor registers interest using AJAX method.

= 3.3.4 =
* Fix for handling of 403 errors when using test tokens.

= 3.3.3 =
* Bump version to indicate compatibility with WordPress 4.2.

= 3.3.2 =
* Fix return values from clipboard functions, and session corruption bug.

= 3.3.1 =
* Switch 'remove_from_clipboard' parameter back to propertyid. Update URIs for clipboard API calls.

= 3.3.0 =
* Update to 'add_to_clipboard' and 'remove_from_clipboard' calls to reflect more RESTful backend API usage.

= 3.2.3 =
* Update methods that generate media URLs to use URLs now provided in server response (since REST 1.0.6).

= 3.2.2 =
* Update URLs for live/sandbox environments in settings.

= 3.2.1 =
* Fix for 'verify_user' method setting wrong user token, causing 401 on subsequent search.

= 3.2.0 =
* Add a 'visitor_logout' method.

= 3.1.5 =
* Fix for JS ajaxurl where WP admin is set to enfore SSL admin logins.

= 3.1.4 =
* Fix for handling of exception responses from 'registerinterest' method calls.

= 3.1.3 =
* Fix for identification of 'agent not subscribed to visitors service' exception.
* Stop sending redundant 'agent_ref' parameter in register user requests.

= 3.1.2 =
* Only show 'live' sectors for agent's sectors pulldown.

= 3.1.1 =
* Fix for display of 'sectors' field/column.

= 3.1.0 =
* Allow for updated responses with multiple sectors per property.

= 3.0.12 =
* Fix for 'create_clipboard' bug causing error for users verifying their address.

= 3.0.11 =
* Add 'fetch_agent_sectors' methods.

= 3.0.10 =
* Add missing 'verify_user' and 'change_password' PHP methods.
* Add 'tenureDescription' method.

= 3.0.9 =
* Fix for broken 'removeFromShortlist' method.
* Fix for broken 'is_user_registered' method.
* Add utility 'getCookie' and 'setCookie' methods to CPD JS.
* Add 'areaDescription' PHP function.
* Add missing 'login_visitor' and 'reset_password' PHP methods.

= 3.0.8 =
* Drop stray empty lines from PHP files, causing 'header output already started' warning.

= 3.0.7 =
* Add functions to add/remove properties from SESSION-based shortlist.

= 3.0.6 =
* Recognise 405 status when agents 'visitor' flag is not set, raise exception.

= 3.0.5 =
* Update 'cpd_search_service_context' to a static class method.

= 3.0.4 =
* Typofix.

= 3.0.3 =
* Rename plugin from 'cpd-search-lite' to 'cpd-search'.

= 3.0.2 =
* Replace 'CPDAjax' global JS with 'CPDSearchConfig'.

= 3.0.1 =
* Various bugfixes from in-house testing.

= 3.0.0 =
* Switch functions wrapped from older SOAP API to use our newer REST API.

= 2.0.2 =
* Drop blank line at end of file causing session header problems.

= 2.0.1 =
* Initial version. Re-write, avoiding lessons learned developing/deploying v1.
