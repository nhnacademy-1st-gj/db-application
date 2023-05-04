# JPA Board

## Requirements:

- Implement using Spring MVC
- Write MockWebMvc test code for all URLs
- Use MyBatis for Data Access
- Validate input items on both client-side and server-side
- Users (regular users and administrators) input data via SQL

## Functions:

1. LOGIN
  - Provide login feature for users to enter ID and PASSWORD.
  - Login information should be kept in Session.
2. Contents of the Board (View, Register, Edit, Delete)
3. Comments on Board Contents (View, Register, Edit, Delete)

## Basic Functions

- All users can view the list of board contents.
  - The list of board contents includes number, title, writer, (editor), date created, and number of comments.
  - The list shows 20 items per page and can navigate to other pages.
- All users can view the contents of the board.
  - The board contents include number, title, content, writer, editor, date created, date modified, and comment list.
- Logged-in users can register board contents.
- Users who created board contents can modify or delete contents.
- Logged-in users can register comments on board contents.
- Administrators can modify all board contents.
- Administrators can delete all board contents.
- Administrators can restore deleted board contents.


## Additional Score 1 

- Users can upload files when registering board contents.
- Logged-in users can download files attached to board contents.
- Logged-in users can like board contents.
- Users who liked the contents can cancel their likes.

## Additional Score 2 

- Logged-in users can reply to board contents.
- Logged-in users can register replies to replies of board contents.
- The board list shows up to five levels of replies.

## dditional Score 3 

- Users who liked contents can view the list of board contents they liked.
- All users can search the board list by title.
- Use SQL's like in the search. Pay attention to the use of index depending on the position of the Wild Key(%).

## Additional Score 4 

- Defend against XSS attacks.
  - Use AbstractAnnotationConfigDispatcherServletInitializer.
- Display the number of views in the board list. The number of views is only added once for the same user who viewed it multiple times.
