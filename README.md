# Code  Challenge

## Requirement

You are required to building a **Production ready** application where you can automatically assign a Salesperson to a customer based on a set of rules.

We would like to see your Backend as well as in Frontend skills in any technology that you are familiar with. Don&#39;t stress about storing data in database use the attached JSON files as your data sources.

## Scenario

All salespeople are assigned to one or more groups from below.

- Group A – Speak Greek
- Group B – Sports car specialist
- Group C – Family car specialist
- Group D – Tradie vehicle specialist

**Salespeople information**

1. Cierra Vega. (Group A)
2. Alden Cantrell. (Group B &amp; Group D)
3. Kierra Gentry. (Group A &amp; Group C)
4. Pierre Cox. (Group D)
5. Thomas Crane. (Group A &amp; Group B)
6. Miranda Shaffer. (Group B)
7. Bradyn Kramer. (Group D)
8. Alvaro Mcgee. (Group A &amp; Group D &amp; Group C)

**Salesperson assigning Rules**

Rules to assign a specific salesperson to the customer is as below in priority order.

If a salesperson is assigned to a customer, that person cannot be assigned to another customer. If there are no salesperson available, application should return a message saying, &quot;All salespeople are busy. Please wait.&quot;

| **Customer** | **Looking for** ||
| --- | --- | --- |
| **Speak Greek** | Sports Car | - Assign from Group A and Group B. <br/> - If cannot be found, assign from Group B <br/> - If cannot be found, assign from any group |
| **Speak Greek** | Family Car | - Assign from Group A and Group C. <br/> - If cannot be found, assign from Group A <br/> - If cannot be found, assign from any group |
| **Regardless of the language** | Tradie Vehicle | - Assign from Group D <br/> - If cannot be found, assign from any group |
| **Don&#39;t speak Greek** | Sports Car | - Assign from Group B <br/> - If cannot be found, assign from any group |
| **Don&#39;t speak Greek** | Family Car | - Assign from Group C <br/> - If cannot be found, assign from any group |
| **Speak Greek** | Not looking for anything specific | - Assign from Group A <br/> - If cannot be found, assign from any group |
| **Don&#39;t speak Greek** | Not looking for anything specific | - Assign from any group |


## Example test case

First Customer is Greek looking for a Family car – Assigned to Kierra Gentry

Second Customer is Greek looking for a Sports car – Assigned to Thomas Crane

Third Customer is English looking for a Sports car – Assigned to Alden Cantrell

….
