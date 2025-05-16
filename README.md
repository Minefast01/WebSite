<!doctype html>
<html lang="th">

<head>
    <meta charset="UTF-8" />
    <title>My Website with Sidebar</title>
    <style>
        body {
            margin: 0;
            font-family: sans-serif;
            display: flex;
            flex-direction: column;
            height: 100vh;
        }

        /* Navbar */
        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background-color: #ffffff;
            border-bottom: 1px solid #ccc;
            padding: 10px 20px;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            height: 60px;
            z-index: 1000;
        }

        .logo-container {
            display: flex;
            align-items: center;
            cursor: pointer;
        }

        .logo-container img {
            height: 32px;
            margin-right: 10px;
        }

        .logo-container span {
            font-size: 18px;
            font-weight: bold;
            color: #333;
        }

        /* Container ด้านล่าง navbar เก็บ Sidebar กับ Content */
        .main-container {
            display: flex;
            flex: 1;
            margin-top: 60px;
            /* เว้นช่องจาก navbar */
            height: calc(100vh - 60px);
            /* ความสูงเต็มลบ navbar */
        }

        /* Sidebar */
        .sidebar {
            width: 200px;
            background-color: #f7f7f7;
            border-right: 1px solid #ccc;
            padding: 20px;
            box-sizing: border-box;
        }

        /* เนื้อหาหลัก */
        .content {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
        }
    </style>
</head>

<body>

    <!-- Navbar -->
    <div class="navbar">
        <div class="logo-container" onclick="location.reload()">
            <img src="https://www.svgrepo.com/show/447724/online-test.svg" alt="Logo" />
            <span>My Website</span>
        </div>
    </div>

    <!-- ส่วนหลักด้านล่าง navbar -->
    <div class="main-container">
        <!-- Sidebar -->
        <div class="sidebar">
            <h3>Sidebar Menu</h3>
            <style>
                ul li a {
                    color: black;
                    /* สีดำ */
                    font-weight: bold;
                    /* ตัวหนา */
                    text-decoration: none;
                    /* เอาเส้นขีดใต้ลิงก์ออก */
                }

                /* เวลาวางเมาส์ ถ้าอยากให้ไม่มีเส้นขีดใต้ด้วย */
                ul li a:hover {
                    text-decoration: none;
                    color: black;
                    /* จะได้ไม่เปลี่ยนสี */
                }
            </style>

            <ul>
                <li><a href="#">Home</a></li><br>
                <li><a href="#">Profile</a></li>
            </ul>


        </div>

        <!-- เนื้อหาหลัก -->
        <div class="content">
            <h1>ยินดีต้อนรับสู่เว็บไซต์ของฉัน</h1>
            <p>นี่คือเนื้อหาหลักของเว็บไซต์ที่แสดงข้างๆ sidebar และไม่ทับ navbar ด้านบน</p>
            <p>คุณสามารถเพิ่มเนื้อหาได้ตามต้องการ</p>
        </div>
    </div>

</body>

</html>
