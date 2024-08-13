# MongoDB Student Records Database****

This repository contains a sample MongoDB database with 100 student records, which can be used for educational purposes, such as assignments and projects related to MongoDB. The data is stored in a JSON file named student_records.json.

## Contents

student_records.json: A JSON file containing 100 student records.
README.md: This file, explaining how to set up and use the database.

## Prerequisites

Before you begin, make sure you have the following:

- MongoDB: Installed locally or access to a MongoDB Atlas cluster.
- Mongosh: MongoDB Shell, which allows you to interact with your MongoDB database.

## Setup Instructions

### Step 1: Clone the Repository

First, clone the repository to your local machine:

git clone https://github.com/mouraleonardo/Student_Records_Database_Sample
cd Student_Records_Database_Sample

### Step 2: Import the JSON File into MongoDB Using Mongosh

You can import the student_records.json file into your MongoDB database using mongosh as follows:

**Open mongosh:**

`mongosh`

Switch to the desired database (or create it if it doesn't exist):

`use seneca_students`

Import the JSON data into the student_records collection:

    const fs = require('fs'); // Load the filesystem module
    
    const fileData = fs.readFileSync("<path_to_file>/student_records.json"); // Read the JSON file
    
    const jsonArray = JSON.parse(fileData); // Parse the JSON file content
    
    db.student_records.insertMany(jsonArray); // Insert the JSON data into the 'student_records' collection
    

## Step 3: Verify the Import

To verify that the data has been imported correctly, you can run:

    db.student_records.find().pretty()

This should display the documents within the student_records collection.
Usage

Once the database is set up, you can use it to practice various MongoDB features, including:

- Indexing/Search: Create indexes to optimize queries.
- Validation: Implement schema validation to enforce data integrity.
- Data API: Interact with the database using the MongoDB Data API.
- Drivers: Connect to the database using MongoDB drivers for various programming languages.
- Node.js: Build Node.js applications that interact with MongoDB.
- Charts: Visualize data using MongoDB Charts.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any questions or issues, feel free to open an issue in this repository or contact me at contact@mouraleonardo.com.