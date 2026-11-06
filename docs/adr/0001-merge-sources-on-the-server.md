# Merge the two data sources on the server, by policy number

The Policy Overview needs the policy admin export (status, deductible, premium) and the coverage feed (cover). We join them on the server, keyed on policy number, and send the browser only the merged data of one customer. This keeps other customers' data out of the browser, which is a product rule. The admin export wins for what the customer pays and the policy status; the coverage feed wins for cover. If a policy is in only one source, it is still shown, with a clear missing-part message; it is never guessed or dropped. How the sources are reconciled in production is still open.

## Considered Options

- Join in the browser: rejected, it would send other customers' data to the browser.
