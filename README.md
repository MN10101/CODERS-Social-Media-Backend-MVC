
![logocyber.png](src/main/resources/img/logocyber.png)

# [ CODERS ]  Social Media App
# Overview
It is a **social** **media** **platform** where users can register, create posts, find friends, and interact with each other's content. 

This **MVC** **app** showcases the use of various technologies such as: 

- **Spring** with **Jpa**, **Web**, **Security**, **Email**. 

- **UI/UX**: **Thymeleaf** with **Bootstrap** is used for creating great user interface for both **desktop** and **mobile** friendly user experience. 

- **Jira** was used for project managment.

- The final touch brings deployment the app on **AWS** using **Elastic** **Beanstalk** service.

# Features

- User registration and authentication
- CRUD operations for posts, comments, and likes
- Friendship management
- Admin dashboard for managing users, posts, and comments
- Real-time updates and email notifications
- Local weather information
- Password validation during registration, change and reset of the password
- Token generation for password reset
- Filter of bad speech
- Deployed in AWS


# Technologies

- Java
- Spring Boot
- Spring Security
- Thymeleaf
- Hibernate (JPA)
- MySQL
- Spring Mail
- OpenWeather API
- Jira

# Setup

## Prerequisites

- JDK 11 or higher
- Maven
- MySQL

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/MN10101/CODERS-Social-Media-Backend-MVC
    ```

2. Set up the MySQL database:
    ```sql
    CREATE DATABASE a3m;
    ```

3. Configure the application properties:
    Update the `src/main/resources/application.properties` file with your MySQL database credentials.
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/a3m
    spring.datasource.username=***
    spring.datasource.password=***
    spring.jpa.hibernate.ddl-auto=update
    ```
4. Add the Weather API key to application properties:
   ```properties
   weather.api.key=your_actual_api_key_here
   ```

5. Build and run the application:
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

6. Access the application at `http://localhost:5000`.

# Database Diagram

EER Diagram
Visual representation of the Entity-Relationship for the database schema.

![eer.png](src/main/resources/img/eer.png)

# Project Structure

## MVC Architecture
![MVCArchitectureCoders.png](src/main/resources/img/MVCArchitectureCoders.png)


## Controllers

- `AdminControllerMVC.java`: Handles admin-related operations like managing users, posts, and comments.
- `CommentControllerMVC.java`: Manages CRUD operations for comments.
- `FriendshipControllerMVC.java`: Manages friendships and friendship invitations.
- `HomeControllerMVC.java`: Redirects to the login success page.
- `LikeController.java`: Manages like and unlike operations for posts and comments.
- `LoginControllerMVC.java`: Handles user login and logout operations.
- `MemberControllerMVC.java`: Manages member profiles and their related operations.
- `PostControllerMVC.java`: Handles CRUD operations for posts.
- `UserControllerMVC.java`: Manages user-related operations like registration and profile updates.
- `WeatherControllerMVC.java`: Fetches and displays local weather information.
- `EmailController.java`: Handles email-related operations.

## Entities

- `Admin.java`: Represents an admin user.
- `Authority.java`: Represents user roles and permissions.
- `Comment.java`: Represents a comment on a post.
- `FriendshipInvitation.java`: Represents a friendship invitation between members.
- `Like.java`: Represents a like on a post or comment.
- `Member.java`: Represents a member with additional profile details.
- `Post.java`: Represents a post created by a member.
- `User.java`: Represents a user in the application.
- `Token.java`: Represents a token for password reset and email verification.

## Repositories

- `AdminRepository.java`: Repository for admin-related database operations.
- `AuthorityRepository.java`: Repository for authority-related database operations.
- `CommentRepository.java`: Repository for comment-related database operations.
- `FriendshipInvitationRepository.java`: Repository for friendship invitation-related database operations.
- `LikeRepository.java`: Repository for like-related database operations.
- `MemberRepository.java`: Repository for member-related database operations.
- `PostRepository.java`: Repository for post-related database operations.
- `UserRepository.java`: Repository for user-related database operations.
- `TokenRepository.java`: Repository for token-related database operations.

## Services

- `AdminService.java`: Contains business logic for admin operations.
- `AdminServiceImpl.java`: Implementation of `AdminService`.
- `AuthorityService.java`: Contains business logic for authority operations.
- `AuthorityServiceImpl.java`: Implementation of `AuthorityService`.
- `BadWordsFilterService.java`: Filters obscene language in comments and posts.
- `CommentService.java`: Contains business logic for comment operations.
- `CommentServiceImpl.java`: Implementation of `CommentService`.
- `FriendshipService.java`: Contains business logic for friendship operations.
- `FriendshipServiceImpl.java`: Implementation of `FriendshipService`.
- `LikeService.java`: Contains business logic for like operations.
- `LikeServiceImpl.java`: Implementation of `LikeService`.
- `MemberService.java`: Contains business logic for member operations.
- `MemberServiceImpl.java`: Implementation of `MemberService`.
- `PostService.java`: Contains business logic for post operations.
- `PostServiceImpl.java`: Implementation of `PostService`.
- `UserService.java`: Contains business logic for user operations.
- `UserServiceImpl.java`: Implementation of `UserService`.
- `WeatherService.java`: Fetches weather information from the OpenWeatherMap API.
- `EmailService.java`: Sends emails for various notifications.
- `TokenService.java`: Manages tokens for password reset and email verification.
- `TokenServiceImpl.java`: Implementation of TokenService.

## Security

- `CustomAuthenticationFailureHandler.java`: Custom handler for authentication failures.
- `CustomAuthenticationSuccessHandler.java`: Custom handler for authentication successes.
- `WebSecurityConfig.java`: Configures web security settings including authentication and authorization.

## Exception Handling

- `GlobalExceptionHandler.java`: Handles global exceptions in the application.
- `UserNotFoundException.java`: Custom exception for handling user not found scenarios.

## Database Initialization

- `DatabaseLoader.java`: Initializes the database with initial data for admin and members.

## Frontend

- `styles-grey.css`: Grey-themed styles for the application.
- `styles-lila.css`: Lila-themed styles for the application.
- `cards.html`: HTML template for displaying cards.
- `footer.html`: Footer template.
- `head.html`: Head template.
- `header.html`: Header template.
- `navbar.html`: Navbar template.
- `admin-dashboard.html`: Admin dashboard template.
- `comments-list.html`: Template for listing comments.
- `members-list.html`: Template for listing members.
- `posts-list.html`: Template for listing posts.
- `comment-error.html`: Template for displaying comment errors.
- `comment-form.html`: Template for comment form.
- `comment-info.html`: Template for displaying comment information.
- `comments.html`: Template for displaying comments.
- `error.html`: Template for general error page.
- `error-unable.html`: Template for blocked user error page.
- `friends.html`: Template for displaying friends list.
- `friendship-invitations.html`: Template for displaying friendship invitations.
- `home.html`: Home page template.
- `login-form.html`: Login form template.
- `login-success.html`: Login success page template.
- `member-change-password.html`: Template for changing member password.
- `member-error.html`: Template for member error page.
- `member-form.html`: Template for member registration and update form.
- `member-info.html`: Template for displaying member information.
- `members.html`: Template for displaying all members.
- `post-error.html`: Template for post error page.
- `post-form.html`: Template for creating and updating posts.
- `post-info.html`: Template for displaying post information.
- `posts-of-friends.html`: Template for displaying friends' posts.
- `posts-your.html`: Template for displaying user's posts.
- `weather.html`: Template for displaying weather information.
- `forgot-password.html`: Template for the forgot password page.
- `reset-password.html`: Template for the reset password page.

## Configuration Files

- `application.properties`: Configuration file for application properties.
- `application-dev.properties`: Configuration file for development environment properties.
- `application-prod.properties`: Configuration file for production environment properties.
- `application-secrets.properties`: Configuration file for secret properties.
- `pom.xml`: Maven Project Object Model (POM) file.

### Dependencies

- Spring Boot Actuator
- Spring Boot Data JPA
- Spring Boot Thymeleaf
- Spring Boot Validation
- Spring Boot Web
- MySQL Connector
- Spring Boot Test
- Spring Boot Security
- Spring Mail
- Thymeleaf Extras Spring Security 6
- Spring Boot Data REST
- Jackson for JSON Parsing

# Usage

## User Registration

1. Navigate to `/mvc/member-form` to register a new member.
2. Fill in the required details and submit the form.
3. Once registered, you will be redirected to the login page.

## Log in

1. Navigate to `/login-form`to log in with an already existing account.
2. Manage the reset of your password going to `/forgot-password`and provide your email and your username to get the reset instructions.


## Own Profile

1. Navigate to `/mvc/members/?memberId={memberId}` to view your profile as an authenticated member.
2. Update your personal information and preferences as needed.
3. Create and update your own posts.
4. View yours friends and your friendship requests.
5. Get information about the weather in your city.

## Friend's profile

1. Navigate to `/mvc/members/?memberId={memberId}` to view the profile of a friend as an authenticated member.
2. View the the personal information of your friend.
3. See the posts of your friend and interact with it with comments and likes.

## Public Feed

1. Navigate to `/mvc/post-of-friends`to view all the posts of your friends.
2. View your friendship requests. 

## Creating and Managing your Posts

1. Navigate to `/mvc/posts-your` to view your posts.
2. Use the form to create new posts.
3. Edit or delete existing posts using the provided options.

## Managing Friendships

1. Navigate to `/mvc/friends` to view your friends.
2. Visit `/mvc/members`to see a list of all the members of the application, search by username and send friendship invitations.
3. Go to `/mvc/friendship-invitations to accept, or decline friendship invitations.
   - Send invitations from the members list.
   - Accept or decline invitations from the friendship invitations page.
4. Remove friends if necessary.

## Admin Dashboard

1. Access the admin dashboard at `/admin-dashboard/admin-dashboard`.
2. Manage users, posts, and comments:
   - View all members, search by username, block/unblock, or delete members.
   - View all posts, search by username, or delete posts.
   - View all comments, search by username, or delete comments.
3. Create initial records or delete all records if needed.




# Demo
## Create an account
![Coders002.png](src/main/resources/screens-cyber/Cybers002.png)

## Validation
![Cybers004.png](src/main/resources/screens-cyber/Cybers004.png)

## Login
![Cybers001.png](src/main/resources/screens-cyber/Cybers001.png)

## Forget Password
![Cybers005.png](src/main/resources/screens-cyber/Cybers005.png)

## Forget Password - Email Notification
![Cybers006.png](src/main/resources/screens-cyber/Cybers006.png)

## Feed
![Cybers007.png](src/main/resources/screens-cyber/Cybers007.png)

## Member Page
![Cybers008.png](src/main/resources/screens-cyber/Cybers008.png)
![Cybers010.png](src/main/resources/screens-cyber/Cybers010.png)

## Update Member
![Cybers013.png](src/main/resources/screens-cyber/Cybers013.png)

## Change Password
![Cybers014.png](src/main/resources/screens-cyber/Cybers014.png)

## Success notification
![Cybers015.png](src/main/resources/screens-cyber/Cybers015.png)


## Your Friends
![Cybers016.png](src/main/resources/screens-cyber/Cybers016.png)

## All Members 
![Cybers017.png](src/main/resources/screens-cyber/Cybers017.png)

## Friendship Invitations
![Cybers018.png](src/main/resources/screens-cyber/Cybers018.png)


## Your Posts
![Cybers020.png](src/main/resources/screens-cyber/Cybers020.png)

## Post Page
![Cybers022.png](src/main/resources/screens-cyber/Cybers022.png)

## Post Form
![Cybers021.png](src/main/resources/screens-cyber/Cybers021.png)

## Comment Form
![Cybers023.png](src/main/resources/screens-cyber/Cybers023.png)

## Admin Dashboard
![Cybers027.png](src/main/resources/screens-cyber/Cybers027.png)

## All Members
![Cybers024.png](src/main/resources/screens-cyber/Cybers024.png)

## All Posts
![Cybers025.png](src/main/resources/screens-cyber/Cybers025.png)

## All Comments
![Cybers026.png](src/main/resources/screens-cyber/Cybers026.png)

## Project Management using Jira
![jira.png](src/main/resources/img/Jira.png)
