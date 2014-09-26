#Project data structure.
`/project/:pid` returns a project object consisting of either the entire structure or the changes since the If-Modified-Since header's timestamp.

The basic structure is thus:
```json
{
  "title": "Title",
  "description": "Description.",
  "participants": [uid, …],
  "tasks": [{
    "title": "Title",
    "description": "Description.",
    "timespans": [[uid, start, end], …]
  }, …]
}
```
