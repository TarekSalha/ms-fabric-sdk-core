# Release Notes

## 0.0.5

- getting or creating an item will retrieve automatically additional properties and item definitions. Note that when retrieving a list this is disabled by default, but can be enabled by setting `with_properties=True` (It is disabled because it takes significantly more time to retrieve all properties for all items)

```python
from msfabricpysdkcore import FabricClientCore

fc = FabricClientCore()
ws = fc.get_workspace_by_name("testworkspace")
items_with_details = ws.list_items(with_properties=True)
```

## 0.0.4

### New Features

- introduced general client
- added admin api client
- moved old client to core client
- added domains and all other admin apis
- more advanced usage patterns


## 0.0.3

### New Features

- added pagination
- added getting item by name and type
- added Lakehouse APIs for listing tables and loading tables
- added capacity reference by name
- added usage patterns for bulk operations

### Bug Fixes

- added a workaround for the create item API bug which does not return the item for all types