---
title: Monitor Job Progress and Performance
description: Describes how you can create a work in process (WIP) method and calculate WIP to estimate the financial value of jobs while they are ongoing.
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.search.form: 89, 92, 1010
ms.date: 04/01/2021
ms.author: edupont

---
# Monitor Job Progress and Performance
As a job progresses, materials, resources, and other expenses are consumed and must be posted to the job. Work in Process (WIP) is a feature that enables you to estimate the financial value of jobs in the general ledger while the jobs are ongoing. In many cases, you might post expenses for a job before invoicing a job. When only expenses have been posted, your financial statement will be inaccurate. For more information, see [Understanding WIP Methods](projects-understanding-wip.md).

To track the value in the general ledger, you can calculate WIP and post the value to the general ledger.

You can calculate WIP based on the following:

* Cost Value
* Sales Value
* Recognizable Cost
* Percentage of Completion
* Completed Contract

If you want to view the result using a different method, you can change the method and calculate WIP again. There is no limit to the number of times that you calculate WIP. WIP is only calculated, it does not get posted to the general ledger. After you have calculated WIP, you can post to the general ledger.

## To create a job WIP method
You can create a job WIP method that reflects the needs of your organization. After you have created it, you can set it as the default job WIP calculation method that will be used in your organization.  

> [!NOTE]
> After you have used your new method to create WIP entries, you cannot delete the method or modify it.  

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job WIP Methods**, and then choose the related link.  
2. Choose the **New** action, and then fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Close the page.   
4. To make this new method the default, choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs Setup**, and then choose the related link.  
5. In the **Default WIP Method** field, choose the method from the list.

## To define a WIP method for a job
When you create a new job, you must specify which job WIP method that applies. In some cases, which Job WIP method that you can use has been set up for you as a default.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.
2. Choose the **New** action. For more information, see [Create Jobs](projects-how-create-jobs.md).  
3. On the **Job Card** page, in the **WIP Method** field, select a WIP method from the list. If a default method has been defined, you can select another option if needed.  

## To calculate WIP
You can determine the WIP amount that is to be posted to balance sheet accounts for the period end reporting. You use the **Job Calculate WIP** batch job to do this.  

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Calculate WIP**, and then choose the related link.  
2. Choose the **Calculate WIP** action.
3. On the **Job Calculate WIP** page, fill in the fields as necessary.
4. Choose the **OK** button.  

> [!NOTE]  
>   The batch job only calculates the WIP. It is not posted to the general ledger. To do so, you must run the **Post WIP to G/L** batch job when you have calculated the WIP. For more information, see the following procedure.

## To post WIP
When you have calculated WIP, you can post it to balance sheet accounts for the period end reporting. You use the **Job Post WIP to G/L** batch job to do this.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Post WIP to G/L**, and then choose the related link.  
2. On the **Job Post WIP to G/L** page, fill in the fields as necessary.  
3. Choose the **OK** button.

## To calculate and post job completion entries
When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**. Then, you must reverse any WIP that has been posted to the general ledger.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.  
2. Select an open job, and then choose the **Edit** action.
3. In the **Status** field, select **Completed**.
4. Follow the assistance steps to calculate and post WIP. Alternatively, follows steps 5 and 6 to do so manually.  
5. Choose the **Calculate WIP** action.
6. On the **Job Calculate WIP** page, fill in the fields as necessary.  

     The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.  
7. Choose the **Job Post WIP to G/L** action.
8. On the **Job Post WIP to G/L** page, fill in the fields as necessary.  

     The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.

## To view job ledger entries
All job-related entries are recorded in job registers and are numbered sequentially, starting with 1. From the job register, you can get an overview of all job ledger entries.    

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Registers**, and then choose the related link.
2. Select a relevant register, and then choose **Job Ledger** action.

On the **Job Ledger Entries** page you can review the entries that are associated with any job.  

## See Also
[Managing Projects](projects-manage-projects.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)   
[Finance](finance.md)  
[Purchasing](purchasing-manage-purchasing.md)         
[Sales](sales-manage-sales.md)      
[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
