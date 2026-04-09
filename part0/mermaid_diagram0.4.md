sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note and clicks Save

    browser->>browser: Capture input value
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    Note right of server: Server stores the new note
    server-->>browser: HTTP  Created
    deactivate server

    Note right of browser: Browser updates the UI with the new note

