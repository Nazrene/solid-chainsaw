# Superheroes

## Introduction

Superheroes is for tracking superheroes and their superpowers. It will use Flask and SQLAlchemy .

## Features

- Get a list of superheroes and their details.
- Get each superheroes associated powers.
-   Get a list of powers and their descriptions.
- Update power descriptions.
- Create new associations between superheroes and their superpowers.

## Models

1. Class Hero: Represents a superhero and has attributes  `id`, `name`, and `super_name`.
2. Class POwer: Represents a superpower and has attributes  `id`, `name`, and `description`.
3. Class HeroPower: Represents the relationship between heroes and their powers. It has attributes `id`, `strength`, `power_id`, and `hero_id`.

### Relationships

- A `Hero` has many `Power`s .
- A `Power` has many `Hero`s .
- A `HeroPower` belongs to a `Hero` and a `Power`.

### Validations

- The `strength` in `HeroPower` must be one of: **'Strong', 'Weak', 'Average'**.
- The `description` in `Power` must be present and at least **20 characters long**.

## API Endpoints

The API supports the following routes:

### Heroes

- **GET /heroes**: Returns a list of all heroes.
- **GET /heroes/:id**: Returns details of a hero by ID.

### Powers

- **GET /powers**: Returns a list of all powers.
- **GET /powers/:id**: Returns details of a specific power by ID.
- **PATCH /powers/:id**: Updates an existing power description.
  
### Hero Powers

- **POST /hero_powers**: Creates a new association between a hero and a power.
