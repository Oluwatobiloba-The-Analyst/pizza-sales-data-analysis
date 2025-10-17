# 🍕 Pizza Sales Data Analysis

## 📄 Project Overview

This project explores pizza sales data using **SQL**, **DAX**, and **Power BI** to uncover key business insights, performance metrics, revenue generation, customer behavior, and sales trends.  

By transforming raw transactional data into interactive visualizations, the dashboard visualizes core KPIs, top and under-performing products, seasonal trends, and customer behavior across categories and sizes.  
The dashboard provides valuable insights that support business decisions related to marketing, product development, and operations — enabling **data-driven decisions** through interactive charts and summaries.

---

## 🎯 Objectives

- Analyze total sales performance and revenue generation  
- Identify top-performing and under-performing pizza products for potential marketing or product review  
- Identify top-performing pizza sizes and categories  
- Explore time-based trends (monthly, daily) to inform marketing strategy  
- Understand customer behavior via average order value and quantity  
- Provide actionable business recommendations to increase revenue and operational efficiency  

---

## 🧰 Tools & Technologies

- **Power BI Desktop** – Data visualization and report building/dashboard creation  
- **DAX (Data Analysis Expressions)** – Calculated measures for KPIs  
- **Power Query** – Data cleaning and transformation  
- **SQL** – Data sorting and filtering  
- **Maven Data Playground** – Main dataset source  

---

## 📁 Dataset Overview

The dataset consists of four interrelated tables simulating a real-world pizza sales environment. Each contains essential attributes used for analysis and dashboard modeling:

### 🔸 `orders.csv`
Contains general information about each order.
- `order_id`: Unique identifier for each order  
- `date`: Date of the order  
- `time`: Time of the order  

### 🔸 `order_details.csv`
Contains line-item breakdown for each order.
- `order_details_id`: Unique identifier for each row  
- `order_id`: Foreign key linking to `orders`  
- `pizza_id`: Foreign key linking to `pizzas`  
- `quantity`: Number of units ordered  

### 🔸 `pizzas.csv`
Provides detailed information about individual pizza products.
- `pizza_id`: Unique pizza identifier  
- `pizza_type_id`: Links to `pizza_types`  
- `size`: Size of the pizza (S, M, L, XL, XXL)  
- `price`: Price per unit  

### 🔸 `pizza_types.csv`
Contains metadata about pizza types.
- `pizza_type_id`: Unique ID for each pizza variety  
- `name`: Name of the pizza  
- `category`: Category (Classic, Supreme, Chicken, Veggie, etc.)  
- `ingredients`: List of ingredients  

### 🧩 Table Relationships
`orders` ← `order_details` → `pizzas` → `pizza_types`

This relational structure allowed for robust sales, category, and performance analysis across multiple dimensions (product, time, size, category).

> 🔗 **Dataset Source:** [Maven Data Playground – Pizza Place Sales](https://mavenanalytics.io/data-playground/pizza-place-sales)

---

## 📊 Exploratory Data Analysis

### 🔢 KPIs Calculated
- **Total Revenue:** 817,860  
- **Total Orders:** 21,350  
- **Total Quantity Sold:** 49,570 pizzas  
- **Average Order Value (AOV):** 38.31  
- **Average Pizzas per Order:** 2.32  

### 📊 Sales Breakdown

- **Revenue by Pizza Size:**  
  Large (L) pizzas generated the highest revenue at **$375.32K**, followed by Medium (M) **$249.38K**, Small (S) **$178.08K**, XL **$14.08K**, and XXL **$1.01K**.  

- **Revenue by Pizza Category:**  
 Classic appears as the best selling category with $220.05K (26.91%)**, followed by Supreme **$208.20K (25.46%)**, Chicken **$195.92K (23.96%)**, and Veggie **$193.69K (23.68%)**.  

- **Total Quantity Sold by Pizza Category:**  
  Classic (14,888 units), Supreme (11,987 units), Veggie (11,649 units), Chicken (11,050 units).  

- **Top 5 Best-Selling Pizzas by Quantity:**  
  1. The Classic Deluxe Pizza – 2,453  
  2. The Barbecue Chicken Pizza – 2,432  
  3. The Hawaiian Pizza – 2,422  
  4. The Pepperoni Pizza – 2,418  
  5. The Thai Chicken Pizza – 2,371  

- **5 Underperforming Pizzas by Quantity:**  
  1. The Soppressata Pizza – 961  
  2. The Spinach Supreme – 950  
  3. The Calabrese Pizza – 937  
  4. The Mediterranean Pizza – 934  
  5. The Brie Carre Pizza – 490  

- **Top-Selling Pizza Sizes by Quantity:**  
  Large (L) (18,956), Medium (M) (15,635), Small (S) (14,403)  

- **Least-Selling Pizza Sizes by Quantity:**  
  XL (552), XXL (28)  

- **Highest Sales Days:** Friday and Saturday  
- **Peak Revenue Months:** March, May, July, and November (each > $70K)  

---

## 🔍 Key Insights

### 1. Sales Volume & Revenue  
- Over **21,000 orders** placed, generating **$817,860** in total revenue.  
- A total of **49,570 pizzas** sold, averaging **2.32 pizzas per order**.  
- **Average order value:** $38.31 — indicating moderate upsell behavior.  

### 2. Size Preference  
- Large (L) pizzas generated the highest sales revenue ($375.32K) and demand (18,956 units). This may be due to customers' preference for the large size.  
- XXL and XL sizes underperformed, likely due to pricing or portion mismatch with customer preferences.  

### 3. Category Performance  
- **Classic pizzas** led in both revenue ($220.05K) and quantity sold (14,888 units). This could be because customers lean towards the familiar or because it taste better.
 
- Supreme, Chicken, and Veggie also performed well with evenly distributed sales.  

### 4. Product Performance  
- **Top 5 Best-Sellers:** The Classic Deluxe Pizza, The Barbecue Chicken Pizza, The Hawaiian Pizza, The Pepperoni Pizza, and The Thai Chicken Pizza each selling above 2.3K units.  
- **5 Underperformers:** The Brie Carre Pizza, The Mediterranean Pizza, The Calabrese Pizza, The Spinach Supreme Pizza, and The Soppressata Pizza (<1K units).  
  →This poor performance may be due to flavour mismatch, or weak marketing. These pizza products may require re-branding, improved marketing, or removal.

### 5. Time-Based Trends  
- **Fridays (8,242 units)** and **Saturdays (7,493 units)** recorded the highest sales, this could be due to weekend parties and people's free time to relax and enjoy themselves. This also suggests ideal days for targeted promos and marketing.  
- **Sunday** recorded the lowest sales (6,035 units).  
- **Revenue spikes** observed in **March, May, July, and November**, (each exceeding $70K), indicating potential seasonality, promotion-driven spikes, or campaign effect. 

 ---

## 💡 Business Recommendations

### 🔹 Optimize Inventory & Promotions
- Stock up on large sizes, medium sizes, and top-selling categories (classic) for high-demand days (Thursdays–Saturdays) to match demand patterns. 
- Bundle best-sellers with under-performers in promotion to move slow stock.  
- Promote high-performing pizzas during **Fridays and Saturdays** to maximize sales.  
- Review pricing and marketing strategies for **XL and XXL** sizes.  
- Offer bundle discounts to increase AOV (Average Order Value).


🔹 Product Strategy
- Gather and analyze customer feedback on low-performing pizzas to identify the problem and determine the next course of action
- Address Under-performers, consider improving, re-branding, discounting, or removing them to reduce menu complexity and inventory waste.



🔹 Boost Customer Spend
- Introduce value-based combos to increase average order value and items per order.

🔹 Leverage Time-Based Campaigns/Monitor Seasonality
- Reinforce marketing efforts during historically strong months like March, May, July, and November.
- Schedule promotions and marketing campaigns on Fridays and Saturdays to capitalize on customer traffic.
- Launch discounts on Fridays and Saturdays to maximize conversion.
- Leverage strong sales periods (March, May, July, November) for seasonal promotions or limited-time offers
- Analyze external events (holidays, campaigns) influencing seasonal sales spikes.

---

## 👤 Author

**Oluwatobiloba Taiwo**  
- [LinkedIn](https://www.linkedin.com/in/oluwatobiloba-taiwo-dvm-b43b51366?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app)  
- [Portfolio](#)  
- [Email](mailto:taiwooluwatobiloba2904@gmail.com)

---

## 📌 License

This project is for **educational and portfolio purposes only**.  

