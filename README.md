# Schema Design for Adoption Website

## User Table

- **Primary Key**: UserID
- **Columns**:
  - UserID (Primary Key)
  - Username
  - Email
  - Password
  - ProfilePicture
  - Location
  - Contact Information
  - API Key/Token
  - Role (User, Admin, etc.)

## Pet Table

- **Primary Key**: PetID
- **Columns**:
  - PetID (Primary Key)
  - Name
  - Type (e.g., dog, cat, bird)
  - Breed
  - Age
  - Size
  - Description
  - Photos (possibly as references to image files)
  - Contact
  - Availability for Adoption (Boolean)


## User-Pet Relationship Table (Favorites, Adoption History, etc.)

- **Primary Key**: InteractionID
- **Columns**:
  - InteractionID (Primary Key)
  - UserID (Foreign Key referencing User.UserID)
  - PetID (Foreign Key referencing Pet.PetID)
  - InteractionType (e.g., Favorite, Adoption)
  - Timestamp

### Schema Overview

- The User and Pet tables have primary keys (UserID and PetID, respectively).
- The User-Pet Relationship table is used to establish many-to-many relationships between users and pets. It has foreign keys referencing both the User and Pet tables, allowing you to track interactions like favorites and adoption history.
- You can use the InteractionType column to distinguish between different types of interactions (e.g., favorite or adoption).
- Timestamps can be used to track when these interactions occurred.

This is a simplified textual representation. To create a visual representation using Crow's Foot notation, you would typically use specialized database design software or draw it out on paper or a digital drawing tool. The relationships in Crow's Foot notation would involve lines connecting the tables with crow's foot symbols at the ends indicating the "many" side of the relationship.
