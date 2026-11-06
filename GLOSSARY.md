# My Contoso

My Contoso lets a Contoso Insurance customer see what they are covered for and what they pay. Customer service reads the same page.

## Language

**Customer**:
A person who holds one or more policies with Contoso Insurance and uses My Contoso to look at them.
_Avoid_: Client, user, policyholder

**Policy**:
One insurance contract of a customer, identified by its policy number.
_Avoid_: Contract, product, insurance

**Policy number**:
The identifier of a policy, shared by both data sources and used to match them.
_Avoid_: Policy ID, reference

**Policy Overview**:
The single page that shows one customer's policies with cover, deductible and premium, plus the monthly total. Customers and customer service see the same page.
_Avoid_: Dashboard, portal, staff view

**Cover**:
What a policy pays for. Comes from the coverage feed.
_Avoid_: Coverage, benefits

**Deductible**:
The part of a claim the customer pays themselves before the policy pays. Always shown as an amount with a short plain explanation.
_Avoid_: Excess, own risk

**Premium**:
What the customer pays for a policy. Comes from the policy admin export.
_Avoid_: Price, fee, cost

**Monthly total**:
The sum of the monthly premiums of the customer's active policies. Premiums billed per quarter or year are converted to a monthly amount and labelled as such.
_Avoid_: Grand total, balance

**Active policy**:
A policy that is currently in force. Only active policies count towards the monthly total.
_Avoid_: Live policy, current policy

**Ended policy**:
A policy that has ended or been cancelled. Shown in a separate, quieter section of the Policy Overview and left out of the monthly total.
_Avoid_: Expired policy, inactive policy, lapsed policy

**Policy admin export**:
The data source that is the source of truth for policy status, deductible and premium (what the customer pays).
_Avoid_: Admin file, CSV

**Coverage feed**:
The data source that is the source of truth for cover.
_Avoid_: Feed file, JSON

**Missing part**:
Information about a policy that one source could not provide. The Policy Overview says so plainly and never hides the policy.
_Avoid_: Error, blank
