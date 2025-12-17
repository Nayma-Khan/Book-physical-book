# Data Model for Physical AI and Humanoid Robotics Book

This document defines the structure of the content entities for the book.

## 1. Chapter

Represents a top-level section of the book.

-   **Fields**:
    -   `title` (string): The title of the chapter (e.g., "Introduction to Physical AI and Robotics").
    -   `summary` (string): A brief description of the chapter's content.
    -   `lessons` (array of Lesson): An ordered list of lessons within the chapter.
    -   `mini_project` (MiniProject): The concluding project for the chapter.
-   **Validation**:
    -   Must have exactly 3 lessons.
    -   Must have exactly 1 mini-project.

## 2. Lesson

Represents a single learning module within a chapter.

-   **Fields**:
    -   `title` (string): The title of the lesson (e.g., "What is Physical AI?").
    -   `content` (Markdown): The main body of the lesson.
    -   `diagrams` (array of string): A list of paths to image files for diagrams.
    -   `code_examples` (array of CodeExample): A list of code snippets.
-   **Validation**:
    -   Content must be written in Markdown.

## 3. Mini-Project

Represents the hands-on project at the end of a chapter.

-   **Fields**:
    -   `title` (string): The title of the project (e.g., "Hello, World!: Make a simulated robot arm wave.").
    -   `objective` (string): A clear statement of what the user will build.
    -   `steps` (array of Step): A list of steps to complete the project.
    -   `final_code` (string): The complete, working code for the project.
-   **Validation**:
    -   Must have a clear objective.

## 4. CodeExample

Represents a code snippet within a lesson.

-   **Fields**:
    -   `language` (string): The programming language (e.g., "python").
    -   `code` (string): The code snippet itself.
    -   `explanation` (string): A description of what the code does.

## 5. Step

Represents a single step in a mini-project.

-   **Fields**:
    -   `description` (Markdown): The instructions for the step.
    -   `code_snippet` (CodeExample, optional): An associated code snippet for the step.
