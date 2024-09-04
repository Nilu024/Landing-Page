# Landing-Page
Restaurant landing page. Valentina Elegance Bistro as title name of restaurant which contains is some information about menu and a form where you can reserve a table for your date also.

<!----HTML---->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Restaurant Landing Page</title>
    <link rel="stylesheet" type="text/css" href="style.css">
    <script type="text/javascript" src="script.js"></script>
</head>		
<body>
    <header>
        <div class="logo">Vintage Elegance Bistro</div>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#reservation" class="btn-reserve">Reserve a Table</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <video autoplay muted loop id="background-video">
            <source src="G:\Nilesh\Projects\Restaurant landing page\The Heavy Hitting Burger - Promo Video.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
        <h1>Welcome to Our Restaurant</h1>
        <p>Delicious food awaits you!</p>
        <a href="#menu" class="btn">View Menu</a>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>We are dedicated to providing the best dining experience with fresh ingredients and exceptional service.</p>
        <p>At our restaurant, we pride ourselves on providing a warm and inviting atmosphere for all our guests. Our facilities include a spacious dining area that comfortably accommodates both intimate dinners and larger gatherings. Enjoy our outdoor seating area, perfect for al fresco dining under the stars. We also offer a fully stocked bar featuring a curated selection of wines, craft beers, and signature cocktails. For families, we provide a dedicated kids' menu and a play area to keep the little ones entertained. Our state-of-the-art kitchen is equipped with the latest technology to ensure the freshest and highest quality meals, prepared by our skilled chefs. Whether you're here for a casual meal or a special occasion, we strive to make every visit memorable.</p>
    </section>

    <section id="menu">
        <h2>Our Menu</h2>
        <div class="menu-items">
            <div class="menu-item">
                <h3>Burger</h3>
                <p>₹150</p>
            </div>
            <div class="menu-item">
                <h3>Pasta</h3>
                <p>₹180</p>
            </div>
            <div class="menu-item">
                <h3>Salad</h3>
                <p>₹80</p>
            </div>
            <div class="menu-item">
                <h3>Dessert</h3>
                <p>₹100</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>Email: vintage@restaurant.com</p>
        <p>Phone: (123) 456-7890</p>
    </section>

    <section id="reservation">

        <form id="order-form">
        <h2>Choose Your Meal</h2>
        
        <div class="meal-selection">
            <label>
                <input type="radio" name="meal" value="pasta" data-price="12"> Pasta - $180
            </label>
            <label>
                <input type="radio" name="meal" value="burger" data-price="10"> Burger - $150
            </label>
            <label>
                <input type="radio" name="meal" value="pizza" data-price="15"> Pizza - $120
            </label>
        </div>
        
        <button type="submit">Place Order</button>
    </form>

    <div id="receipt" class="hidden">
        <h3>Bill Receipt</h3>
        <p id="selected-meal">Selected Meal: <span id="meal-name"></span></p>
        <p id="meal-price">Price: $<span id="price"></span></p>
    </div>
    
        <h2 class="table-reserve">Reserve a Table</h2>
        <form id="reservation-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <input type="date" required>
            <input type="time" required>
            <button type="submit" class="btn">Submit Reservation</button>
    
        </form>
    </section><br><br>

    <footer>
        <p>&copy; 2024 Restaurant Name. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>


<!-----CSS----->

* {
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
    color: ghostwhite;
}

header {
    background: #333;
    color: #fff;
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 1000;
}

header nav ul {
    list-style: none;
    padding: 0;
}

header nav ul li {
    display: inline;
    margin-left: 20px;
}

header nav ul li a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
}

header nav ul li a:hover {
    color: #e67e22;
}

.logo{
    color: #D5006D;
    font-size: 40px;
}

.hero {
    background: url('restaurant.jpg') no-repeat center center/cover;
    height: 400px;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    animation: fadeIn 1.5s ease-in;
}

.hero {
    position: relative;
    height: 400px;
    overflow: hidden;
}
.hero {
    position: relative;
    height: 100vh; /* Full height of the viewport */
    overflow: hidden; /* Hide overflow */
}

#background-video {
    position: fixed; /* Fixes the video in place */
    top: 50%; /* Center vertically */
    left: 50%; /* Center horizontally */
    min-width: 100%; /* Minimum width to cover the viewport */
    min-height: 100%; /* Minimum height to cover the viewport */
    width: auto; /* Maintain aspect ratio */
    height: auto; /* Maintain aspect ratio */
    z-index: -1; /* Place video behind text */
    transform: translate(-50%, -50%); /* Center the video */
    filter: blur(5px);
    object-fit: cover; /* Cover the entire area */
}

.hero h1, .hero p {
    position: relative; /* Ensure text is above the video */
    z-index: 1;
    color: #fff; /* Change text color for better visibility */
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.btn {
    background: #e67e22;
    color: #fff;
    padding: 15px 20px;
    text-decoration: none;
    border-radius: 5px;
    transition: background 0.3s;
}

.btn:hover {
    background: #d35400;
}

section {
    padding: 40px 20px;
    text-align: center;
    scroll-margin-top: 100px;
}

.menu-items {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    cursor: pointer;
}

.menu-item {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
    margin: 10px;
    width: 200px;
    transition: transform 0.3s;
}

.menu-item:hover {
    transform: scale(1.05);
}

footer {
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
}

#reservation {
    background: blur(10px);
    padding: 20px;
    border-top: 1px solid #ddd;
    border: 2px solid #00668d; /* Set the border color */
    border-radius: 30px; /* Optional: round the corners */
    padding: 20px; /* Space between the border and the form content */
    /*background-color: #f9f9f9; /* Optional: background color for the form */*/
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Optional: add a subtle shadow */
    max-width: 400px;
    margin: 20px auto;
}

#reservation-form {
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: 0 auto;
}

#reservation-form input {
    margin: 10px 0;
    padding: 10px;
     width: calc(100% - 22px); /* Full width minus padding */
    border: 1px solid #ccc;
    border-radius: 5px;
}

#reservation-form button {
    background: #d35400;
    color: #fff;
    border: none;
    padding: 10px;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s;
}

#reservation-form button:hover {
    background: #FA8072;
    color: #FF0000;
}


 .meal-selection {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        label {
            margin-right: 20px; /* Space between radio buttons */
            display: inline-block; /* Keep labels inline */
        }

        #receipt {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            background-color: #fff;
            border-radius: 5px;
        }

        .hidden {
            display: none; /* Hide the receipt initially */
        }


<!-----JavaScript----->

const form = document.getElementById('order-form');
     const receipt = document.getElementById('receipt');
        const mealName = document.getElementById('meal-name');
        const price = document.getElementById('price');

        form.addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent form submission

            const selectedMeal = form.querySelector('input[name="meal"]:checked');
            if (selectedMeal) {
                mealName.textContent = selectedMeal.value.charAt(0).toUpperCase() + selectedMeal.value.slice(1);
                price.textContent = selectedMeal.getAttribute('data-price');
                receipt.classList.remove('hidden'); // Show the receipt
            } else {
                alert('Please select a meal.');
            }
    });


document.getElementById('reservation-form').addEventListener('submit', function(event) {
event.preventDefault(); // Prevent the form from submitting

    // Get form data
    const name = this[0].value;
    const email = this[1].value;
    const date = this[2].value;
    const time = this[3].value;

    // Display a confirmation message
    alert(`Thank you, ${name}! Your reservation for ${date} at ${time} has been received.`);
    
    // Reset the form
    this.reset();
});
