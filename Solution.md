1. Project structure
Create a folder named Assignment-8.1 with these two files:


text
Assignment-8.1/
│
├── index.html
└── style.css
2. HTML file — index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard Layout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="dashboard">

        <!-- Header -->
        <header class="header">
            <h2>My Dashboard</h2>
            <p>Welcome back, Admin!</p>
        </header>

        <!-- Sidebar -->
        <aside class="sidebar">
            <h3>Menu</h3>
            <ul>
                <li>Dashboard</li>
                <li>Analytics</li>
                <li>Users</li>
                <li>Reports</li>
                <li>Settings</li>
            </ul>
        </aside>

        <!-- Main Content -->
        <main class="main-content">
            <h2>Dashboard Overview</h2>

            <div class="cards">

                <div class="card">
                    <h3>Total Users</h3>
                    <p>1,250</p>
                </div>

                <div class="card">
                    <h3>Total Sales</h3>
                    <p>₹45,000</p>
                </div>

                <div class="card">
                    <h3>Orders</h3>
                    <p>320</p>
                </div>

                <div class="card">
                    <h3>Revenue</h3>
                    <p>₹75,000</p>
                </div>

            </div>
        </main>

    </div>

</body>
</html>
3. CSS file — style.css

css

/* Basic Styling */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f6f9;
}

/* Outer Dashboard Grid */
.dashboard {
    display: grid;

    grid-template-columns: 220px 1fr;
    grid-template-rows: 80px 1fr;

    min-height: 100vh;
}

/* Header */
.header {
    grid-column: 1 / 3;
    background-color: #2563eb;
    color: white;

    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 20px;
}

/* Sidebar */
.sidebar {
    background-color: #1e293b;
    color: white;
    padding: 25px;
}

.sidebar h3 {
    margin-bottom: 20px;
}

.sidebar ul {
    list-style: none;
}

.sidebar li {
    padding: 15px 5px;
    border-bottom: 1px solid #475569;
    cursor: pointer;
}

/* Main Content */
.main-content {
    padding: 30px;
}

.main-content h2 {
    margin-bottom: 25px;
    color: #1e293b;
}

/* Statistics Cards Grid */
.cards {
    display: grid;

    grid-template-columns: repeat(2, 1fr);

    gap: 20px;
}

/* Individual Cards */
.card {
    background-color: white;
    padding: 30px;
    border-radius: 10px;

    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);

    text-align: center;
}

.card h3 {
    color: #64748b;
    margin-bottom: 15px;
}

.card p {
    color: #2563eb;
    font-size: 28px;
    font-weight: bold;
}

/* Responsive Design */
@media (max-width: 600px) {
    .dashboard {
        grid-template-columns: 1fr;
        grid-template-rows: 80px auto 1fr;
    }

    .header {
        grid-column: 1;
    }

    .sidebar {
        padding: 15px;
    }

    .sidebar ul {
        display: flex;
        flex-wrap: wrap;
        gap: 15px;
    }

    .cards {
        grid-template-columns: 1fr;
    }
}
4. Expected dashboard design
My Dashboard

Welcome back, Admin!

Menu

Dashboard

Analytics

Users

Reports

Settings

Dashboard Overview

Total Users

1,250
Total Sales

₹45,000
Orders

320
Revenue

₹75,000
5. CSS Grid properties used
CSS Property

Purpose

display: grid

Creates a grid layout

grid-template-columns

Defines column sizes

grid-template-rows

Defines row sizes

grid-column

Controls column placement

gap

Adds space between cards

min-height

Sets minimum dashboard height

repeat(2, 1fr)

Creates two equal columns

6. How to run the project
Open the project folder in VS Code.

Create index.html and style.css.

Paste the respective code into each file.

Save both files.

Open index.html in your browser (or use Live Server).

Inspect the layout and CSS Grid properties using browser Developer Tools (F12).

7. Submission checklist

Dashboard webpage (index.html)

CSS file (style.css)

Header created

Sidebar and main content created

Four statistic cards added

CSS Grid properties implemented

Gaps added between cards

Browser layout inspected