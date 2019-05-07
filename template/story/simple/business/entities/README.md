# Data entities

Data entities contain the entity-specific business rules for a given item 
of data. Data entities contain:

- A collection of data attributes (mandatory)
- A collection of entity-specific business rules (optional but usual)

## Example - a Fixed Rate Loan

The concept of a loan on which interest is payable is well understood. A loan 
may be represented by a Data Entity called Loan. Let's consider the attributes
and entity-specific rules for a simple Fixed Rate Loan.

### Data Attributes of a Loan

A Loan may have a number of attributes:

1. The amount of the loan (the principal)
2. The interest rate of the loan (the rate) 
3. The repayment period of the loan (the period)

### Entity-specific Business Rules for a Loan

Typical entity-specific business rules would be:

- makePayment()
- applyInterest()
- chargeLateFee()

## Published Data Entities

A Data Entity may be reused by a number of Stories or, indeed, by a number of
separate applications. A Loan, for example, is a very common concept and so 
it's very likely that a Loan Data Entity would be reused many times.

In such cases, these Data Entities are likely to be stored in their own
separate modules (or repositories) and be referenced by the various Stories
that interact with them. Such Data Entities are called Published Data Entities.

## Restricted Data Entities

When this is the case, the *entities* folder within a Story contains Data 
Entities that are excusively used by the current Story and are not used by
by any other Story, they appear in the *entities* folder of a Story. In such
cases, the Data Entities are known as Restricted Data Entities because they
are restricted to use within the scope of the current Story.



