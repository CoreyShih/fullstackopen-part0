# New note in Single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: browser executes JavaScript code that adds form data to notes
    Note right of browser: browser executes callback function that renders notes
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of browser: browser sends payload containing submitted form data
    Note left of server: server executes JavaScript code that adds form data to notes
    server-->>browser: 201 Created
    deactivate server
```