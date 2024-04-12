## Flask Application Design

### HTML Files
- **index.html**: The home page of the application, listing all tenants.
  - `<table>` to display tenant information (e.g., name, rent due, etc.)
  - Button to add new tenant
- **add_tenant.html**: Form for adding a new tenant.
  - Input fields for tenant name, rent due, etc.
  - Submit button to create the tenant

### Routes
- **GET /**: Route for the home page. Renders the `index.html` file with the list of tenants.
- **POST /add_tenant**: Route for adding a new tenant. Receives data from the `add_tenant.html` form, creates a new tenant object, and redirects to the home page.
- **GET /tenant/<id>/edit**: Route for editing an existing tenant. Renders a form prefilled with the tenant's data.
- **POST /tenant/<id>/update**: Route for updating an existing tenant. Receives data from the edit form, updates the tenant object, and redirects to the home page.
- **GET /tenant/<id>/delete**: Route for deleting an existing tenant. Confirms deletion and redirects to the home page.