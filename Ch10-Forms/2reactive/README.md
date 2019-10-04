# Chapter 10 Forms: Reactive form - login

## Objectives

- Add an authentication service
- Create a login form
- Update Display when user is logged in

## Steps

1. Continue working in your **my-angular-albums** project. If you haven't completed previous exercises, you can copy the src directory from the solution in the last exercise over yours.

1. Copy the files from the **/services** folder from the same folder of this README.me into your project folder **/app/services**.
   
2. In **app.module.ts** in the @NgModule decorator of core, import **ReactiveFormsModule** to be able to create a reactive form. Make sure the import of the module as an ES6 import is at the top of the file.

3. Copy the file from the **/shared** folder from the same folder of this README.me into your project folder **/app/shared**.   This defines an interface for login information.

4. Create a component for logging in, and have it added to **app.module.ts** by using the CLI

    ```command
      ng g c LoginComponent -it -is
    ```

5. View the files in the **/login** folder from the same folder of this README.me. Update your login files to match. 
    1. In the **login.component.html** notice the use of formGroup and how the error messages, and submit are worked with conditionally.
    2. In the **login.component.ts** file, notice the work with FormBuilder, and setting up of email and password along with Validators. Validators.required is built in, and ValidationService.emailValidator and ValidationService.passwordValidator are custom. 

6. Update the app-routing.module.ts file to add an entry for the path /login  

      ```javascript
          { path: "login", component: LoginComponent },
      ```

7. Update the **navbar.component.ts** and **navbar.component.html** to make the navbar dynamic so that the text displayed is either Login or Logout depending on the status. Refer to the **navbar** folder in this README document.

8. With these changes in place your code should now work. Clicking on login should bring up the login page. Once logged in, the navbar, which is subscribed to the service, should be updated to say Logout.