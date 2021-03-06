[![Maintainability](https://api.codeclimate.com/v1/badges/e3a4b7ce6158bc66ca58/maintainability)](https://codeclimate.com/github/Lambda-School-Labs/project-canopy-be/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/e3a4b7ce6158bc66ca58/test_coverage)](https://codeclimate.com/github/Lambda-School-Labs/project-canopy-be/test_coverage)

# API Documentation

- API documentation can be found here (https://documenter.getpostman.com/view/10583912/Szf27XLo?version=latest)

#### Backend deployed at [Heroku](https://projectcanopybackend.herokuapp.com) <br>

## Getting started

To get the server running locally:

- Clone this repo
- CD in project-canopy-be
- **npm install** to install all required dependencies
- **npm run server** to start the local server
- **npm test** to start server using testing environment

### Backend framework goes here

#### Node.js

- is designed to build scalable network applications
- ease of use

#### Express.js

- is a minimal and flexible framework
- provides a robust set of features for web applications

## Endpoints

### Data Routes

| Method | Endpoint      | Description                          |
| ------ | ------------- | ------------------------------------ |
| GET    | `/by/:filter` | Filters by country, habitat, or all. |

| Method | Endpoint | Description                       |
| ------ | -------- | --------------------------------- |
| POST   | `/`      | Returns Species Card Information. |

### DS Routes

#### Biodiversity Routes

| Method | Endpoint    | Description                          |
| ------ | ----------- | ------------------------------------ |
| GET    | `/`         | Returns all hotspot habitats.        |
| GET    | `/:country` | Returns hotspot habitats by country. |

#### Threats Routes

| Method | Endpoint            | Description                 |
| ------ | ------------------- | --------------------------- |
| GET    | `/`                 | Returns all threats.        |
| GET    | `/:habitat_code`    | Returns threats by habitat. |
| GET    | `/country/:country` | Returns threats by country. |

# Data Model

#### DATA

---

```
 "country": "Cameroon",
        "classes": [
            {
                "class": "AMPHIBIA",
                "speciesCount": 211,
                "threatenedCount": 56,
                "threatLevels": [
                    {
                        "rank": "Critically Endangered",
                        "count": 18
                    },
                    {
                        "rank": "Endangered",
                        "count": 25
                    },
                    {
                        "rank": "Vulnerable",
                        "count": 13
                    }
                ],
                "species": [
                    {
                        "className": "AMPHIBIA",
                        "country": "Cameroon",
                        "redlistCategory": "Endangered",
                        "scientificName": "Arthroleptis perreti",
                        "speciesName": "perreti",
                        "kingdomName": "ANIMALIA",
                        "phylumName": "CHORDATA"
                    }
```

#### BIODIVERSITY DATA

---

```
 {
        "habitat": "Forest - Subtropical / Tropical Moist Lowland",
        "count": 531
    }
```

#### THREATS DATA

---

```
{
        "name": "Small-holder farming",
        "count": 754
    }
```

## Actions

`countriesClasses(filter)` -> Returns countries by class

`habitatsClasses(filter)` -> Returns habitats by class

`allCountsByClass()` -> Returns all the counts by class

`speciesCardInformation(scientificName)` -> Returns species card information

## Environment Variables

In order for the app to function correctly, the user must set up their own environment variables.

create a .env file that includes the following:

\_ DB_ENV - set to "development" until ready for "production"

## Contributing

When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change.

Please note we have a [code of conduct](./code_of_conduct.md). Please follow it in all your interactions with the project.

### Issue/Bug Request

**If you are having an issue with the existing project code, please submit a bug report under the following guidelines:**

- Check first to see if your issue has already been reported.
- Check to see if the issue has recently been fixed by attempting to reproduce the issue using the latest master branch in the repository.
- Create a live example of the problem.
- Submit a detailed bug report including your environment & browser, steps to reproduce the issue, actual and expected outcomes, where you believe the issue is originating from, and any potential solutions you have considered.

### Feature Requests

We would love to hear from you about new features which would improve this app and further the aims of our project. Please provide as much detail and information as possible to show us why you think your new feature should be implemented.

### Pull Requests

If you have developed a patch, bug fix, or new feature that would improve this app, please submit a pull request. It is best to communicate your ideas with the developers first before investing a great deal of time into a pull request to ensure that it will mesh smoothly with the project.

Remember that this project is licensed under the MIT license, and by submitting a pull request, you agree that your work will be, too.

#### Pull Request Guidelines

- Ensure any install or build dependencies are removed before the end of the layer when doing a build.
- Update the README.md with details of changes to the interface, including new plist variables, exposed ports, useful file locations and container parameters.
- Ensure that your code conforms to our existing code conventions and test coverage.
- Include the relevant issue number, if applicable.
- You may merge the Pull Request in once you have the sign-off of two other developers, or if you do not have permission to do that, you may request the second reviewer to merge it for you.

### Attribution

These contribution guidelines have been adapted from [this good-Contributing.md-template](https://gist.github.com/PurpleBooth/b24679402957c63ec426).

## Documentation

See [Frontend Documentation](https://github.com/Lambda-School-Labs/project-canopy-fe).
See [DS Documentation](https://github.com/Lambda-School-Labs/project-canopy-ds)
