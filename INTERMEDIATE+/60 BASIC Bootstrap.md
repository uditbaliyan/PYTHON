

---
### Bootstrap

- **Bootstrap** is a popular open-source front-end framework for designing responsive and mobile-first websites.

---

### Getting Started

- Include Bootstrap CSS and JavaScript files in your HTML.

```html
<!-- Add Bootstrap CSS -->
<link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">

<!-- Add Bootstrap JS and Popper.js (required for some components) -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
```

---

### Grid System

- Bootstrap's grid system allows for creating responsive layouts.

```html
<div class="container">
  <div class="row">
    <div class="col-sm-6">
      Left Column
    </div>
    <div class="col-sm-6">
      Right Column
    </div>
  </div>
</div>
```

---

### Components

- Bootstrap provides a wide range of pre-styled UI components.

```html
<button class="btn btn-primary">Primary Button</button>
<span class="badge badge-success">Success Badge</span>
```

---

### Navigation

- Easily create responsive navigation bars.

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">Navbar</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav ml-auto">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Features</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Pricing</a>
      </li>
    </ul>
  </div>
</nav>
```

---

### Forms

- Bootstrap provides styles for form elements.

```html
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1">
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

---

### Alerts

- Display contextual feedback messages.

```html
<div class="alert alert-success" role="alert">
  This is a success alert!
</div>
```

---

### Modals

- Create modal dialogs for pop-up content.

```html
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModal">
  Launch Modal
</button>

<div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Modal Title</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        Content goes here...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

---

### Note:

- Bootstrap provides a wide range of components and utilities. Refer to the [official Bootstrap documentation](https://getbootstrap.com/docs/4.5/getting-started/introduction/) for detailed information and examples.

Bootstrap simplifies front-end development by providing pre-styled components and a responsive grid system. It's widely used for creating modern and visually appealing websites.