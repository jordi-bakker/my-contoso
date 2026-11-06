# Demo-only customer selection with `?customer=`

There is no sign-in yet. For the demo, `?customer=C1001` selects the customer, and the server returns only that customer's data. This is not a security boundary: anyone can change the parameter. It is acceptable only with synthetic data, and real authentication must replace it before any real customer data is used. A missing or unknown customer shows a neutral "We couldn't find that customer" message, with no list of customers and no hint whether an ID exists.

## Considered Options

- Build real authentication in the first slice: rejected, it is out of scope for the first slice.
