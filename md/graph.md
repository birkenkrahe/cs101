```mermaid
graph TD
  A[[notes.txt]] --> B[Extract Tasks]
  B --> C[[tasks.csv]]
  C --> D[Verify]
  D -->|Fail| B
  D -->|Pass| E[[log.txt]]
```