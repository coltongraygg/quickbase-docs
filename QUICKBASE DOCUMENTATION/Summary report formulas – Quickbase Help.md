## Summary report formulas

Use this feature to create a new type of calculation in a summary report. With it, you can perform calculations on a set of aggregate data by first summing the data set, and then calculating an average. This is made possible with a formula function you can plug into a report formula when customizing the report. Use this feature to create an "average of averages" in a report.

With summary formulas, you can create both report formulas and summary report formulas on summary reports.

Like report formulas, you can add custom calculations to your report summary formulas, but these formulas perform calculations on aggregated sets of data instead of individual values.

To create a summary formula, first identify which fields you want to aggregate and then write your formula as you normally would, using those aggregated fields. When building a summary report, you have the option to use **Report Formulas**, **Summary Formulas**, or a mix of both. **Summary Formulas** are exclusive to summary reports.

We can use summary formulas in three steps:

1.  So let’s define two summary variables, one for Order Total and the other for Total Cost. We start by defining summary variables. Summary formula use variables you define here, not ordinary fields. These variables are recognized only in these formulas.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572899954580/step_1_define.png)
2.  Next, we’ll write the summary formulas. Use your variables as you would normally use fields. For example, an income formula might be `[Revenue(tot)]-[expense(tot)]`.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572864121876/step_2_write.png)
3.  And finally, we’ll add the summary formula to display on the report.  
    ![](https://helpv2.quickbase.com/hc/article_attachments/4572864137492/sumarize_data.png)