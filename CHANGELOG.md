Changelog
=========

v1.1.7
------

* Do not require Live key in Test mode and vice versa
* Include cancel url, order reference & order URLs in payment data
* Don't show the eligibility message in case of API error
* Stop checking in vendor dependencies – they'll be included in each release's ZIP file


v1.1.6
------

* Dependencies update

v1.1.5
-------

* Fixes display on cart option that was always on
* Tested against latest versions of Wordpress/WooCommerce

v1.1.4
-------

* Fixes various warnings when WooCommerce isn't activated
* Updates dependencies
* Fixes errors when Alma's API is not available
* Attempt to fix problem triggered when calling the Wordpress API 

v1.1.3
-------

* Fixes warning when `excluded_products_list` is not set

v1.1.2
------

* Adds hidden option to be able to choose installments count to use for created payments

v1.1.1
------

* Fixes bug occurring in `wp-admin/nav-menus.php`

v1.1.0
------

* Fixes case of "alma" in includes path
* Adds possibility to exclude product categories from installment payments, to help enforce contractual restrictions 
  (i.e. Alma cannot be used to sell/buy virtual/downloadable products such as gift cards, subscriptions, ...)

v1.0.1
------
Let's start following semver.

* Switches logo file to SVG
* Uses latest Eligibility check behaviour to remove one extra call to the API
* Adds User-Agent string containing the module's version, WordPress version, WooCommerce, PHP client and PHP versions,
to all requests going to Alma's API.
* Adds support for Alma's IPN callback mechanism

v1.0.0
------
This version evolved for a while without any version bump 🤷‍♂️
Features in the latest push to this release:

* Module can be configured in Test and Live mode; Test mode only shows Alma's payment method to visitors who are also
administrators of the shop
* A message displays below the cart to indicate whether the purchase is eligible to monthly installments
* The module adds a payment method to the checkout, which redirects the user to Alma's payment page.
If everything goes right (i.e. Customer doesn't cancel, pays the right amount, ... ), the order is validated upon customer return.
