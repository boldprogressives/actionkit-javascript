## ak-async-post.js

A replacement for ActionKit's widget.js ("AJAX signup") with a simpler Javascript API,
with no specific expectations about how your HTML is structured.

Usage:

var data = {
  "email": "joe@example.com",
  "name": "Joe Smith",
  "phone" "555-111-2345",
  "action_favorite_color": "Blue",
  "action_pets": ["dog", "cat"]
}; // or any valid actionkit form submission

function myCallback(result, data) {
  if (result === "error") {
    return doSomethingErroryWith(data); 
  }
  doSomethingSuccessyWith(data);
};

submitActionKitForm("https://act.example.com", "my-page-name", data, myCallback);
