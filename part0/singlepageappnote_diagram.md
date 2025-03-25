# 0.6: New note in Single page app diagram

``` mermaid
sequenceDiagram
    participant Browser
    participant JavaScript
    participant Server

    Browser->>JavaScript: Form data (input)
    Note left of JavaScript: JS code captures the form data and prevents form submission

    JavaScript->>Server: Sends a POST request to server for updating the list

    Server-->>JavaScript: Sends a response status with a JSON confirmation

    JavaScript-->>Browser: Renders an updated list of notes (output)
```