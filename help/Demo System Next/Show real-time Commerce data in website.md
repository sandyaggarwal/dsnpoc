---
title: Show real-time Commerce data in website
slug: 5bWn-show-real-time-commerce-data-in-website
createdAt: Wed Dec 13 2023 13:20:03 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Dec 13 2023 13:30:05 GMT+0000 (Coordinated Universal Time)
---

If your DSN website has a working integration with Adobe Commerce/Magento, and uses products imported from there, you can display some of the product properties by loading them directly from Commerce instance.

## Pre-requisites

- Correct Commerce integration in project
- Products imported from this Commerce instance (SKU must match both products in project and in Commerce catalog)
- Product screen for a product from Commerce.

## Set up real-time product fetching

- 1. Edit your project and switch to **Screens** tab
  2. Find a screen for a Commerce-imported product
  3. Edit screen content
- ![](../../assets/1R8ptpHr0XI69qpKLkNrM_image.png)

* 4\. Select a property you want to make dynamic, eg. Product Name and enable  **Fetch from server** switch. Some properties like Category cannot be used like that due to technical reasons, however most of them can.
* ![](../../assets/hwi_USO8ZobULcmA3I-Rz_image.png)

5\. Now, every time you open this screen, product name will be read directly from Commerce instance, instead of the previously imported value.

6\. To check that, change product name in Commerce, save, and then reload the product page. After a brief loading indicator, a new name should be displayed

**Note**: In case of problems with receiving product data, the dynamic property will fall back to the imported value, and if this is missing as well, it will try to use 'Default value' provided directly in the component sidebar. You can also use product properties in dynamic variables in texts and titles. More about it here [FAQ](<../Demo System Next/FAQ.md>).
