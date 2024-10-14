---
title: Import Commerce products to your project
slug: ox5k-import-commerce-products-to-your-project
createdAt: Wed Dec 13 2023 12:58:47 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Dec 13 2023 13:31:30 GMT+0000 (Coordinated Universal Time)
---

In order to show Adobe Commerce products in DSN website or mobile app, you need to import them to your project first. **Note**: imported products are a just a copy stored in your project and won't get synchronised with Commerce, unless you re-import them.&#x20;

However, if particular web page has Commerce product assigned, it is possible to [Show real-time Commerce data in website](<../Demo System Next/Show real-time Commerce data in website.md>). You can then use most of its properties via Product Property component or dynamic properties in texts and titles. See [FAQ](<../Demo System Next/FAQ.md>) for more details.

## Pre-requisite

Your project needs an active Commerce integration for this feature to work. See [Link Commerce instance with your project](<../Demo System Next/Link Commerce instance with your project.md>).

## Importing products

- 1. Edit your web Project
  2. Open **Products** tab.
  3. Click **Import from Commerce **button
  4. In the dialog, provide filters for product search. Usually search will be based on Categories and further narrowed down by name fragment or price range.&#x20;
- ![](../../assets/GIYYV6IrXxrlisXy8NL60_image.png)

* 5\. Once filters have been selected, click **Search** button and wait for a few seconds. The description should be updated with the number of products found. Tweak filters and search again until you reach a satisfying number.

  *Prefer smaller number of products. Large number of products will require more work later on and will negatively impact the website performance.*

  6\. Once finished with filters, click **Import** button to save products to your project. They will appear on the product list. Products imported from Adobe Commerce have a fixed set of properties, including a **commerceServer **one containing instance URL.
* ![](../../assets/cDQPnOrHFpVD3wPP-MwAT_image.png)

## Using imported products

Currently, in order to use a product, you need to either

- create a product screen
- and/or reference it manually in a component like Product Card (new product will appear on a product selection drop-down list)

**Note**: You can use one product screen to server as template. It does not have any product assigned, but will rather receive product data automatically, eg. via link from Product Card component. This way, you will be able to reuse one screen for multiple products, making it easier to manage changes and generally more scalable.

### Create product screen using a default template

- To create a product screen with pre-defined template, visit Products tab, select a product and click **Create Linked Screen** button next to product's name.

  If this product is used by a screen already, this button will say **Edit Linked Screen** instead, serving as a link. You can edit created screen to customise it to your needs with components.
- ![](../../assets/IK5FzYM49h5tkjSLS5KUg_image.png)

### Create product screen using existing screen

If you have a customised product screen already, you can use it as a kind of template:

- 1. Open **Screens** tab in your project
  2. Select an existing product screen
  3. On screen card, click the **Duplicate** action button
  4. Select duplicated screen
  5. Click **Edit** button in sidebar and rename it appropriately
  6. Select **Is fixed product screen** switch if not enabled
  7. Select a new product from a **Linked Product** drop-down
- ![](../../assets/-OHy53rIEzgqMBubVUP5j_image.png)



