# Putting it All Together: Client-Server Communication

## Learning Goals

- Understand how to communicate between client and server using fetch, and how
  the server will process the request based on the URL, HTTP verb, and request
  body
- Debug common problems that occur as part of the request-response cycle

## Introduction

Just like the last lesson, we've got code for a React frontend and Rails API
backend set up. This time though, it's up to you to use your debugging skills to
find and fix the errors!

To get the backend set up, run:

```console
$ bundle install
$ rails db:migrate db:seed
$ rails s
```

Then, in a new terminal, run the frontend:

```console
$ npm install --prefix client
$ npm start --prefix client
```

Confirm both applications are up and running by visiting
[`localhost:4000`](http://localhost:4000) and viewing the list of toys in your
React application.

## Deliverables

In this application, we have the following features:

- Display a list of all the toys
- Add a new toy when the toy form is submitted
- Update the number of likes for a toy
- Donate a toy to Goodwill (and delete it from our database)

The code is in place for all these features on our frontend, but there are some
problems with our API! We're able to display all the toys, but the other three
features are broken.

Use your debugging tools to find and fix these issues.

There are no tests for this lesson, so you'll need to do your debugging in the
browser and using the Rails server logs and `byebug`.

**Note**: You shouldn't need to modify any of the React code to get the
application working. You should only need to change the code for the Rails API.

As you work on debugging these issues, use the space in this README file to take
notes about your debugging process. Being a strong debugger is all about
developing a process, and it's helpful to document your steps as part of
developing your own process.

## Your Notes Here

- Add a new toy when the toy form is submitted

  - How I debugged:

- Update the number of likes for a toy

  - How I debugged:

- Donate a toy to Goodwill (and delete it from  database)

  - How I debugged:To start debugging, I would first check the Rails server logs for any errors or warnings that might give me an idea of what's going wrong with the API. I would also check the network tab in the browser's developer tools to see if any requests are failing or returning unexpected responses.

Add a new toy when the toy form is submitted:

I would check the controller action responsible for handling the toy creation request to see if it's receiving the correct parameters and if any errors are being thrown during the creation process.
I would also check if the CORS configuration is correctly set up to allow requests from the frontend to the API.
Update the number of likes for a toy:

I would check the controller action responsible for updating the number of likes for a toy to see if it's receiving the correct parameters and if any errors are being thrown during the update process.
I would also check if the frontend is sending the correct request method (PUT or PATCH) and if the CSRF token is being included in the request headers.
Donate a toy to Goodwill (and delete it from our database):

I would check the controller action responsible for handling the toy deletion request to see if it's receiving the correct parameters and if any errors are being thrown during the deletion process.
I would also check if the frontend is sending the correct request method (DELETE) and if the CSRF token is being included in the request headers.
Additionally, I would check if the controller is correctly handling the deletion of the associated records in any associated models, such as deleting any associated likes for the toy being donated.

