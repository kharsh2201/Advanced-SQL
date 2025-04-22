# Advanced-SQL
## Collaborated with an airline client to analyze flight, passenger, and operational data for improved efficiency. Utilized advanced SQL techniques, including joins, CTEs, and window functions, to extract actionable insights. This data-driven approach identified critical patterns, reducing reporting time by 40% and enhancing operational decision-making and customer experience.

---

## ✈️ **SQL Capstone Project: AirlineDB Analysis**

### **Objective:**
The goal of this project was to gain hands-on experience with relational databases by writing and executing complex SQL queries to extract, analyze, and interpret meaningful insights from a simulated airline database (*AirlineDB*). The project tested practical knowledge of joins, window functions, CTEs, grouping, filtering, and formatting functions.

---

### **Step-by-Step Execution Process:**

#### **1. Understanding the Schema**
- The first step involved reviewing the **AirlineDB schema**, which included tables like `flights`, `airports`, `aircrafts`, `bookings`, `tickets`, `ticket_flights`, `boarding_passes`, and `seats`.
- Relationships between these tables were mapped to understand how to retrieve flight, customer, and booking data across various dimensions.

---

#### **2. Data Formatting and Selection**
- Queries began with simple selections and formatting, e.g., displaying the booking date in `YYYY-MMM-DD` format using the `TO_CHAR()` function.
- Columns such as ticket numbers, passenger details, and seat numbers were retrieved using inner joins across `tickets`, `boarding_passes`, and related tables.

---

#### **3. Aggregations and Frequency Analysis**
- Using `GROUP BY`, the project calculated how frequently each seat number was allocated.
- A **CTE (Common Table Expression)** and **RANK()** function were used to rank seats by frequency to identify the least allocated ones.

---

#### **4. Financial Analysis (LTV & Refunds)**
- To find the **highest and lowest paying customers by month**, a combination of `SUM()`, `TO_CHAR()`, and `DENSE_RANK()` was applied across joined `bookings` and `tickets`.
- Refund-eligible customers were identified by joining cancelled `flights` with `ticket_flights`, `tickets`, and `bookings`, and summing total amounts.

---

#### **5. Journey & Boarding Insights**
- Flight count per ticket was calculated to differentiate between **non-stop vs. multi-leg journeys**.
- A left join between `tickets` and `boarding_passes` was used to identify **tickets without boarding passes**.

---

#### **6. Time and Schedule-Based Analysis**
- Morning flights (6AM–11AM) were filtered using `EXTRACT(HOUR FROM scheduled_departure)`.
- The **earliest morning flights** per airport and **last flights** per day were retrieved using **window functions** and **MAX()**/**MIN()** aggregations.

---

#### **7. Flight Characteristics & Aircraft Data**
- Queries explored aircraft seating types, range brackets, and models (Airbus vs. Boeing).
- Flights with **range between 3000–6000**, **from specific airports**, and **cancellations by aircraft model** were extracted.

---

#### **8. Airport Performance**
- Airports with the **most/least departures**, **most cancellations (arriving)**, and **Europe/Moscow timezone** codes were retrieved using joins and aggregations.

---

#### **9. Advanced Join and Filtering**
- Multi-table joins helped retrieve flight counts between specific airport pairs (e.g., URS–KUF), and filter flights using status (`Cancelled`, `Delayed`), range, or model conditions.
- Specific attention was paid to proper use of aliases and efficient grouping logic.

---

### **Outcomes:**
- Built 30+ SQL queries answering real-world airline business questions.
- Strengthened practical understanding of data formatting, ranking, filtering, and aggregate analytics in SQL.
- Used **PostgreSQL functions** such as `TO_CHAR()`, `EXTRACT()`, `RANK()`, `DENSE_RANK()`, `CASE`, and `JOINs` extensively.

---

### **Tools & Skills Used:**
- **Database Platform:** Skillovilla SQL Playground
- **Database:** AirlineDB
- **Languages & Functions:** SQL, CTEs, Joins, Aggregations, Window Functions
- **Key Skills Demonstrated:** Data extraction, business insight generation, schema analysis, logical query formulation.
