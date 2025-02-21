# MVCBlogSite

MVCBlogSite is a blog web application developed using the **ASP.NET Core MVC** framework. This application allows users to manage blog posts, view them, and interact with the content. The application follows the **Model-View-Controller (MVC)** design pattern, making it scalable, maintainable, and easy to extend.

## Features

- **Post Management:**
  - Create, edit, and delete blog posts.
  - Display posts on the homepage with sorting and pagination.

- **User Roles:**
  - **Admin**: Manage users, blog posts, and application settings.
  - **Guest/Reader**: View blog posts.

- **Comments**:
  - Users can add comments to posts.
  - Moderation features for admin.

- **User Authentication**:
  - Built-in user authentication using ASP.NET Identity.

- **Search Functionality**:
  - Users can search for blog posts by title and content.

## Installation

To run the project on your local machine:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/MVCBlogSite.git
    ```

2. Open the project in **Visual Studio** or **Visual Studio Code**.

3. **Install dependencies** by restoring the NuGet packages:
    - If using Visual Studio, right-click the solution and select **Restore NuGet Packages**.
    - If using Visual Studio Code, use the terminal:
      ```bash
      dotnet restore
      ```

4. **Run the application**:
    - If using Visual Studio, press **F5** or use **Ctrl + F5**.
    - If using Visual Studio Code, run:
      ```bash
      dotnet run
      ```

5. Navigate to **http://localhost:5000** in your browser to see the application.

## Requirements

- **.NET Core 3.1** or higher
- **ASP.NET Core MVC**: Built-in framework for creating web apps using the MVC pattern.
- **Entity Framework Core**: Used for database access (SQLite or SQL Server).

## Project Structure

The project is structured as follows:

- **Controllers**:
  - **BlogController**: Handles requests related to blog posts, including CRUD operations.
  - **AccountController**: Manages user login, registration, and profile functionality.
  - **AdminController**: Admin functionalities for managing posts and users.
  
- **Models**:
  - **Post**: Represents a blog post, with properties such as `Title`, `Content`, `Author`, `DateCreated`, etc.
  - **Comment**: Represents comments on blog posts, with properties like `Author`, `Content`, `PostId`.
  - **User**: Represents user information, extending the ASP.NET Identity model.

- **Views**:
  - **Home/Index.cshtml**: Displays a list of blog posts.
  - **Posts/Create.cshtml**: Form for creating a new post.
  - **Posts/Details.cshtml**: Displays a single blog post with its comments.
  - **Account/Login.cshtml**: User login form.
  - **Admin/Index.cshtml**: Dashboard for managing posts and users.
  
- **Data**:
  - Contains database context class for accessing the database using **Entity Framework**.

- **Services**:
  - **PostService**: Contains business logic for managing blog posts.
  - **CommentService**: Contains business logic for managing comments.

## Technologies Used

- **ASP.NET Core MVC**: Web framework for building the application.
- **Entity Framework Core**: ORM for database access.
- **ASP.NET Identity**: User authentication and authorization.
- **SQLite** (or **SQL Server**): Database for storing blog data.
- **HTML, CSS, JavaScript**: For frontend UI.
- **Bootstrap**: For responsive and clean UI design.

## Usage

- **Admin**: 
  - Login to manage posts and users.
  - Create, edit, or delete blog posts.
  - Manage user roles and permissions.
  
- **User**:
  - View blog posts.
  - Leave comments on posts.
  - Use the search bar to find posts by title or content.

- **Guest**: 
  - View blog posts but cannot leave comments or create posts.

## Contributions

We welcome contributions to the project. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Open a pull request with a description of the changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
