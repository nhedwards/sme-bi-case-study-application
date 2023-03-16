# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The goal of exercises in case study is for learners to apply what was learned in the previous courses to new problems or situations. This is best pedagogical practice for retaining and building skills.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/case-study-analyzing-customer-churn-in-tableau/exploratory-analysis-1?ex=4) from the Case Study: Analyzing Customer Churn in Tableau. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners in **case studies**.

## 1st VM Exercise

#### Dataset

- [ ] Add datasets used to the `datasets/` folder

#### Files

- [ ] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

Use Power Query Editor to unpivot the data into a table that simply shows the loan id, winning bid, and winning counterparty. Then transform the data in a way to find the top bid and bidder for each loan.


#### Context

The trade is on! You’ve sent the data tape out, and now you’re getting prices back from each counterparty. You need to be able to figure out who placed the highest offer on each mortgage loan so you know who you will trade it to. Luckily, this can be done within a few steps in Power Query Editor.


#### Steps to be executed by the student (max 6)

1. Upload loan_bids.xlsx into Power BI from the Datasets folder on the desktop.
2. Open the Power Query Editor and unpivot each counterparty so that there are only three columns: Loan ID, Price, and Bidder. Rename them accordingly.
3. In the Power Query Editor, click Group By and group the rows by loan id, and create a new column called “max price” that finds the max of price, and another column that includes all rows called “All bids”
4. Add a column within the Power Query Editor with this formula: Table.Max([All bids], "Price"
5. Expand the custom column and just include the counterparty.
6. Click close and apply. Double-check the relationship between loan_bids and loan_data is linked on loan_id on a one-to-one relationship.
7. Add a table that displays all the data with loan_id as the first field, and give it a title, “Loan-level data”.


#### Exercise question:
What is the max bid for loan id 5021364? Round your answer to the nearest 100th (i.e. 100.00).
100.89.


#### End goal:

[Screenshot 2023-03-15 at 9 39 40 PM](https://user-images.githubusercontent.com/107631815/225487671-66530dd2-cae8-467b-8488-0619508558fb.png)

## Finalized Workbook

#### Files
You can upload your final workbook in the exercises folder as `ex-final-sol.twbx` or `ex-final-sol.pbix`.

#### Explanation & Description
This is the first exercise in chapter two. The learner will use steps in the Power Query Editor to organize the bids in an effective way to pool mortgages to the highest bidders in order to maximize trade proceeds.

This exercise is foundational to the rest of the course. Without properly identifying the winning bids and prices, we cannot create mortage pools, which are the way the mortgages are grouped and sold to buyers, or perform financial analysis on the profit earned from trading.

#### End goal:
![Screenshot 2023-03-15 at 9 44 44 PM](https://user-images.githubusercontent.com/107631815/225488311-b965c3ab-2b98-4216-818c-28a02b9d2b69.png)
