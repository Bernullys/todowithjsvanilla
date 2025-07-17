# todowithjsvanilla
This is a To Do app using JS vanilla

This app is based in a class of ColorCode DOM API video.

At first it was doing it on the inspectator console of the web browser.
The main objective was to manipulate the DOM API, so we clean up the body using: document.body.innerText = "" , and then start to creating the application. I did it a couple of times but after that I want to really use it so I create the repository.

The first function was creating a title, label, input, a button and a section were to put all ToDo's. So we create those elements and then append them to the body. At first we create a function to create list items of the input content onclick of the button, append those items to a section and then clean the value of the input.

Then we add a form to improve a little bit. So instead of a function we create the formName.onsubmit = (e) => e.preventDefault() .....
So now we have the advantage of a form.

Then I add two buttons when creating a todo. One to delete and another to check if the todo is done.

The delete button has its detail: we create a function that applaid the function remove() to its argument. But here is the detail: when we applay onclick to the delete button equals to the delete function we have to apply the bind function. Bind function does: (chatGpt response)

        The bind method is used to create a new function (deleteTodo with a partially applied argument) and set its this value to null. The this value is not used inside deleteTodo, so null is passed.

        The first argument (null) in bind is the value to be used as this when calling deleteTodo. In this case, since deleteTodo doesn't use this, it doesn't matter what value is used.

        The second argument (todoContainer) is passed to deleteTodo as its first argument (el). This is done through the bind method, effectively creating a new function that expects the element to be deleted as its first argument.

        The result is that when deleteButton is clicked, deleteTodo is called with todoContainer as its argument.

        This usage of bind allows you to create a function (deleteTodo) that can be used as an event handler with a specific argument (todoContainer). This is particularly useful when you need to pass additional parameters to a function used as an event handler.

Then the check button adds a class to the text of the todo, and also changes the textContent of itself.

Then I add classes using style label and with DOM manipulation using classList.

The if statement check if the value of the input isn't empty so it can't add empty todos.

Then I add a functionallity of the subtitle to be visible only when there were todos added.

Then I add a counter of todos, having a variable initialazed on zero and add one everytime the form is submited and substracting one when deleting a todo.
