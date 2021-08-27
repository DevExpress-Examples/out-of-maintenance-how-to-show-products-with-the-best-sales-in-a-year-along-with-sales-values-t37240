<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128581353/18.2.3%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T372408)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/Dashboard_AggrBestSalesProducts/Form1.cs) (VB: [Form1.vb](./VB/Dashboard_AggrBestSalesProducts/Form1.vb))
<!-- default file list end -->
# Dashboard for WinForms - How to calculate Highest Product Sales by Year


This example demonstrates how to use the [Aggr](https://docs.devexpress.com/Dashboard/115870) function to display products with the highest sales by year. 

## Example Structure

![screenshot](images/screenshot.png)

Aggregated data use the following custom expressions:

| Calculated Field | Expression |
| --- | --- |
| Max Product Sales by Year | ``` Aggr(Max([Product Sales by Year]), GetYear([OrderDate])) ``` |
| Product Sales by Year | ``` Aggr(Sum([Sales]), GetYear([OrderDate]), [ProductName]) ``` |
| Highest Product Sales | ``` Iif([Max Product Sales by Year] = [Product Sales by Year], [ProductName] + ' ($ ' + [Product Sales by Year] + ')', null) ``` |

## Documentation

- [Intermediate Level Aggregations](https://docs.devexpress.com/Dashboard/115870/)
- [Aggregations](https://docs.devexpress.com/Dashboard/115894/)
- [Expression Constants, Operators, and Functions](https://docs.devexpress.com/Dashboard/400122/)

## More Examples

- [Dashboard for WinForms - How to display best and worst monthly sales for each year](https://github.com/DevExpress-Examples/how-to-display-best-and-worst-monthly-sales-for-each-year-t369371)
- [Dashboard for WinForms - How to Calculate the Contribution of Quarterly Sales to Total Yearly Sales](https://github.com/DevExpress-Examples/how-to-calculate-the-contribution-of-quarterly-sales-to-total-yearly-sales)
- [Dashboard for WinForms - How to evaluate a customer acquisition using the quarter/year of their first purchase](https://github.com/DevExpress-Examples/how-to-divide-customers-count-by-the-number-of-orders-they-made-t372356)
- [Dashboard for WinForms - How to divide customers' count by the number of orders they made](https://github.com/DevExpress-Examples/how-to-divide-customers-count-by-the-number-of-orders-they-made-t372356)
- [Dashboard for WinForms - How to display sales by years in comparison with the previous year's sales](https://github.com/DevExpress-Examples/win-dashboard-display-previous-year-sales)
- [Dashboard for WinForms - How to Display Product Sales that are Greater than $20k](https://github.com/DevExpress-Examples/How-to-Display-Product-Sales-that-are-Greater-than-20k)
- [Dashboard for WinForms - How to Display Products with Sales Greater than Average Sales per Category](https://github.com/DevExpress-Examples/How-to-Display-Product-with-Sales-Greater-than-Average-Sales-per-Category)
