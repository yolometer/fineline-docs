#Project data structure.
`/project/:pid` returns a project object
```json
{
  "title": "Title",
  "description": "Description.",
  "tasks": [{
    "title": "Title",
    "description": "Description.",
    "timespans": [[uid, start, end], …]
  }, …]
}
```
