# Hotel_Business_Understand_Improve_Revenue
Power BI project focused on hotel business analysis using star schema modeling, data transformation, and revenue insights.

# **Hotel Booking & Revenue Analysis Dashboard**

## **Project Overview**

This Power BI dashboard provides a comprehensive analysis of hotel operations, including bookings, revenue, profit, and guest trends. The dashboard is designed using a **star schema** structure, enabling efficient reporting and easy scalability for future data.

---

## **Data Description**

The dataset contains hotel booking records with the following key columns:

* **CheckIn / CheckOut Dates** – for calculating booking duration and stay type
* **Guest Type & Guest Country** – to analyze customer segments
* **Room Category / Stay Type** – for room-level analysis
* **Revenue & Cost Columns** – Total Revenue, Fixed Cost, Variable Cost, Total Cost, Profit
* **Time Attributes** – Month, Weekday, Season, Holiday

## **Data Transformation Steps**

1. Converted revenue and cost columns to **decimal numbers**
2. Converted bookings and cancellations to **whole numbers**
3. Created **calculated columns**:

   * **Booking Duration** = CheckOut – CheckIn
   * **Stay Type** = Short / Medium / Long based on duration
   * **Room Category** = based on ADR ranges
4. Added **foreign keys** for star schema:

   * **DateKey** (Fact_Booking → DimDate)
   * **RoomKey** (Fact_Booking → DimRoom)
   * **CustomerKey** (Fact_Booking → DimCustomer)
   * **HotelKey** (Fact_Booking → DimHotelBranches)

---

## **Star Schema**

* **Fact Table:** `Fact_Booking`

  * Measures: Revenue, Profit, Total Cost, Bookings, Cancellations
  * Keys: DateKey, RoomKey, CustomerKey, HotelKey
* **Dimension Tables:**

  * **DimDate:** Date, Month, Weekday, Season, Holiday, DateKey
  * **DimRoom:** Room Category, Stay Type, RoomKey
  * **DimCustomer:** Guest Type, Guest Country, CustomerKey
  * **DimHotelBranches:** HotelKey, Hotel Name

---

## **Report View / Visualizations**

The dashboard includes **key visualizations**:

1. **Cards:**

   * Total Revenue
   * Total Profit
   * Total Bookings

2. **Charts:**

   * Monthly Profit Trend (Column Chart)
   * Profit by Day of Week (Column/Line Chart)
   * Number of Bookings by Room Category (Bar Chart)
   * Revenue by Stay Type (Column/Stacked Chart)
   * Bookings by Guest Type (Pie Chart)

3. **Tables:**

   * Hotel Performance Summary: Sum of Bookings, Revenue, Profit

> All visuals include meaningful titles and aligned layout for clarity. Slicers are used for Month, Room Category, and Guest Type to filter data interactively.

---

## **Key Insights**

* The **monthly revenue and profit trend** helps identify peak seasons.
* **Room Category and Stay Type analysis** highlights the most profitable rooms and booking patterns.
* **Guest Type analysis** shows customer distribution and preference.
* The **hotel summary table** consolidates bookings, revenue, and profit for easy reporting.

---

## **Conclusion**

This dashboard provides a **complete view of hotel operations** using a clean star schema design, making it **easy to analyze key metrics and trends**. It is fully scalable for additional hotels or extended datasets in the future.


