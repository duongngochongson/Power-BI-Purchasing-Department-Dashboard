# Power BI Purchasing Department Dashboard
The project aims to visualize overall and in-depth information on the purchasing department for managers and business analysts.

## Table of Contents:
1. [Overall](#overall)
2. [Design Thinking](#dt)
3. [Visualization Process](#vis)
4. [How to Use Dashboard](#how)

<div id='overall'/>
  
## Overall

**Platform**: Microsoft Power BI for desktop.

**Main Techniques**: Design thinking, clean and transform data in Power Query, develop models, and employ DAX.

**Context**: AdventureWorks database supports standard online transaction processing scenarios for a fictitious bicycle manufacturer. The purchasing department will be responsible for purchasing goods, raw materials, and semi-finished products for production. Management expects that the ordered goods are sufficient for sales, on time, and at optimal import prices.

**Goal**: Based on the context, I will create dashboard for vendor performance, including 2 visuals: an overview and a detailed information. To achievie it, I apply design thinking to identify key metrics, then pull relevant data from Google BigQuery.
  
**Links to data dict:** https://dataedo.com/download/AdventureWorks.pdf

<div id='dt'/>

## Design Thinking

### Step 1 - Empathize

| 5W1H | |
| - | - |
| Who will be viewing this Dashboard?                                | Purchasing Manager, accountant |
| If we had to choose only one key Stakeholder, who would it be? | Purchasing Manager |
| What problem does this Dashboard solve?                            | It enhances vendor oversight, promotes data-driven decisions, and helps optimize vendor relationships and costs.|
| Describe the problem in one sentence                               | Provide the Purchasing Manager with necessary information about the overview situation, as well as the performance details of the vendor in particular. |
| When and where will Stakeholders view this Dashboard?        | The Dashboard can be viewed during monthly meetings or managers alone.|
| Why do stakeholders need this Dashboard?                   | Understand vendor overview performance and evaluate decisions|
| How stakeholders achievie their goals?           | Understand the situation to make decisions |


|Stakeholder Empathy | |
| -- | -- |
| Pains  | A large amount of info that need to be analyzed as well as identify important information |
| Thinking and feeling  | Worry about the effectiveness of the purchasing department in general. As well as have opinions about vendors |
| Seeing  | Dashboard of the company's purchasing department and each vendor's info for comparison and contrast |
| Saying and doing   | The dashboard system is quite intuitive to grasp the overview information to see the big picture. Also the vendor detail dashboard is full of information to see in depth|
| Gains | See the overview change and the details of how the vendors are operating to make the right choice|

### Step 2 - Define POV

|       | NORTHSTAR METRIC     |
|----|---|
| **What VALUE you want to measure?** | The effectiveness of orders |
| **WHEN the value DELIVERY SUCCESS?** | Orders are completed with no errors (such as number of receive products or stockable products) |
| **Northstar Metric Name**  | % No-error Orders (no-error order is order that the number of products in the order is equal to the number of stocked products) |
| **WHY do you choose this metric?** | Because the goal is to provide enough goods for the production department. |

### Step 3 - Ideate

| Layer 0 Dimension: Total Metrics   | Layer 1 Dimension: Breakdown by 1 Dimension |
|----|----|
| % no-error orders, % receive products, % reject products, % fee | % above over time, by ship method, and sub-category type |

**Next, I repeat Step 4 - Prototype and Review several times to achieve the final result**

<div id='vis'/>

## Visualization Process

### Data Modeling

Data imported to Power BI from Google BigQuery public dataset, then data is transformed in Power Query, finally modeled as below.

![data modeling](https://github.com/user-attachments/assets/98f43851-ab01-4de1-8394-adc2f6871420)

### Dashboard Building

Visual 1: Vendor Performance Overview

![overview](https://github.com/user-attachments/assets/c8559dd8-970a-4323-8610-2da1d4ed237f)

Visual 2: Vendor Performance Detail

![detail](https://github.com/user-attachments/assets/eb3511e4-922f-4b27-87bf-33d3348fb9f2)

<div id='how'/>

## How to Use Dashboard

Below is workflow suggestion:

| **Action**                      | **Description**                                                                                      |
|---------------------------------|------------------------------------------------------------------------------------------------------|
| Access and Review Summary       | Start by looking at the Overview tab to check key stats like error-free orders, total costs, extra fees, and the number of active vendors. This gives you a quick view of overall vendor performance and spending. |
| Analyze Trends and Rankings     | Use the trend charts to spot patterns or problems, like a drop in reliability or rising costs. Vendor rankings help you see which vendors are performing well and which need attention. |
| Select and Analyze Vendor       | Switch to the Vendor tab to focus on a specific vendor. View detailed metrics like non-error orders, extra fees, and trends, providing a closer look at their performance and cost-effectiveness. |
| Examine Vendor Details          | Check product-specific data such as pricing, fees, taxes, and freight costs. This gives you a complete view of each vendor’s cost structure and helps with decision-making. |
| Generate Reports and Take Action| Use the insights to create reports, share findings, and make informed decisions, like improving vendor relationships or renegotiating contracts. |
