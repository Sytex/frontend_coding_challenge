# Sytex coding challenge 🎯

This repository holds a coding challenge for devs applying for frontend jobs @ [Sytex](https://sytex.io).

## Context

In this coding challenge, we will provide you with a real (albeit very diluted) business use case. The objective is that you design an UI to consume and show forms provided by a set of dummy APIs.

## The challenge!

In Sytex, a Form (think Google Forms) is used to gather information in the field. Our users would go to (sometimes _very_) remote locations to do some type of installation, improvements, upgrades or maintenance in the field. You can picture someone driving to the middle of the Atacama desert to repair a solar panel, or to a Brazilian _morro_ in Rio to install a new 5G cell.

During and after the work is done, data must be gathered to make sure the job was done correctly, and to inform the rest of the organization about the status and results.

Forms are based on a template. The template is the set of questions (form entries) that will need to be answered in the field. For example, the questions for the worker repairing a solar panel would be very different that for the worker installing a brand new 5G cell.

Entries are grouped, so that the form can be presented in a way that makes sense to the end user. For example, the form for the worker repairing a solar panel would have a group for the "General Information", and another group for the "Solar Panel Information". The form for the worker installing a brand new 5G cell would have a group for the "General Information", and another group for the "5G Cell Information".

### Objectives

We will provide mocked example of a couple of templates. The coding challenge consists in UI views that will allow the user to:

- View a list of forms and search by code and/or description.
- Select a form and view the structure of the selected form in friendly and understandable way.
- Be able to answer entries with appropriate validations and sanitizations

A `Form` contains a set of entries and groups. Each `Entry` has some metadata, and an `input_type`.

Their `input_type` represents the action the user needs to do to answer ("fill") them:

**input_type:** `1`

- This is a "Text Input" `Entry`.
- `answer` is a `String`.
- The end user would answer it using a text field.

**input_type:** `2`

- This is an "Options" `Entry`.
- `answer` is a `String` with the value of the selected option.
- The end user would answer it using a set of radio buttons or select list.

**input_type:** `3`

- This is a "Yes/No" `Entry`.
- `answer` is a `boolean`.
- The end user would answer it by pressing a button with either a "Yes" or a "No" label.

## What we expect

You can go for whatever you think it's the best solution for this assignment, both code and UI design! Just a couple of pointers:

- Use [Angular framework](https://angular.dev) (TypeScript) as the main programming language.
- Use any data persistence (memory included) as long as the objectives are met.

We'll check for these things in order of importance:

- Whether the solution embraces standard software development patterns and practices.
- A good UI/UX approach.

## Must have's

- Usage of latest Angular features such as signals and computed expressions
- Clean code
- Clean architecture

## Nice to haves

- State management implementing BloC pattern (You will find a brief example of how we implement it at Sytex in this repo)
- Test coverage
- Correct use of css selectors and stylesheets

As you may be subject to time constrains while doing this assignment, we expect you to choose what to prioritize accordingly.

## What you'll need to do

1. Clone (do not fork) the repository.
2. Understand the provided code.
3. Implement UI/UX to complete form's answers with corresponding validations, and display the form data with
   entries and answers.
4. Upload your code to a new repository
   - do not create a fork
   - do not create a pull request
5. [Send us the link](mailto:front@sytex.io) to your repository with the solution - if you don't like the idea of your solution to be publicly available make sure to create a private repository and invite [juanjo-ferrero](https://github.com/juanjo-ferrero), [adolfobushi](https://github.com/adolfobushi).

## Questions?

If you have any questions regarding this assignment or need to review some ideas, let us know within an issue in your repository and we'll answer promptly! Alternatively you can [send us an email](mailto:front@sytex.io).

# frontend_coding_challenge
