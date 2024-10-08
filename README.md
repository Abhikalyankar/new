
# Blog API using Python, Django, and REST Framework


### A RESTful API for a blog application where users can perform CRUD operations on blog posts. This API include user authentication and role-based access.




# Hi, I'm Abhishek! 👋

## GitHub Profile Link
https://github.com/Abhikalyankar
## Documentation

#### Key Features:

User Authentication: Users must register and log in to access the API. The API uses token-based authentication (e.g., JWT) to secure endpoints.

Role-Based Access Control (RBAC): Different user roles (e.g., Admin, Author, Reader) have varying levels of access:
Admin: Full access to create, read, update, and delete any blog post.

Author: Can create new posts and modify or delete only their own posts.

Reader: Can view posts but cannot create, update, or delete them.
CRUD Operations:

Create: Users with the appropriate role can create new blog posts.
Read: All users (authenticated or not) can view a list of blog posts or details of a single blog post.

Update: Users can edit their own posts, while Admins can edit any post.

Delete: Users can delete their own posts, while Admins can delete any post.


API Features:

Pagination: Blog post lists are paginated to improve performance and user experience.

Sorting and Filtering: Users can sort and filter blog posts based on criteria such as publication date, author, or title.

Error Handling: Detailed and consistent error messages for invalid requests.

Authentication via JWT: All endpoints, except those that retrieve public blog posts, require a valid token to be accessed.
Technologies Used:

Backend Framework: Django REST Framework (DRF)
Authentication: JSON Web Tokens (JWT)

Database: PostgreSQL (or your preferred database)

Getting Started:

Prerequisites:

Python 3.x

Django

Django REST Framework

Django REST JWT
## EndPoints

Method         


| Method  | Endpoint                  | Description                       | Access         |
|---------|---------------------------|-----------------------------------|----------------|
| `GET`   | `/api/blog-list/`          | Retrieve a list of all blog posts | Public         |
| `GET`   | `/api/blog-details/{id}/`  | Retrieve a single blog post by ID | Public         |
| `POST`  | `/api/blog-create/`        | Create a new blog post            | Author, Admin  |
| `PUT`   | `/api/blog-update/{id}/`   | Update a blog post                | Author (own), Admin |
| `DELETE`| `/api/blog-delete/{id}/`   | Delete a blog post                | Author (own), Admin |
