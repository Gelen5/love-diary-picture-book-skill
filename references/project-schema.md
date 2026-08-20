# Project working schema

Keep a compact working record for each project. It may be a Markdown or JSON file outside the final public package.

```yaml
project_title: ""
output:
  format: pdf
  ratio: 3:4
  page_count: null
people:
  - id: husband
    label: ""
    photo_refs: []
    approved_traits: []
  - id: wife
    label: ""
    photo_refs: []
    approved_traits: []
  - id: child
    label: ""
    photo_refs: []
    approved_traits: []
milestones:
  - date: YYYY-MM-DD
    event: ""
    source: user-confirmed | chat-export
    approved: false
scenes:
  - sequence: 1
    date: YYYY-MM-DD
    phase: first-contact
    excerpt: ""
    speaker: ""
    visual_brief: ""
    outfit: ""
    status: proposed | pilot | approved | proof | final
gates:
  characters: pending
  timeline: pending
  pilots: pending
  proof: pending
```

The schema is a working aid, not a requirement to expose the user's raw chat export or private photos in the final package.
