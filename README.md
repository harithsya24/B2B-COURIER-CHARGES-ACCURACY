# B2B-COURIER-CHARGES-ACCURACY

# B2B Ecommerce Fraud: Case Study - ABC Company

ABC Company operates an e-commerce platform and processes thousands of orders daily. To deliver these orders, ABC has partnered with several courier companies in India, which charge them based on the weight of the products and the distance between the warehouse and the customer’s delivery address. ABC wants to check if the fees charged by the courier companies for each order are correct.

## Table of Contents

1. [Introduction](#introduction)
2. [Datasets](#datasets)
3. [Methodology](#methodology)
4. [Solution](#solution)
5. [Results](#results)
6. [Conclusion](#conclusion)

## Introduction

ABC Company needs to verify the accuracy of courier charges for each order. This involves comparing the weights calculated from the company's internal data against the weights stated in the courier invoices. Additionally, the delivery zones and charges must be validated to ensure correct billing.

## Datasets

ABC's internal data is split across three reports:
1. **Website Order Report**: Contains order IDs and products (SKUs) for each order.
2. **Master SKU**: Provides the gross weight of each product.
3. **Warehouse PIN for All India Pincode Mappings**: Used to determine the delivery area.
Dataset is taken from: https://statso.io/b2b-ecommerce-fraud-case-study.

Courier companies provide the following billing data:
1. **Courier Company Invoices**: Includes AWB number, order ID, shipment weight, warehouse pickup PIN, customer delivery PIN, delivery area, charge per shipment, and type of shipment.

## Methodology

1. **Calculate Total Weight**: Using the Website Order Report and Master SKU, calculate the total weight of each order. Round up the weight to the nearest multiple of 0.5 kg.
2. **Determine Delivery Area**: Use the warehouse PIN to all India Pincode mappings to determine the delivery area and compare it with the courier company's reported area.
3. **Calculate Expected Charges**: Apply the logic of calculating charges based on the weight slab, delivery area, and type of shipment using the courier fee rate card. The total charge per shipment is the sum of the fixed charge and any additional charges based on plate weight.
4. **Compare and Analyze**: Compare the calculated total weight and charges with those stated by the courier company. Identify discrepancies and categorize them as correctly charged, overcharged, or undercharged.

## Results

The results will highlight the accuracy of the fees charged by the courier companies. This analysis will help ABC identify any discrepancies and take necessary actions to rectify incorrect charges.

## Conclusion

This case study aims to ensure accurate billing by courier companies, thereby preventing financial losses due to overcharging and ensuring fair transactions. By systematically comparing internal calculations with courier invoices, ABC can maintain transparency and accountability in its operations.
