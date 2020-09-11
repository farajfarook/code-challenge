# Code  Challenge

## Requirement

You are required to building a **Production ready** application where you can automatically assign a Salesperson to a customer based on a set of rules.

We would like to see your Backend *(We Prefer .NET core)* as well Frontend *(We Prefer Angular)* skills. Don't stress about storing data in database use the attached JSON file as your data sources. If you are an experienced Java developer who likes to work on .NET, feel free on using Java to build the backend.

## Scenario

All salespeople are assigned to one or more groups from below.

- Group A – Speak Greek
- Group B – Sports car specialist
- Group C – Family car specialist
- Group D – Tradie vehicle specialist

**Salespeople Information** 

*you can find this data in [salesperson.json](salesperson.json)*

1. Cierra Vega. (Group A)
2. Alden Cantrell. (Group B & Group D)
3. Kierra Gentry. (Group A & Group C)
4. ...

**Salesperson Assigning Rules**

Rules on assigning a specific salesperson to the customer are below in priority order.

If a salesperson is assigned to a customer, that person cannot be assigned to another customer. If there are no salesperson available, application should return a message saying, &quot;All salespeople are busy. Please wait.&quot;

| **Customer** | **Looking for** | **Rules** |
| --- | --- | --- |
| **Speak Greek** | Sports Car | - Assign from Group A and Group B. <br/> - If cannot be found, assign from Group B <br/> - If cannot be found, assign from any group |
| **Speak Greek** | Family Car | - Assign from Group A and Group C. <br/> - If cannot be found, assign from Group A <br/> - If cannot be found, assign from any group |
| **Regardless of the language** | Tradie Vehicle | - Assign from Group D <br/> - If cannot be found, assign from any group |
| **Don't speak Greek** | Sports Car | - Assign from Group B <br/> - If cannot be found, assign from any group |
| **Don't speak Greek** | Family Car | - Assign from Group C <br/> - If cannot be found, assign from any group |
| **Speak Greek** | Not looking for anything specific | - Assign from Group A <br/> - If cannot be found, assign from any group |
| **Don't speak Greek** | Not looking for anything specific | - Assign from any group |

<hr/>

## Example Test Case

First Customer is Greek looking for a Family car – Assigned to Kierra Gentry

Second Customer is Greek looking for a Sports car – Assigned to Thomas Crane

Third Customer is English looking for a Sports car – Assigned to Alden Cantrell

….
