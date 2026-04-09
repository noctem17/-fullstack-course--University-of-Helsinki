```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note and clicks Save

    browser->>browser: Capture input and prevent default form submission
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: Server stores the new note
    server-->>browser: HTTP Created
    deactivate server

    Note right of browser: JavaScript updates the DOM with the new note

