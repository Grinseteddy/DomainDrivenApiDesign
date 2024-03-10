# Catalog Search

The catalog search allows members to search for books. It follows the CQRS pattern. The catalog itself is maintained in Catalog Maintenance. 

## Async

- Send Book not found (Search criteria)
- Receive New Catalog entry added (Catalog entry)

## Sync

- Get Catalog entry (search criterias)
- Post Catalog entry
- Put Catalog entry