# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

My answer: C:\Users\zarri\sql\03_homework\images\Zarrin_sql_assignment1_q1_ERD1.drawio.png

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

My answer: C:\Users\zarri\sql\03_homework\images\Zarrin_sql_assignment1_q2_ERD2.drawio.png

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
```
My answer: C:\Users\zarri\sql\03_homework\images\Zarrin_sql_assignment1_q3.drawio.png & 
C:\Users\zarri\sql\03_homework\images\Zarrin_sql_assignment1_q1_2_3.drawio.png

There are privacy implications to consider when storing personal informations like customer addresses. Both architectures retain customer address information, which could potentially include sensitive personal data. Type 2 model retains historical changes and may pose greater privacy risks as it keeps a more detailed history of customer's address updates over time. It is important to have proper security measures and comply with personal and data protection regulations to ensure that customer privacy is protected, particularly with type 2 SCD model.


## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Your answer...
```
My answer: 

1-	My ERD displays the type of the relationship between tables, like one to many or many to many, which is not shown in AdventureWorks Schema. For example, in my ERD it is shown that "Employee Shift" and "Employee" tables have a "Many mandatory" to "Many Optional" relationship, as each shift must have at least one employee assigned to it, and an employee may or may not have any shifts assigned to them.  This means that while each shift must have employees assigned to it (many mandatory), employees may have shifts or may not have any shifts assigned to them (many optional).

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `June 1, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-3-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
