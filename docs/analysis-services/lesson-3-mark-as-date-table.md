---
title: "Lesson 4: Mark as Date Table | Microsoft Docs"
ms.custom: ""
ms.date: "03/27/2017"
ms.prod: analysis-services
ms.prod_service: "analysis-services, azure-analysis-services"
ms.service: ""
ms.component: ""
ms.reviewer: ""
ms.suite: "pro-bi"
ms.technology: 
  
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "SQL Server 2016"
ms.assetid: c32cc336-b7d8-4122-9d62-4936344d2315
caps.latest.revision: 18
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Lesson 3: Mark as Date Table
[!INCLUDE[ssas-appliesto-sql2016-later-aas](../includes/ssas-appliesto-sql2016-later-aas.md)]

In Lesson 2: Add Data, you imported a dimension table named DimDate. While in your model this table is named DimDate, it can also be known as a *Date table*, in that it contains date and time data.  
  
Whenever you use DAX time-intelligence functions in calculations, as you'll do when you create measures a little later, you must specify date table properties, which include a *Date table* and a unique identifier *Date column* in that table.
  
In this lesson, you'll mark the DimDate table as the *Date table* and the Date column (in the Date table) as the *Date column* (unique identifier).  

Before we mark the date table and date column, we need to do a little housekeeping to make our model easier to understand. You'll notice in the DimDate table a column named **FullDateAlternateKey**. It contains one row for every day in each calendar year included in the table. We'll be using this column a lot in measure formulas and in reports. But, FullDateAlternateKey is not really a good identifier for this column. We'll rename it to **Date**, making it easier to identify and include in formulas. Whenever possible, it's a good idea to rename objects like tables and columns to make them easier to identify in client reporting applications like Power BI and Excel. 
  
Estimated time to complete this lesson: **3 minutes**  
  
## Prerequisites  
This topic is part of a tabular modeling tutorial, which should be completed in order. Before performing the tasks in this lesson, you should have completed the previous lesson: [Lesson 2: Add data](../analysis-services/lesson-2-add-data.md). 

### To rename the FullDateAlternateKey column

1.  In the model designer, click the **DimDate** table.

2.  Double click the header for the **FullDateAlternateKey** column, and then rename it to **Date**.

  
### To set Mark as Date Table  
  
1.  Select the **Date** column, and then in the **Properties** window, under **Data Type**, make sure  **Date** is selected.  
  
2.  Click the **Table** menu, then click **Date**, and then click **Mark as Date Table**.  
  
3.  In the **Mark as Date Table** dialog box, in the **Date** listbox, select the **Date** column as the unique identifier. It will usually be selected by default. Click **OK**. 

    ![as-tabular-lesson3-date-table](../analysis-services/media/as-tabular-lesson3-date-table.png)
  

## What's next?
Go to the next lesson: [Lesson 4: Create Relationships](../analysis-services/lesson-4-create-relationships.md).
  
