<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; display: flex; flex-direction: column; height: 100vh; }
        header { background-color: #333; color: #fff; padding: 15px; text-align: center; }
        .container { display: flex; flex: 1; background-color: #f4f4f4; }
        .sidebar { width: 200px; background-color: #444; color: #fff; padding: 20px; }
        .main-content { flex: 1; padding: 20px; }
    </style>
</head>
<body>

    <header>
        <h1>Dashboard Header</h1>
    </header>

    <div class="container">
        <nav class="sidebar">
            <p>Menu Item 1</p>
            <p>Menu Item 2</p>
        </nav>
        <main class="main-content">
            <h2>Welcome to the Dashboard</h2>
            <p>Here is where your main content will go.</p>
        </main>
    </div>

</body>
</html>
