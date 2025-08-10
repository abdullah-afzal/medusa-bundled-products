<h1 align="center">
  📦 medusa-bundled-products
</h1>

<p align="center">
  A Medusa plugin that adds <b>bundled product</b> functionality, allowing you to create and manage product bundles that combine multiple products into a single offering. Perfect for <i>kits</i>, <i>starter packs</i>, and <i>promotional combos</i>, base on medusa example for bundles.
</p>

---

## ✨ Features

* Create bundled products with linked products
* Set custom pricing for bundles
* Integrates seamlessly with Medusa’s core product and variant models
* Supports cart and order handling for bundles
* Easily extendable for storefront display

---

## 🔄 Compatibility

* **Medusa version**: `@medusajs/medusa` **>= 2.4.0**

---

## 📦 Installation

1. **Install the plugin**:

   ```bash
   npm install medusa-bundled-products
   # or
   yarn add medusa-bundled-products
   ```

2. **Add it to your `medusa-config.js`**:

   ```js
   module.exports = defineConfig({
     // ...
     plugins: [
       {
         resolve: "medusa-bundled-products",
         options: {
           // Optional configuration
         },
       },
     ],
   });
   ```
3. **Run Migrations**:
   ```js
    npx medusa db:migrate
   ```

---

## 🚀 API Endpoints

### **Admin Endpoints**

* `POST /admin/bundled-products` → Create a bundled product
* `GET /admin/bundled-products` → List all bundled products

### **Storefront Endpoints**

* `GET /store/bundled-products/:id` → Get a specific bundled product
* `POST /store/cart/:id/line-item-bundles` → Add a bundle to a cart
* `DELETE /store/cart/:id/line-item-bundles/:bundle_id` → Remove a bundle from a cart

---

## 🛒 Cart Behavior

This plugin ensures bundles are treated as a **single unit** in the cart:

* Adding/removing updates all associated items together
* Pricing and inventory are handled accurately for all bundle components

---

## 💡 Proposals, Bugs, Improvements

If you have ideas, feature requests, or bug reports, please [open an issue](https://github.com/abdullah-afzal/medusa-bundled-products/issues).

---

## 💼 Pro Version

A **Pro version** is available under a commercial license — [contact me](https://github.com/abdullah-afzal) for details.

---

## 📜 License

© 2024 [abdullah-afzal](https://github.com/abdullah-afzal) — All rights reserved.

---
