---
title: Products & Cart
slug: GhYH-pr
createdAt: Tue Oct 24 2023 10:45:42 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Oct 24 2023 11:13:25 GMT+0000 (Coordinated Universal Time)
---

:::hint{type="info"}
Note: With latest Adobe Commerce Integration it is possible to import products from Adobe Commerce instance and use them in Cart/Checkout process, with data and events being sent to both AEP and Adobe Commerce.
By default, however, products and checkout flow only send data to AEP.
:::

### Products

You can use Products tab to define products and their properties, both built-in, like name, image, description, and custom.

Defined products can then be linked to a designated page. This is done by selecting the product page in Screens tab and checking **Is product screen **switch and selecting product in a dropdown. Linking product to a screen has a range of benefits:

- screen will populate dataLayer.product object with linked product's properties
- all product-related components on this screen will use the linked product by default, so you don't have to link each component manually
- you can use product properties in dynamic texts on this screen (eg. in Text component) by using **${product.property} **notation,&#x20;
  eg. 'This item costs ${product.price} USD'.

If you want to display other product's details on another product's screen, you can override the component's **Product **property by setting it manually.

### Adding to Cart

In order to allow adding product to cart, simply put a **Cart & Checkout > Add to cart button** to product page, selecting a product in its properties if needed.

### Cart

In modular web projects you can build your own cart screen. Open your project in Experience Builder and switch to Navigation tab. There, in the third column labeled "Cart":

- toggle **Enable cart **switch on to show cart button in website's main navigation&#x20;
- use **Cart screen **dropdown to select which screen will be opened when user clicks the cart button

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FpJacGB0iSaPNKMhtkvWV%2Fimage.png?alt=media\&token=9b95f312-35fd-4550-8fe3-6edbda82e3d6)

Now, open the chosen cart page in Screens tab and edit its components. You can use all components, particularly the ones from the Cart & Checkout category:

- **Cart Content **- displays a table with a list of items added to cart
- **Cart Price Summary **- displays a table-like cost summary. Includes shipping and discounts if such were applied
- **Button **-** **component to navigate to checkout or order confirmation page

### Checkout & Order Confirmation

You can spread the checkout process across as many screens as you wish, gathering information and completing the order. Additional components you can use are:

- Standard form components to provide Billing Address
- **Shipping Method **- allows to select from user-defined shipping methods to set the delivery method and cost
- **Discount **- allows to insert user-defined promo codes to apply discount (value or percent). Codes can be literal values, include \* wildcard sign or be a Regular Expression
- **Order Summary** - displays a sectioned summary of billing address, shipping, discount, etc.
- **Confirm Order Button **- important component that sends additional metadata and generates the order confirmation number (for AEP and to display on a thank-you page)

Pay extra attention to using **Confirm Order Button **at the end of your checkout flow. It will generate order confirmation number, as well as clean up the persisted cart, shipping and discount data stored locally (only some dataLayer properties remain). Order confirmation number is saved in **dataLayer.commerce.order.purchaseOrderNumber, **and you can reference it on a post-confirmation/thank-you page, eg. in Text component with dynamic selector: **${commerce.order.purchaseOrderNumber} **

