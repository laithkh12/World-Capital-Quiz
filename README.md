# Capital City Quiz App

This is a simple quiz web application built with Node.js, Express, and PostgreSQL. The app presents a list of countries and asks the user to enter the capital city of each. The quiz data is retrieved from a PostgreSQL database.

## Features

- Displays a random country and prompts the user to enter its capital.
- Tracks the total score based on correct answers.
- Displays a final score at the end of the quiz.

## Prerequisites

- **Node.js** and **npm** installed on your machine
- **PostgreSQL** database server running locally
- **dotenv** for loading environment variables

## Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/capital-city-quiz.git
   cd capital-city-quiz
   ```

2. **Install dependencies

   ```bash
   npm install
   ```

3. **Create the PostgreSQL Database
   ```bash
   CREATE DATABASE world;
   \c world
   CREATE TABLE capitals (
      id SERIAL PRIMARY KEY,
      country VARCHAR(255) NOT NULL,
      capital VARCHAR(255) NOT NULL
   );
   ```

4. **Configure Environment Variables

```bash
DB_PASSWORD=your_password_here
```

5. **Run the App
```bash
npm start
```

## File Structure
1 - index.js: Main server file that sets up the Express app, connects to PostgreSQL, and handles quiz logic.
2 - index.ejs: Template file for the quiz interface, with fields for displaying the country, capturing the user's answer, and displaying the score.
3 - public/styles/main.css: (Optional) CSS file for styling the quiz page.

## Usage
1 - The app fetches a random country from the database and displays it.
2 - The user submits their answer for the capital city.
3 - The app checks if the answer is correct, updates the score, and moves to the next question.
