# Sports Salaries

## Description

Provide a short description explaining the what, why, and how of your project. Use the following questions as a guide:



- What was your motivation?
- Why did you build this project? (Note: the answer is not "Because it was a homework assignment.")
- What problem does it solve?
- What did you learn?

## Table of Contents (Optional)

If your README is long, add a table of contents to make it easy for users to find what they need.

- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Installation

What are the steps required to install your project? Provide a step-by-step description of how to get the development environment running.



* Create a `customer_db` database in pgAdmin 4, and then create the following two tables within the database:
  * A `premise` table that contains the `id`, `premise_name`, and `county_id` columns.
  * A `county` table that contains the `id`, `county_name`, `license_count`, and `county_id` columns.
  * Make sure to assign a primary key, as Pandas will not be able to do so.
* In Jupyter Notebook, perform all ETL steps.
* **Extraction**
  * Put each CSV into a Pandas DataFrame.
* **Transform**
  * Copy _only_ the columns you need into a new DataFrame.
  * Rename the columns to match the tables created in the database.
  * Handle any duplicates.
    * **Hint:** Some locations have the same name, but each license number is unique.
  * Set the index to the previously created primary key.
* **Load**
  * Create a connection to the database.
  * Check for a successful connection to the database, and confirm that the tables have been created.
  * Append DataFrames to tables. Be sure to use the index that was set earlier.
* Confirm that the **Load** was successful by querying the database.

## Usage

Provide instructions and examples for use. Include screenshots as needed.

To add a screenshot, create an `assets/images` folder in your repository and upload your screenshot to it. Then, using the relative filepath, add it to your README using the following syntax:

    ```md
    ![alt text](assets/images/screenshot.png)
    ```

## Credits

List your collaborators, if any, with links to their GitHub profiles.

If you used any third-party assets that require attribution, list the creators with links to their primary web presence in this section.

If you followed tutorials, include links to those here as well.

## License

The last section of a high-quality README file is the license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, refer to [https://choosealicense.com/](https://choosealicense.com/).

---
