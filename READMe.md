# Styling HTML with CSS

## Step 1: Create the Project Folder

In your **Documents** folder, create a project folder named **UserPortalPart1**.

## Step 2: Create a Login Template

Inside the project folder, create a file named **login.html** using the template below:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Login</title>
    </head>
    <body>
        <div class="page-container">
            <h1>MyCompany</h1>
            <h2>Login</h2>
            <p>One sign-on.<br>Full access to our company website.</p>
            <form>
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required placeholder="Enter your username"><br><br>
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required placeholder="Enter your password"><br><br>
                <button type="submit">Login</button>
            </form>
            <a href="register.html">Don't have an account? Register here.</a>
        </div>
    </body>
</html>
```

- Save the file and preview it in your browser.

## Step 3: Create Inline CSS

- Create a `style` attribute for the `<h1>` element with the content below to override the default black font color.

```html
<h1 style="color: brown">MyCompany</h1>
```

- Save the file and preview it in your browser.

## Step 4: Create Internal CSS (Embedded CSS)

- Create internal CSS by adding a `<style>` element inside the `<head>` element with the styles below to center the content of the `<body>` element.

```html
<head>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100dvh;
        }
    </style>
</head>
```

- Save the file and preview it in your browser.

## Step 5: Create External CSS

- Inside the project folder, create a file named **style.css** with the content below.

```css
body {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Ubuntu, Cantarell, sans-serif;
    margin: 0;
}
h1,
h2,
p {
    margin: 0;
}
p {
    line-height: 1.6;
}
form {
    display: flex;
    flex-direction: column;
    gap: 15px;
}
label {
    font-weight: 600;
}
input {
    background: whitesmoke;
    border: none;
    border-radius: 999px;
    padding: 10px 20px;
    font-size: 16px;
    font-family: inherit;
    box-sizing: border-box;
}
input:focus {
    outline: none;
}
button {
    background: black;
    color: white;
    border: 1px solid black;
    border-radius: 999px;
    padding: 10px 20px;
    font-size: 16px;
    font-family: inherit;
    cursor: pointer;
}
a {
    color: black;
    text-decoration: underline;
}
.page-container {
    width: 100%;
    max-width: 450px;
    padding: 40px;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    gap: 15px;
}
```

- Link the external CSS file to your HTML by adding the `<link>` element inside the `<head>` element, as shown below.

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

- You can now safely remove the `<br>` tags from your HTML, as CSS is now handling the spacing. Your updated **login.html** page should look like this:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Login</title>
        <link rel="stylesheet" href="style.css">
        <style>
            body {
                display: flex;
                flex-direction: column;
                align-items: center;
                min-height: 100dvh;
            }
            
        </style>
    </head>
    <body>
        <div class="login-container">
            <h1 style="color:brown">MyCompany</h1>
            <h2>Login</h2>
            <p>One sign-on.<br>Full access to our company website.</p>
            <form>
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required placeholder="Enter your username">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required placeholder="Enter your password">
                <button type="submit">Login</button>
            </form>
            <a href="register.html">Don't have an account? Register here.</a>
        </div>
    </body>
</html>
```
- Save the file and preview it in your browser.

## Step 6: Create Register Page

- Inside the project folder, create a new file named **register.html** using the template below:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Register</title>
        <link rel="stylesheet" href="style.css">
        <style>
            body {
                display: grid;
                place-items: center;
                min-height: 100dvh;
            }
            .register-container {
                display: grid;
                grid-template-columns: 1fr 2fr;
                gap: 60px;
                max-width: 900px;
                width: 100%;
                padding: 40px;
                box-sizing: border-box;
            }
            @media (max-width: 768px) {
                .register-container {
                    grid-template-columns: 1fr;
                }
            }
        </style>
    </head>
    <body>
        <div class="register-container">
            <h1 style="color:brown">MyCompany</h1>
            <div class="page-container" style="max-width: 650;">
                <h2>Register</h2>
                <p>Create an account to access our company website.</p>
                <form>
                    <label for="fullname">Full Name:</label>
                    <input type="text" id="fullname" name="fullname" required placeholder="Enter your full name">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required placeholder="Enter your email">
                    <label for="username">Username:</label>
                    <input type="text" id="username" name="username" required placeholder="Enter your username">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password" required placeholder="Create a password">
                    <button type="submit">Register</button>
                </form>
                <a href="login.html">Already have an account? Login here.</a>
            </div>
        </div>
    </body>
</html>
```
- Save the file and preview it in your browser. 


