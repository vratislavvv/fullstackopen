# 0.5: Single page app diagram

``` mermaid
sequenceDiagram
    participant browser
    participant server
    participant javascript


    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    server-->>browser: HTML document

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->>browser: the css file

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    server-->>browser: the JavaScript file

    javascript->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->>javascript: the data in JSON format

    javascript->>browser: Renders the data as notes on the page
```