<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Water Safety</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Spartan:wght@400;700&display=swap');

        body {
            font-family: 'Spartan', sans-serif;
            background-image: url('pngegg.png'); /* Local image path */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            color: #333;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #ABF4FF; /* Updated header color */
            color: #333; /* Changed text color for better contrast */
            padding: 40px 20px; /* Increased padding for a larger header */
            display: flex; /* Use flexbox for layout */
            justify-content: center; /* Center elements horizontally */
            align-items: center; /* Center items vertically */
            position: relative; /* Needed to keep the logo on the left */
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        header img {
            height: 250px; /* Increased height of the logo */
            width: auto; /* Maintains aspect ratio */
            position: absolute; /* Allows the logo to remain on the left */
            left: 20px; /* Adjust position from the left */
        }

        header h1 {
            font-size: 48px; /* Increased font size for better visibility */
            margin: 0;
            text-align: center; /* Center the title text */
        }

        .container {
            margin: 20px auto;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 8px;
            max-width: 1000px; /* Increased max-width for better layout */
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            display: flex; /* Flexbox to align register form on the left */
            justify-content: space-between;
            align-items: flex-start; /* Align items to the top */
            flex-wrap: wrap; /* Allow wrapping on smaller screens */
        }

        h2 {
            margin-top: 0;
            font-size: 28px;
        }

        p {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 35px;
        }

        .content {
            flex: 1 1 60%; /* Adjusted flex properties for better responsiveness */
            margin-right: 20px; /* Add space between content and register form */
        }

        .register {
            flex: 1 1 35%; /* Takes up less space than the content */
            margin-top: 20px;
        }

        .register input {
            padding: 10px;
            font-size: 16px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%; /* Full width within the register container */
            box-sizing: border-box; /* Include padding and border in the element's total width and height */
        }

        .register button {
            background-color: rgba(0, 80, 115, 0.8);
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            width: 100%; /* Full width for the button */
            box-sizing: border-box; /* Include padding and border in the element's total width and height */
            margin-top: 10px;
            transition: background-color 0.3s ease;
        }

        .register button:hover {
            background-color: rgba(0, 63, 94, 0.8);
        }

        .contact {
            margin-top: 40px;
            text-align: center;
        }

        .contact p {
            font-size: 16px;
        }

        .thank-you {
            margin-top: 30px;
            text-align: center;
            color: rgba(0, 80, 115, 0.8);
            font-size: 20px;
            font-weight: bold;
            display: none;
        }

        /* Responsive Adjustments */
        @media (max-width: 768px) {
            header {
                flex-direction: column; /* Stack logo and title on mobile */
                align-items: flex-start; /* Align to the left on mobile */
                padding: 30px 20px; /* Adjust padding for smaller screens */
            }

            header img {
                position: static; /* Reset positioning for smaller screens */
                height: 200px; /* Slightly smaller on mobile */
                margin-bottom: 10px; /* Space below logo */
            }

            header h1 {
                font-size: 36px; /* Adjust font size for mobile */
                text-align: left; /* Align title to the left on mobile */
            }

            .container {
                flex-direction: column;
                align-items: center;
            }

            .content, .register {
                flex: 1 1 100%;
                margin-right: 0;
            }
        }
    </style>
    <script>
        function registerPhoneNumber() {
            const MotherPhone = document.getElementById('MotherPhone').value.trim();
            const FatherPhone = document.getElementById('FatherPhone').value.trim();
            const phoneRegex = /^\d{10}$/; // Example regex for 10-digit phone numbers

            if (MotherPhone && FatherPhone) {
                if (phoneRegex.test(MotherPhone) && phoneRegex.test(FatherPhone)) {
                    document.querySelector('.thank-you').style.display = 'block';
                    // Clear the input fields
                    document.getElementById('MotherPhone').value = '';
                    document.getElementById('FatherPhone').value = '';
                } else {
                    alert("Please enter valid 10-digit phone numbers.");
                }
            } else {
                alert("Please enter both the Mother and Father phone numbers.");
            }
        }
    </script>
</head>
<body>
    <header>
        <img src="Smart_Sensing-2-removebg-preview.png" alt="Smart Sensing Logo"> <!-- Add the logo here -->
        <h1>Smart Water Safety</h1>
    </header>
    <div class="container">
        <div class="content">
            <h2>Welcome to Smart Water Safety</h2>
            <p>Measuring water current is crucial in various fields such as environmental monitoring and maritime navigation. Understanding the speed and direction of water currents can help predict weather patterns, monitor aquatic ecosystems, and improve the safety and efficiency of marine operations.</p>
            <p>This project aims to design and develop a sensor-based system to measure the speed and direction of water currents, detect eddies, and also detect drowning cases. This project aims to maintain the safety and security of the community from water accidents, such as the 2019 incident in the Shaleela Sea in Abu Dhabi, where a father drowned while trying to save his son who was being swept away by the water current. Unfortunately, the father and son drowned and died in the water current.</p>
        </div>
        <div class="register">
            <input type="text" id="MotherPhone" placeholder="Enter Mother phone number">
            <input type="text" id="FatherPhone" placeholder="Enter Father phone number">
            <button onclick="registerPhoneNumber()">Register Phone Numbers</button>
        </div>
    </div>
    <div class="thank-you">
        Thank you! The phone numbers have been successfully registered.
    </div>
    <div class="contact">
        <p><strong>Contact Email:</strong> <a href="mailto:H00467844@hct.ac.ae">H00467844@hct.ac.ae</a></p>
        <p><strong>Location:</strong> <a href="https://www.google.com/maps/dir/24.3113152,54.6739013/@24.3110791,54.7434663,12z?entry=ttu&g_ep=EgoyMDI0MDkyMy4wIKXMDSoASAFQAw%3D%3D" target="_blank" rel="noopener noreferrer">HCT College B</a></p>
    </div>
</body>
</html>
