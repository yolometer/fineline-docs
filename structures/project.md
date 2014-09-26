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
    "timespans": [[tsid, uid, start, end], …]
  }, …]
}
```

#Semantics
When updating the project data, HTTP verbs apply thusly:
 - PUT puts all data present in the call, into the appropriate set with special semantics depending on the set.
  - PUT which includes a timespan will put on a timespan on the same timespan id(tsid)
  - PUT which includes a task will put on a task of the same title property.
 - DELETE removes all data present in the call, in the appropriate sets.
 - GET gets all data in the project.
