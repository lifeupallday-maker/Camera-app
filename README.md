```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UniCam - Universal Security Camera Hub</title>
    <!-- Using Material Icons from CDN -->
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <style>
        /* CSS Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #4a6bff;
            --secondary: #6c757d;
            --dark: #212529;
            --light: #f8f9fa;
            --danger: #dc3545;
            --success: #28a745;
            --border-radius: 8px;
        }

        body {
            background-color: #f5f7fa;
            color: var(--dark);
            line-height: 1.6;
        }

        /* Main App Container */
        .app-container {
            display: flex;
            min-height: 100vh;
        }

        /* Sidebar Navigation */
        .sidebar {
            width: 250px;
            background: white;
            box-shadow: 2px 0 10px rgba(0,0,0,0.1);
            padding: 20px 0;
            position: fixed;
            height: 100vh;
            z-index: 100;
            transition: all 0.3s;
        }

        .sidebar-collapsed {
            width: 80px;
        }

        .sidebar-collapsed .nav-text {
            display: none;
        }

        .logo {
            text-align: center;
            padding: 0 20px 20px;
            border-bottom: 1px solid #eee;
            margin-bottom: 20px;
        }

        .logo h2 {
            font-size: 1.5rem;
            color: var(--primary);
        }

        .logo-icon {
            font-size: 2rem;
            color: var(--primary);
            display: none;
        }

        .sidebar-collapsed .logo-icon {
            display: block;
        }

        .sidebar-collapsed .logo-full {
            display: none;
        }

        .nav-menu {
            list-style: none;
        }

        .nav-item {
            padding: 10px 20px;
            margin: 5px 0;
            cursor: pointer;
            display: flex;
            align-items: center;
            border-radius: var(--border-radius);
            transition: all 0.2s;
        }

        .nav-item:hover {
            background-color: rgba(74, 107, 255, 0.1);
        }

        .nav-item.active {
            background-color: var(--primary);
            color: white;
        }

        .nav-icon {
            margin-right: 15px;
            font-size: 1.2rem;
        }

        .sidebar-collapsed .nav-icon {
            margin-right: 0;
        }

        /* Main Content Area */
        .main-content {
            flex: 1;
            margin-left: 250px;
            transition: all 0.3s;
        }

        .sidebar-collapsed + .main-content {
            margin-left: 80px;
        }

        /* Top Navigation Bar */
        .top-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 30px;
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 90;
        }

        .search-bar {
            display: flex;
            align-items: center;
            background: #f1f3f5;
            padding: 8px 15px;
            border-radius: 20px;
            width: 300px;
        }

        .search-bar input {
            border: none;
            background: transparent;
            outline: none;
            width: 100%;
            margin-left: 10px;
        }

        .user-actions {
            display: flex;
            align-items: center;
        }

        .notification-badge {
            position: relative;
            margin-right: 25px;
            cursor: pointer;
        }

        .badge {
            position: absolute;
            top: -5px;
            right: -5px;
            background: var(--danger);
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18 Camera-app
app that connects all home cameras
