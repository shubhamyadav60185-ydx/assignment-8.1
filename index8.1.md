## 1. Aim

To create a basic, responsive dashboard webpage using CSS Grid Layout.

## 2. Objectives

- Create a dashboard header.
- Create a sidebar and main content area.
- Display four statistic cards in the dashboard.
- Use `display: grid` for the outer layout.
- Apply `grid-template-columns` and `grid-template-rows`.
- Use `gap` to add spacing between grid items.
- Make the dashboard responsive for different screen sizes.
- Inspect the grid layout using browser developer tools.

## 3. Technologies Used

- HTML5
- CSS3
- CSS Grid
- Media Queries
- Google Fonts

## 4. Project Structure

Create a folder named `assignment-8.1` with the following files:

```text
assignment-8.1/
├── index.html
└── style.css
```

## 5. Complete HTML Code

Create a file named `index.html` and paste the following code.

### index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta
        name="description"
        content="A responsive dashboard demonstrating CSS Grid Layout."
    >

    <title>Dashboard | Admin Panel</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link
        href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap"
        rel="stylesheet"
    >

    <link rel="stylesheet" href="style.css">
</head>

<body>

    <!-- Dashboard Outer Grid -->

    <div class="dashboard">

        <!-- Dashboard Header -->

        <header class="header">
            <a href="#dashboard" class="brand">
                <span class="brand-icon">D</span>
                DashBoard
            </a>

            <div class="header-search">
                <input
                    type="search"
                    placeholder="Search anything..."
                    aria-label="Search dashboard"
                >
            </div>

            <div class="header-profile">
                <div class="notification" aria-label="Notifications">
                    ♧
                </div>

                <div class="profile-avatar">SY</div>

                <div class="profile-info">
                    <strong>Shubham Yadav</strong>
                    <span>Administrator</span>
                </div>
            </div>
        </header>

        <!-- Sidebar -->

        <aside class="sidebar">
            <p class="sidebar-heading">MAIN MENU</p>

            <nav aria-label="Dashboard navigation">
                <ul class="sidebar-menu">

                    <li>
                        <a href="#dashboard" class="menu-link active">
                            <span class="menu-icon">▦</span>
                            Dashboard
                        </a>
                    </li>

                    <li>
                        <a href="#analytics" class="menu-link">
                            <span class="menu-icon">▥</span>
                            Analytics
                        </a>
                    </li>

                    <li>
                        <a href="#projects" class="menu-link">
                            <span class="menu-icon">▣</span>
                            Projects
                        </a>
                    </li>

                    <li>
                        <a href="#reports" class="menu-link">
                            <span class="menu-icon">▤</span>
                            Reports
                        </a>
                    </li>

                    <li>
                        <a href="#settings" class="menu-link">
                            <span class="menu-icon">⚙</span>
                            Settings
                        </a>
                    </li>

                </ul>
            </nav>

            <div class="sidebar-bottom">
                <div class="help-card">
                    <span class="help-icon">?</span>
                    <h3>Need Help?</h3>
                    <p>Contact our support team for assistance.</p>
                    <a href="mailto:support@example.com">
                        Contact Support →
                    </a>
                </div>
            </div>
        </aside>

        <!-- Main Content -->

        <main class="main-content" id="dashboard">

            <section class="welcome-section">
                <div>
                    <p class="eyebrow">OVERVIEW</p>
                    <h1>Dashboard</h1>
                    <p class="welcome-text">
                        Welcome back! Here is what's happening today.
                    </p>
                </div>

                <button
                    class="date-button"
                    type="button"
                    onclick="this.textContent = 'Today: ' + new Date().toLocaleDateString()"
                >
                    ◷ View Today's Date
                </button>
            </section>

            <!-- Statistics Cards -->

            <section class="stats-grid" aria-label="Statistics">

                <article class="stat-card" id="analytics">
                    <div class="stat-top">
                        <span class="stat-label">Total Revenue</span>
                        <span class="stat-icon revenue-icon">₹</span>
                    </div>

                    <h2>₹1,25,000</h2>

                    <p class="stat-change positive">
                        ↑ 12.5% <span>from last month</span>
                    </p>
                </article>

                <article class="stat-card">
                    <div class="stat-top">
                        <span class="stat-label">Total Users</span>
                        <span class="stat-icon users-icon">♙</span>
                    </div>

                    <h2>2,450</h2>

                    <p class="stat-change positive">
                        ↑ 8.2% <span>from last month</span>
                    </p>
                </article>

                <article class="stat-card" id="projects">
                    <div class="stat-top">
                        <span class="stat-label">Total Projects</span>
                        <span class="stat-icon projects-icon">▣</span>
                    </div>

                    <h2>156</h2>

                    <p class="stat-change positive">
                        ↑ 5.4% <span>from last month</span>
                    </p>
                </article>

                <article class="stat-card" id="reports">
                    <div class="stat-top">
                        <span class="stat-label">Pending Tasks</span>
                        <span class="stat-icon tasks-icon">◷</span>
                    </div>

                    <h2>24</h2>

                    <p class="stat-change negative">
                        ↓ 3.1% <span>from last month</span>
                    </p>
                </article>

            </section>

            <!-- Recent Activity and Progress -->

            <section class="content-grid">

                <article class="panel activity-panel">
                    <div class="panel-heading">
                        <div>
                            <h2>Recent Activity</h2>
                            <p>Latest updates from your dashboard</p>
                        </div>

                        <a href="#reports" class="view-link">View All</a>
                    </div>

                    <div class="activity-list">

                        <div class="activity-item">
                            <span class="activity-dot purple-dot"></span>
                            <div>
                                <h3>New project created</h3>
                                <p>Website Redesign project was created.</p>
                                <span class="activity-time">10 minutes ago</span>
                            </div>
                        </div>

                        <div class="activity-item">
                            <span class="activity-dot blue-dot"></span>
                            <div>
                                <h3>New user registered</h3>
                                <p>A new member joined the platform.</p>
                                <span class="activity-time">30 minutes ago</span>
                            </div>
                        </div>

                        <div class="activity-item">
                            <span class="activity-dot green-dot"></span>
                            <div>
                                <h3>Monthly report completed</h3>
                                <p>Your monthly report is ready to view.</p>
                                <span class="activity-time">1 hour ago</span>
                            </div>
                        </div>

                        <div class="activity-item">
                            <span class="activity-dot orange-dot"></span>
                            <div>
                                <h3>Task deadline approaching</h3>
                                <p>Review your upcoming tasks.</p>
                                <span class="activity-time">2 hours ago</span>
                            </div>
                        </div>

                    </div>
                </article>

                <article class="panel progress-panel">
                    <div class="panel-heading">
                        <div>
                            <h2>Project Progress</h2>
                            <p>Current project status</p>
                        </div>
                    </div>

                    <div class="progress-item">
                        <div class="progress-info">
                            <span>Website Redesign</span>
                            <strong>80%</strong>
                        </div>

                        <div class="progress-track">
                            <div class="progress-fill purple-fill"
                                 style="width: 80%"></div>
                        </div>
                    </div>

                    <div class="progress-item">
                        <div class="progress-info">
                            <span>Mobile Application</span>
                            <strong>65%</strong>
                        </div>

                        <div class="progress-track">
                            <div class="progress-fill blue-fill"
                                 style="width: 65%"></div>
                        </div>
                    </div>

                    <div class="progress-item">
                        <div class="progress-info">
                            <span>Marketing Campaign</span>
                            <strong>45%</strong>
                        </div>

                        <div class="progress-track">
                            <div class="progress-fill green-fill"
                                 style="width: 45%"></div>
                        </div>
                    </div>

                    <div class="progress-item">
                        <div class="progress-info">
                            <span>Customer Research</span>
                            <strong>90%</strong>
                        </div>

                        <div class="progress-track">
                            <div class="progress-fill orange-fill"
                                 style="width: 90%"></div>
                        </div>
                    </div>
                </article>

            </section>

            <!-- Footer -->

            <footer class="main-footer" id="settings">
                <p>© 2026 DashBoard Admin Panel. All rights reserved.</p>
                <p>Designed using HTML5, CSS3 and CSS Grid.</p>
            </footer>

        </main>

    </div>

</body>
</html>
```

## 6. Complete CSS Code

Create a file named `style.css` in the same folder and paste the following code.

### style.css

```css
/* =================================
   1. Global Styles
================================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: "Poppins", sans-serif;
    color: #1e293b;
    background-color: #f5f7fb;
    line-height: 1.6;
}

a {
    color: inherit;
    text-decoration: none;
}

button,
input {
    font: inherit;
}

button {
    cursor: pointer;
}

.dashboard {
    min-height: 100vh;
}

/* =================================
   2. Outer Dashboard Grid
================================= */

.dashboard {
    display: grid;
    grid-template-columns: 250px minmax(0, 1fr);
    grid-template-rows: 76px minmax(0, 1fr);
    grid-template-areas:
        "header header"
        "sidebar main";
}

/* =================================
   3. Header
================================= */

.header {
    grid-area: header;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 24px;
    padding: 0 30px;
    background-color: #ffffff;
    border-bottom: 1px solid #e8edf5;
}

.brand {
    display: flex;
    align-items: center;
    gap: 10px;
    flex-shrink: 0;
    color: #1e293b;
    font-size: 21px;
    font-weight: 700;
}

.brand-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 11px;
    background: linear-gradient(135deg, #6366f1, #8b5cf6);
    color: #ffffff;
    font-size: 22px;
}

.header-search {
    flex: 1;
    max-width: 380px;
}

.header-search input {
    width: 100%;
    padding: 11px 15px;
    border: 1px solid #e2e8f0;
    border-radius: 9px;
    outline: none;
    background-color: #f8fafc;
    color: #1e293b;
    font-size: 13px;
}

.header-search input:focus {
    border-color: #818cf8;
    box-shadow: 0 0 0 3px #eef2ff;
}

.header-profile {
    display: flex;
    align-items: center;
    gap: 13px;
}

.notification {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 38px;
    height: 38px;
    border-radius: 10px;
    background-color: #f1f5f9;
    color: #475569;
    font-size: 22px;
}

.profile-avatar {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: #e0e7ff;
    color: #4338ca;
    font-size: 13px;
    font-weight: 700;
}

.profile-info strong,
.profile-info span {
    display: block;
}

.profile-info strong {
    font-size: 12px;
}

.profile-info span {
    color: #94a3b8;
    font-size: 11px;
}

/* =================================
   4. Sidebar
================================= */

.sidebar {
    grid-area: sidebar;
    display: flex;
    flex-direction: column;
    min-width: 0;
    padding: 30px 18px;
    background-color: #ffffff;
    border-right: 1px solid #e8edf5;
}

.sidebar-heading {
    margin: 0 0 18px 12px;
    color: #94a3b8;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.5px;
}

.sidebar-menu {
    display: flex;
    flex-direction: column;
    gap: 8px;
    list-style: none;
}

.menu-link {
    display: flex;
    align-items: center;
    gap: 13px;
    padding: 12px;
    border-radius: 9px;
    color: #64748b;
    font-size: 13px;
    font-weight: 500;
    transition: all 0.2s ease;
}

.menu-link:hover {
    background-color: #f1f5f9;
    color: #4f46e5;
}

.menu-link.active {
    background-color: #eef2ff;
    color: #4f46e5;
    font-weight: 600;
}

.menu-icon {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 22px;
    font-size: 19px;
}

.sidebar-bottom {
    margin-top: auto;
    padding-top: 40px;
}

.help-card {
    padding: 18px 15px;
    border: 1px solid #e0e7ff;
    border-radius: 13px;
    background-color: #f5f7ff;
}

.help-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 30px;
    height: 30px;
    margin-bottom: 12px;
    border-radius: 9px;
    background-color: #e0e7ff;
    color: #4338ca;
    font-weight: 700;
}

.help-card h3 {
    margin-bottom: 6px;
    font-size: 13px;
}

.help-card p {
    margin-bottom: 12px;
    color: #64748b;
    font-size: 11px;
}

.help-card a {
    color: #4f46e5;
    font-size: 11px;
    font-weight: 600;
}

/* =================================
   5. Main Content
================================= */

.main-content {
    grid-area: main;
    display: flex;
    flex-direction: column;
    gap: 28px;
    min-width: 0;
    padding: 30px;
}

.welcome-section {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 18px;
}

.eyebrow {
    color: #6366f1;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.5px;
}

.welcome-section h1 {
    margin: 4px 0;
    font-size: 28px;
    line-height: 1.4;
}

.welcome-text {
    color: #94a3b8;
    font-size: 13px;
}

.date-button {
    padding: 10px 15px;
    border: 1px solid #e2e8f0;
    border-radius: 9px;
    background-color: #ffffff;
    color: #475569;
    font-size: 12px;
    transition: border-color 0.2s ease;
}

.date-button:hover {
    border-color: #818cf8;
}

/* =================================
   6. Statistics Cards Grid
================================= */

.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
}

.stat-card {
    min-width: 0;
    padding: 22px;
    border: 1px solid #e8edf5;
    border-radius: 14px;
    background-color: #ffffff;
    box-shadow: 0 3px 12px rgba(15, 23, 42, 0.025);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.stat-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 24px rgba(15, 23, 42, 0.06);
}

.stat-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 8px;
    margin-bottom: 18px;
}

.stat-label {
    color: #64748b;
    font-size: 12px;
}

.stat-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    width: 38px;
    height: 38px;
    border-radius: 11px;
    font-size: 20px;
    font-weight: 600;
}

.revenue-icon {
    background-color: #dcfce7;
    color: #15803d;
}

.users-icon {
    background-color: #dbeafe;
    color: #1d4ed8;
}

.projects-icon {
    background-color: #ede9fe;
    color: #6d28d9;
}

.tasks-icon {
    background-color: #ffedd5;
    color: #c2410c;
}

.stat-card h2 {
    margin-bottom: 10px;
    font-size: clamp(20px, 2vw, 27px);
    line-height: 1.3;
    overflow-wrap: anywhere;
}

.stat-change {
    font-size: 11px;
    font-weight: 600;
}

.stat-change span {
    color: #94a3b8;
    font-weight: 400;
}

.positive {
    color: #16a34a;
}

.negative {
    color: #ea580c;
}

/* =================================
   7. Recent Activity and Progress Grid
================================= */

.content-grid {
    display: grid;
    grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
    gap: 22px;
}

.panel {
    min-width: 0;
    padding: 24px;
    border: 1px solid #e8edf5;
    border-radius: 14px;
    background-color: #ffffff;
}

.panel-heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    margin-bottom: 25px;
}

.panel-heading h2 {
    font-size: 16px;
}

.panel-heading p {
    margin-top: 4px;
    color: #94a3b8;
    font-size: 11px;
}

.view-link {
    flex-shrink: 0;
    color: #4f46e5;
    font-size: 11px;
    font-weight: 600;
}

/* Recent Activity */

.activity-list {
    display: flex;
    flex-direction: column;
}

.activity-item {
    display: flex;
    align-items: flex-start;
    gap: 13px;
    padding: 15px 0;
    border-bottom: 1px solid #f1f5f9;
}

.activity-item:first-child {
    padding-top: 0;
}

.activity-item:last-child {
    padding-bottom: 0;
    border-bottom: none;
}

.activity-dot {
    flex-shrink: 0;
    width: 10px;
    height: 10px;
    margin-top: 6px;
    border-radius: 50%;
}

.purple-dot {
    background-color: #8b5cf6;
}

.blue-dot {
    background-color: #3b82f6;
}

.green-dot {
    background-color: #22c55e;
}

.orange-dot {
    background-color: #f97316;
}

.activity-item h3 {
    font-size: 12px;
}

.activity-item p {
    color: #64748b;
    font-size: 11px;
}

.activity-time {
    display: block;
    margin-top: 4px;
    color: #94a3b8;
    font-size: 10px;
}

/* Project Progress */

.progress-item {
    margin-bottom: 24px;
}

.progress-item:last-child {
    margin-bottom: 0;
}

.progress-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    margin-bottom: 10px;
    font-size: 11px;
}

.progress-info span {
    color: #475569;
}

.progress-info strong {
    color: #334155;
}

.progress-track {
    width: 100%;
    height: 8px;
    overflow: hidden;
    border-radius: 20px;
    background-color: #f1f5f9;
}

.progress-fill {
    height: 100%;
    border-radius: inherit;
}

.purple-fill {
    background-color: #8b5cf6;
}

.blue-fill {
    background-color: #3b82f6;
}

.green-fill {
    background-color: #22c55e;
}

.orange-fill {
    background-color: #f97316;
}

/* =================================
   8. Footer
================================= */

.main-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: auto;
    padding-top: 20px;
    border-top: 1px solid #e2e8f0;
    color: #94a3b8;
    font-size: 10px;
}

/* =================================
   9. Tablet Responsive Design
================================= */

@media (max-width: 1100px) {
    .dashboard {
        grid-template-columns: 210px minmax(0, 1fr);
    }

    .header {
        padding: 0 22px;
    }

    .main-content {
        padding: 24px;
    }

    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .content-grid {
        grid-template-columns: minmax(0, 1fr);
    }
}

/* =================================
   10. Mobile Responsive Design
================================= */

@media (max-width: 700px) {
    .dashboard {
        grid-template-columns: minmax(0, 1fr);
        grid-template-rows: auto auto minmax(0, 1fr);
        grid-template-areas:
            "header"
            "sidebar"
            "main";
    }

    .header {
        min-width: 0;
        flex-wrap: wrap;
        gap: 14px;
        padding: 16px 5%;
    }

    .brand {
        font-size: 18px;
    }

    .brand-icon {
        width: 35px;
        height: 35px;
        font-size: 18px;
    }

    .header-search {
        order: 3;
        flex: 1 1 100%;
        max-width: none;
    }

    .header-profile {
        gap: 8px;
    }

    .notification {
        display: none;
    }

    .profile-avatar {
        width: 34px;
        height: 34px;
    }

    .profile-info strong {
        font-size: 11px;
    }

    .profile-info span {
        font-size: 10px;
    }

    .sidebar {
        padding: 16px 5%;
        border-right: none;
        border-bottom: 1px solid #e8edf5;
    }

    .sidebar-heading,
    .sidebar-bottom {
        display: none;
    }

    .sidebar-menu {
        flex-direction: row;
        flex-wrap: wrap;
        gap: 8px;
    }

    .menu-link {
        gap: 6px;
        padding: 9px 10px;
        background-color: #f8fafc;
        font-size: 11px;
    }

    .menu-icon {
        width: auto;
        font-size: 15px;
    }

    .main-content {
        gap: 22px;
        padding: 22px 5%;
    }

    .welcome-section {
        align-items: flex-start;
    }

    .welcome-section h1 {
        font-size: 25px;
    }

    .date-button {
        font-size: 10px;
    }

    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 12px;
    }

    .stat-card {
        padding: 16px;
    }

    .stat-top {
        align-items: flex-start;
        gap: 8px;
    }

    .stat-label {
        font-size: 11px;
    }

    .stat-icon {
        width: 32px;
        height: 32px;
        font-size: 17px;
    }

    .stat-card h2 {
        font-size: 20px;
    }

    .stat-change {
        font-size: 10px;
    }

    .panel {
        padding: 18px;
    }

    .main-footer {
        flex-direction: column;
        align-items: flex-start;
    }
}

/* =================================
   11. Extra Small Screens
================================= */

@media (max-width: 380px) {
    .header-profile {
        gap: 6px;
    }

    .profile-info strong {
        max-width: 105px;
        overflow-wrap: anywhere;
    }

    .stats-grid {
        grid-template-columns: minmax(0, 1fr);
    }

    .stat-card {
        padding: 18px;
    }

    .welcome-section {
        flex-direction: column;
    }

    .date-button {
        align-self: flex-start;
    }

    .menu-link {
        padding: 8px;
        font-size: 10px;
    }

    .panel-heading h2 {
        font-size: 14px;
    }

    .activity-item p {
        overflow-wrap: anywhere;
    }
}
```

## 7. Explanation of CSS Grid Properties

| Property | Purpose |
|---|---|
| `display: grid` | Creates a CSS Grid container |
| `grid-template-columns` | Defines the columns of the layout |
| `grid-template-rows` | Defines the rows of the layout |
| `grid-template-areas` | Assigns named areas to the layout |
| `grid-area` | Places an element in a named grid area |
| `gap` | Adds spacing between grid items |
| `minmax(0, 1fr)` | Allows a track to shrink without forcing overflow |
| `repeat(4, minmax(0, 1fr))` | Creates four equally sized columns |

### Outer Dashboard Layout

```css
.dashboard {
    display: grid;
    grid-template-columns: 250px minmax(0, 1fr);
    grid-template-rows: 76px minmax(0, 1fr);
    grid-template-areas:
        "header header"
        "sidebar main";
}
```

This creates a two-column dashboard with a full-width header, a sidebar on the left, and main content on the right.

### Statistics Cards Layout

```css
.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
}
```

This displays four statistic cards in a row on large screens. Media queries change the layout to two columns on smaller screens and one column on extra-small screens.

## 8. How to Run the Project

1. Open Visual Studio Code.
2. Create the `assignment-8.1` folder.
3. Create `index.html` and `style.css`.
4. Paste the corresponding code into both files.
5. Save the files.
6. Right-click `index.html` and select **Open with Live Server**, or open the file directly in a browser.
7. Check the dashboard header, sidebar, statistic cards, activity section, progress section, and footer.

## 9. Browser Grid Inspection

1. Open the webpage in Google Chrome.
2. Right-click the page and choose **Inspect**.
3. Open the **Elements** panel.
4. Select the element with the class `dashboard`.
5. In the Styles panel, locate `display: grid`.
6. Use Chrome DevTools' grid overlay controls to inspect the columns, rows, and grid gaps.
7. Select `.stats-grid` and inspect its four-column layout.
8. Resize the browser to test the tablet and mobile layouts.

## 10. Expected Output

The webpage displays:

- A dashboard header with a logo, search field, notification icon, and profile.
- A sidebar containing Dashboard, Analytics, Projects, Reports, and Settings.
- Four statistic cards showing revenue, users, projects, and pending tasks.
- A recent activity panel.
- A project progress panel with progress bars.
- A footer with copyright information.
- A responsive layout that adapts to different screen sizes.

## 11. Result

Successfully created a responsive dashboard webpage using HTML5, CSS3, and CSS Grid. The project uses grid columns, rows, named grid areas, gaps, and media queries to organize the header, sidebar, statistic cards, main content, and footer.
