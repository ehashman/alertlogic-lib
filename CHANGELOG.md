# 0.3.0

API changes:

- AL Customer IDs in the customer map are returned as a list of matching IDs,
  for those customers that have multiple AL accounts.

# 0.2.0

API changes:

- Return deferreds instead of dereferencing them for the consumer.
- Return all data from the AL API instead of filtering it down to name, device
  type, status and IP addresses.

# 0.1.2

Enhancement: warns user when they attempt to query Log Manager devices for a
null customer, and prevents such requests from being sent.

# 0.1.1

Bugfix: get log manager device type at top-level of the returned JSON (instead
of looking inside the status info).

# 0.1.0

Initial release.

## Customers

- Adds `get-customers!` for fetching Alert Logic customer accounts and
  sub-accounts
- Adds `get-customers-map!` which maps known customer IDs (based on a naming
  convention) to Alert Logic customer IDs

## Log Manager

- Adds `get-lm-devices-for-customer!` for fetching all devices available under
  the Alert Logic Log Manager for a given customer
