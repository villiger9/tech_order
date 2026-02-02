# Tech Order ✅

**Tech Order** is an Odoo module to manage restaurant-style meal orders (internal and external), meals, ingredients, customer feedback, and basic automation for order lifecycle management.

---

## 🔧 Key Features

- Manage **Meals**, **Meal Categories**, and **Ingredients**
- Create **Orders** (Internal / External) with items and computed prices
- Order states: **Draft → Confirmed → In Process → Delivered → Cancelled** with actionable header buttons
- Add **External Items** (link to `product.product`) via a wizard for external orders
- Customer **Feedbacks** with an approval server-action
- Configurable **Max Table Number** via Settings
- Daily scheduled job marks orders as **Urgent** when due
- Demo data and an **Order Report** included
- Access control with user groups: **User**, **Manager**, **Internal Order**, **External Order** and domain rules

---

## 🧩 Requirements

- Odoo (recommended: **Odoo 15**, should work on Odoo 14+)
- Python dependencies: same as standard Odoo installation (no extra pip packages required)
- Depends on core modules: `base`, `product`

---

## 🚀 Installation

1. Copy the `tech_order` folder into your Odoo addons directory.
2. Restart the Odoo server.
3. Update the Apps list and install the **Tech Order** module.
4. (Optional) Install demo data by enabling demo mode or using the module's demo to see sample meals and orders.

---

## ⚙️ Configuration

- Go to **Settings → Tech Order** (only accessible for the Manager group) and set **Max Table Number**.
- User groups are defined in `security/security.xml` (assign users to `User`, `Manager`, `Internal Order`, `External Order` as needed).

---

## 🧭 Usage

- Create **Meal Categories** and **Meals** (set price and add ingredients).
- Create an **Order**, choose `type` (internal/external), add items and quantities.
- Use the header buttons on an Order to **Confirm**, **Start Processing**, **Mark as Delivered**, or **Cancel**.
- For external orders, use **Add External Item** to attach a `product.product`.
- Approve feedbacks using the server action `Approve` (available in Feedback form or via the action menu).

> Tip: The cron job `Set Urgent` runs daily to set `is_urgent` on orders near their expected date.

---

## 📄 Reporting

- The module includes `reports/order_report.xml` that can be used to print order summaries.

---

## 🧪 Tests & Demo

- Demo data is included in `demo/demo.xml` to help you get started quickly.
- No automated tests included (PRs welcome!).

---

## 🤝 Contributing

- Contributions, bug reports, and improvements are welcome. Please open a Pull Request or an issue with a clear description and steps to reproduce.

---

## ✉️ Author

- Tala — https://sy.linkedin.com/in/talah-hjaij

---

**Enjoy using Tech Order!** ✨
