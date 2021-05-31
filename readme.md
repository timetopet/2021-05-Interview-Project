
## Prerequisites

* [composer](https://getcomposer.org/download/) needs to be installed on your and available globally.
* Your local machine needs PHP 7.4 or later.

# Installation

1. Create a new **private** repository from your personal Github account.
2. `git clone` this new empty project to your local machine.
3. Download this project and unzip to the new repository your created.
4. **Important** Make an initial commit with the unzipped files.
2. From the command line run 'composer install'. This will take 5-10 minutes depending your internet connection and computer.
3. Start the local server `php artisan serve` and open http://localhost:8000 in your browser.

# Expectations

* We expect this project to take roughly 2-3 hours. 
* This project uses [Laravel 4.2](https://laravel.com/docs/4.2) 
* There are no limits on what JS libraries and/or CSS frameworks you use. Feel free to use whatever you are comfortable and most efficient with.
* Your submission will be reviewed on usability (of HTML page) and code quality. 
 
# Project Requirements

### GET:http://localhost:8000/widgets

Upon initial load, this HTML page should display a form to create a widget. A widget has 3 user set fields.

```
    name - Required. The name of the widget. Needs to be unique.
    color - Required. The color of the widget. Does not need to be unique.
    description - Optional. 
```

Form should handle input and enforce input requirements.

Once at least one widget has been created, this page should show a list of all available widgets. Clicking on a widget should allow us to edit it. We should also have the option to create additional widgets as well.

### GET:http://localhost:8000/api/widgets

This API endpoint should return a list of all created widgets as a JSON string.

### POST:https://localhost:8000/api/widget/create

This API endpoint should accept a JSON payload in the request body `{"name": "test widget", "color": "#0da2ff","description": "test description" }` allowing us to create a new widget. 

The response should return the newly created widget as a JSON string assuming input passes validation. Any issues with request should return a simple JSON response of form 

```
{
    "error": "This is what is wrong with your request"
}
```

### POST:https://localhost:8000/api/widget/edit

This API endpoint should accept a JSON payload in the request body `{"id": 1,"name": "test widget", "color": "#0da2ff","description": "test description" }` allowing us to modify an existing widget.

The response should return the updated widget as a JSON string assuming input passes validation. Any issues with request should return a simple JSON response of form 

```
{
    "error": "This is what is wrong with your request"
}
```


