Form management
===============
There are two different ways to build forms on the IPBES website. Entity forms and Webforms. 

Webforms
--------

Useful for performing surveys. It is well established and has a number of modules that integrate with it such as multiple file upload. It inherits node functionality like scheduled publishing, cloning, access control and conditional fields. It also offers a page where you can get a quick overview of results and options for downloading submissions. It also has an inbuilt notification system. The disadvantage of using webforms is that you cannot use existing fields as entities and rendering forms using views is more difficult (not impossible).

Webforms can be accessed under the Content tab in the administration menu: /admin/content/webform

Entity forms
------------

Entityforms can make a wide variety of forms with lots of different fields available. Entityforms uses the entity API which guarantees it will work with Views, Rules, Entity Reference, Organic Groups and all Drupal fields. This makes it possible to look up existing content and vocabularies and render forms differently. Entity form also offers functionality like conditional fields and field groupings.

Entityforms can be accessed under the Structure tab in the administration menu: admin/structure/entityform_types

