sequenceDiagram
participant browser
participant server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
activate server
server->>browser: HTML Document
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa/main.css
activate server
server->>browser: CSS File
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa/spa.js
activate server
server->>browser: JavaScript File
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa/data.json
activate server
server->>browser: 0 Object { content: "noooo", date: "2023-02-01T10:39:28.691Z" }
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa/favicon.ico
activate server
server->>browser: favicon
deactivate server
