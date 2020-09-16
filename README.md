# Code  Challenge

## Requirement

You are required to build a **Production ready** application where you can automatically assign a Salesperson to a customer, based on a set of rules.

We would like to see your Backend and Frontend skills. Don't stress about storing data in database - instead, use the attached JSON file as your data source. Use design patterns and utilise coding best practices whereever applicable.
If you are an experienced Java developer who likes to work on .NET, feel free to use Java in order to build the backend. **We are using .NET Core and Angular in our team. And we love clean code.**

## Scenario

All salespeople are assigned to one or more groups from the below list.

- Group A – Speak Greek
- Group B – Sports car specialist
- Group C – Family car specialist
- Group D – Tradie vehicle specialist

**Salespeople Information** 

*you can find this data in [salesperson.json](salesperson.json)*

1. Cierra Vega. (assigned to Group A)
2. Alden Cantrell. (assigned to Group B & Group D)
3. Kierra Gentry. (assigned to Group A & Group C)
4. ...

**Salesperson Assigning Rules**

Rules on assigning a specific salesperson to a customer are below, in order of priority.

If a salesperson is assigned to a customer, that person cannot be assigned to another customer at the same time. If there are no salespeople available, the application should return a message saying, &quot;All salespeople are busy. Please wait.&quot;

| **Customer** | **Looking for** | **Rules** |
| --- | --- | --- |
| **Speaks Greek** | Sports Car | - Assign from Group A and Group B. <br/> - If cannot be found, assign from Group B <br/> - If cannot be found, assign from any group |
| **Speaks Greek** | Family Car | - Assign from Group A and Group C. <br/> - If cannot be found, assign from Group A <br/> - If cannot be found, assign from any group |
| **Regardless of the language** | Tradie Vehicle | - Assign from Group D <br/> - If cannot be found, assign from any group |
| **Doesn't speak Greek** | Sports Car | - Assign from Group B <br/> - If cannot be found, assign from any group |
| **Doesn't speak Greek** | Family Car | - Assign from Group C <br/> - If cannot be found, assign from any group |
| **Speaks Greek** | Not looking for anything specific | - Assign from Group A <br/> - If cannot be found, assign from any group |
| **Doesn't speak Greek** | Not looking for anything specific | - Assign from any group |

<hr/>

## Example Test Case

First Customer speaks Greek and is looking for a Family car – Assigned to Kierra Gentry

Second Customer speaks Greek and is looking for a Sports car – Assigned to Thomas Crane

Third Customer doesn't speak Greek and is looking for a Sports car – Assigned to Alden Cantrell

….
