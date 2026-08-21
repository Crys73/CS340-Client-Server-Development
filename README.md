# CS340-Client-Server-Development
A project that applies database systems concepts and principles in the development of a client/server application with development of client-side code that interfaces with a database.

# Grazioso Salvare Animal Rescue Dashboard

## Project Overview
This project creates an interactive dashboard for *Grazioso Salvare* using data from the *Austin Animal Center*. The dashboard helps identify dogs that may be good candidates for different search‑and‑rescue roles.

Users can:
- Filter dogs by rescue type
- View matching records in a data table
- See a chart based on the selected data
- View the animal’s location on an interactive map

The dashboard connects to MongoDB using the reusable CRUD Python module I built in Project One. That module acts as the “database layer,” so the dashboard doesn’t need to know how MongoDB works internally.

## Technologies Used
- Python
- MongoDB / PyMongo
- Pandas
- Dash
- Plotly
- Dash Leaflet
- JupyterLab (Codio)

## How I Write Maintainable, Readable, and Adaptable Programs
I keep my programs maintainable by organizing the code into clear, separate parts instead of putting everything in one place. For example, the **AnimalShelter** class in my CRUD module handles all database operations--Create, Read, Update, and Delete. The dashboard simply uses those methods without needing to know how the database works behind the scenes.

This made Project Two much easier because I didn’t have to rewrite any database code. I reused the CRUD module from Project One, which saved time and kept the dashboard cleaner and easier to update.

The CRUD module can also be reused in future tools that need access to the same animal database--like admin dashboards, reporting tools, or automated scripts. Keeping the database logic separate makes the whole system easier to maintain and adapt when requirements change.

## How I Approach Problems as a Computer Scientist
I start by understanding the requirements and then break the problem into smaller steps. For this project, I looked at what Grazioso Salvare needed and figured out which data would help identify dogs for different rescue roles. Then I turned those needs into MongoDB queries and connected them to dashboard controls.

This project was different from earlier assignments because it wasn’t just about writing code--it was about building a tool someone could actually use. I had to think about how the database, the logic, and the user interface all worked together.

In future projects, I would follow the same approach:
- Understand the client’s needs
- Identify the data required
- Design the database and queries
- Build the application around that data
- Test each requirement individually

This helps ensure the final product actually solves the client’s problem.

## What Computer Scientists Do -- and Why It Matters
Computer scientists solve real‑world problems using technology, data, and logical thinking. In this project, I created a tool that helps Grazioso Salvare use their animal shelter data more effectively.

Instead of searching through hundreds of records manually, users can choose a rescue category and instantly see matching animals. The dashboard also shows a chart summarizing the results and a map showing each animal’s location.

This project shows how computer science can turn raw data into something useful--helping organizations make faster, better decisions. For Grazioso Salvare, this means identifying potential search‑and‑rescue dogs more efficiently and consistently.

## Project Structure
**CRUD_Python_Module.py**
Contains the reusable *AnimalShelter* class, which:
> - Connects to MongoDB
> - Inserts new records (*create()*)
> - Retrieves records (*read()*)
> - Updates records (*update()*)
> - Deletes records (*delete()*)
> - Automatically generates the next available *record_number*

**ProjectTwoDashboard.ipynb**
Contains the interactive dashboard. It:
> - Connects to MongoDB through the CRUD module
> - Retrieves animal records
> - Filters by rescue type
> - Displays an interactive data table
> - Generates a breed distribution pie chart
> - Shows an interactive map
> - Highlights selected table rows
> - Includes the Grazioso Salvare logo
> - Uses callbacks to connect dashboard components

## Key Takeaway
The biggest lesson from this project was the value of separating the database logic from the application logic. Reusing the CRUD module made the dashboard easier to build and showed how software components can be designed for reuse instead of being written for one‑time use.

This project strengthened my skills in Python, MongoDB, data visualization, interactive dashboards, and translating client requirements into a working solution.
