# doppler
Doppler is an intropection tool for redshift - to understand who is querying what.

## Quickstart
[TODO]

## What problem does this solve?
Data warehouses are really great, but as with any tool which is focussed on
providing access to a resource for all, it's important to know how it's being
used. Doppler is a tool to understand not what has been provisioned, but how
that provisioned content is being used. If you want to solve the problem of
making things consistent, then you should definitely look at [dbt](https://github.com/fishtown-analytics/dbt)
which is an excellent tool in this space. Doppler aims to answer a few of the
following questions:

- Which tables in my datawarehouse are being queried the most?
- Which users are querying my datwarehouse the most?
- Which tables are being used the most?
- [eventually] Which columns in my datawarehouse are being queried the most?

By understanding the answers to these questions, you can use those insights
to improve the design of your sql models.

## How does it work
We analyse the recent query logs of a datawarehouse, parse the sql to work
out the entities which are being queried and then export the data so that
you can extract the insights from it.
