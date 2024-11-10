# CSE326-project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Volunteer Recruitment</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f8ff; 
        }

        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1em 0;
        }

        .header-image {
            width: 100%;
            height: auto;
            margin-bottom: 20px;
        }

        nav {
            margin: 0;
            padding: 0.5em 0;
            background-color: #333;
        }

        nav a {
            color: white;
            padding: 14px 20px;
            text-decoration: none;
            display: inline-block;
            transition: background-color 0.3s; /* Smooth hover transition */
        }

        nav a:hover {
            background-color: #555; /* Darker shade for hover */
            color: white;
        }

        #about {
            background: linear-gradient(135deg, #e0f7fa, #f1f8e9);
            padding: 40px;
            text-align: left;
            border-radius: 8px;
            margin: 20px auto;
            max-width: 800px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        #about h2 {
            font-size: 2em;
            color: #0073e6;
            margin-bottom: 20px;
            text-align: center;
            position: relative;
        }
        #about h2::after {
            content: "";
            width: 80px;
            height: 3px;
            background: #0073e6;
            display: block;
            margin: 10px auto 0;
        }
        #about p {
            font-size: 1.1em;
            line-height: 1.6;
            color: #333;
            margin-bottom: 20px;
        }

        section {
            padding: 20px;
            margin: 20px;
            background-color: #fff; /* White background for sections */
            border-radius: 10px; /* Rounded corners */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Shadow for depth */
        }

        .opportunities-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }

        .opportunity {
            background-color: #e7ffe7; /* Light green background for cards */
            padding: 15px;
            margin: 10px;
            border: 1px solid #4CAF50; /* Green border */
            border-radius: 10px;
            flex: 0 1 calc(30% - 20px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15); /* Deeper shadow */
            transition: transform 0.3s; /* Smooth hover effect */
        }

        .opportunity:hover {
            transform: translateY(-5px); /* Lift on hover */
        }

        .signup-btn {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            border-radius: 5px; /* Rounded button */
            transition: background-color 0.3s; /* Smooth hover transition */
        }

        .signup-btn:hover {
            background-color: #45a049; /* Darker shade for button hover */
        }

        .form-popup {
            display: none;
            position: fixed;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            border: 2px solid #4CAF50;
            border-radius: 10px;
            padding: 20px;
            background-color: white;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            z-index: 1001;
            width: 300px;
        }

        .form-popup input,
        .form-popup textarea {
            width: calc(100% - 20px);
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .form-popup .form-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .form-popup label {
            flex: 1;
            margin-right: 10px;
        }

        .form-popup button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            margin-top: 10px;
            width: 100%;
            border-radius: 5px; /* Rounded button */
            transition: background-color 0.3s; /* Smooth hover transition */
        }

        .form-popup button:hover {
            background-color: #45a049; /* Darker shade for button hover */
        }

        .gallery {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }

        .gallery img {
            margin: 10px;
            width: 150px;
            height: 150px;
            border-radius: 5px;
            transition: transform 0.3s; /* Smooth hover transition */
        }

        .gallery img:hover {
            transform: scale(1.05); /* Zoom effect on hover */
        }

        .contact {
            text-align: center;
            padding: 20px;
            background-color: #333;
            color: white;
            border-radius: 10px; /* Rounded corners */
        }

        

        .reviews {
            background-color: #fff; /* White background for reviews */
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Shadow for depth */
        }

        .review {
            margin: 10px 0;
            border-bottom: 1px solid #ccc;
            padding-bottom: 10px;
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: #333;
            color: white;
            margin-top: 20px;
            border-radius: 10px; /* Rounded corners */
        }
        /* Footer Styling */
footer {
  background-color: #333;
  color: white;
  text-align: left; /* Align text to the left */
  padding: 20px 0;
  position: relative;
  bottom: 0;
  width: 100%;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  padding-left: 20px; /* Add padding on the left side */
}

.social-media-links {
  display: flex;
  justify-content: flex-start; /* Align items to the left */
  gap: 20px;
  margin-top: 10px;
}

.social-media-links a:hover {
  transform: scale(1.1);
  color: #0077b5; /* LinkedIn Blue */
}


.social-icon {
  width: 40px;
  height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  transition: background-color 0.3s ease;
}

.social-icon img {
  width: 25px;
  height: 25px;
}

.social-icon:hover {
  background-color: #555;
}

.social-icon.facebook-icon {
  background-color: #3b5998;
}

.social-icon.instagram-icon {
  background-color: #e4405f;
}

.social-icon.twitter-icon {
  background-color: #1da1f2;
}

.social-icon.linkedin-icon {
  background-color: #0077b5;
}

    </style>
</head>
<body>

    <header>
        <img src="DALL·E 2024-11-10 15.49.57 - Homepage image for a volunteer recruitment website, showing a diverse group of volunteers wearing casual clothes and happy expressions. Background inc.jpg" alt="Volunteer Header Image" class="header-image"> <!-- Add your header image here -->
    </header>

    <nav>
        <a href="#about">About Us</a>
        <a href="#opportunities">Volunteer Opportunities</a>
        <a href="#gallery">Gallery</a>
        <a href="#contact">Contact Us</a>
    </nav>

    <section id="about">
        <h2>About Us</h2>
        <p>We are a community-driven organization committed to making a positive impact in society. Our mission is to bring together volunteers and provide them with opportunities to contribute to meaningful social causes. We strive to create a better world through collective efforts, whether it's by helping communities in need, conserving the environment, or supporting various social welfare initiatives.</p>
    </section>

    <section id="opportunities">
        <h2>Volunteer Opportunities</h2>
        <div class="opportunities-container">
            <div class="opportunity">
                <h3>Food Distribution</h3>
                <p>Help distribute food to the needy in your community.</p>
                <button class="signup-btn" onclick="document.getElementById('form1').style.display='block'">Sign Up</button>
                <div id="form1" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name1">Your Name:</label>
                        <input type="text" id="name1" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email1">Your Email:</label>
                        <input type="email" id="email1" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason1">Reason:</label>
                        <textarea id="reason1" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form1').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Community Cleanup</h3>
                <p>Join us for a day of cleaning up parks and public spaces.</p>
                <button class="signup-btn" onclick="document.getElementById('form2').style.display='block'">Sign Up</button>
                <div id="form2" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name2">Your Name:</label>
                        <input type="text" id="name2" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email2">Your Email:</label>
                        <input type="email" id="email2" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason2">Reason:</label>
                        <textarea id="reason2" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form2').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Mentoring Youth</h3>
                <p>Guide and inspire the next generation through mentorship.</p>
                <button class="signup-btn" onclick="document.getElementById('form3').style.display='block'">Sign Up</button>
                <div id="form3" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name3">Your Name:</label>
                        <input type="text" id="name3" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email3">Your Email:</label>
                        <input type="email" id="email3" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason3">Reason:</label>
                        <textarea id="reason3" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form3').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Event Organization</h3>
                <p>Help organize community events to bring people together.</p>
                <button class="signup-btn" onclick="document.getElementById('form4').style.display='block'">Sign Up</button>
                <div id="form4" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name4">Your Name:</label>
                        <input type="text" id="name4" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email4">Your Email:</label>
                        <input type="email" id="email4" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason4">Reason:</label>
                        <textarea id="reason4" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form4').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Animal Shelter</h3>
                <p>Assist in caring for and finding homes for animals in need.</p>
                <button class="signup-btn" onclick="document.getElementById('form5').style.display='block'">Sign Up</button>
                <div id="form5" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name5">Your Name:</label>
                        <input type="text" id="name5" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email5">Your Email:</label>
                        <input type="email" id="email5" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason5">Reason:</label>
                        <textarea id="reason5" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form5').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Fundraising</h3>
                <p>Help raise funds for local charities and community projects.</p>
                <button class="signup-btn" onclick="document.getElementById('form6').style.display='block'">Sign Up</button>
                <div id="form6" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name6">Your Name:</label>
                        <input type="text" id="name6" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email6">Your Email:</label>
                        <input type="email" id="email6" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason6">Reason:</label>
                        <textarea id="reason6" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form6').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Environmental Awareness</h3>
                <p>Help spread awareness about environmental issues and initiatives.</p>
                <button class="signup-btn" onclick="document.getElementById('form7').style.display='block'">Sign Up</button>
                <div id="form7" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name7">Your Name:</label>
                        <input type="text" id="name7" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email7">Your Email:</label>
                        <input type="email" id="email7" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason7">Reason:</label>
                        <textarea id="reason7" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form7').style.display='none'">Submit</button>
                </div>
            </div>
            <div class="opportunity">
                <h3>Senior Assistance</h3>
                <p>Provide companionship and assistance to elderly community members.</p>
                <button class="signup-btn" onclick="document.getElementById('form8').style.display='block'">Sign Up</button>
                <div id="form8" class="form-popup">
                    <h3>Registration Form</h3>
                    <div class="form-row">
                        <label for="name8">Your Name:</label>
                        <input type="text" id="name8" placeholder="Your Name" required>
                    </div>
                    <div class="form-row">
                        <label for="email8">Your Email:</label>
                        <input type="email" id="email8" placeholder="Your Email" required>
                    </div>
                    <div class="form-row">
                        <label for="reason8">Reason:</label>
                        <textarea id="reason8" placeholder="Why do you want to volunteer?" required></textarea>
                    </div>
                    <button onclick="document.getElementById('form8').style.display='none'">Submit</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Added Reviews Section -->
    <section class="reviews">
        <h2>Volunteer Reviews</h2>
        <div class="review">
            <strong>Jane Doe:</strong>
            <p>"Volunteering has changed my life. I met amazing people and made a difference!"</p>
        </div>
        <div class="review">
            <strong>John Smith:</strong>
            <p>"The community cleanup was a rewarding experience. I encourage everyone to get involved!"</p>
        </div>
        <div class="review">
            <strong>Emily Johnson:</strong>
            <p>"Being a mentor has been one of the most fulfilling experiences of my life."</p>
        </div>
        <!-- More reviews can be added here -->
    </section>

    <section id="gallery">
        <h2>Gallery</h2>
        <div class="gallery">
            <img src="v1.jpg" alt="Photo 1">
            <img src="v2.jpg" alt="Photo 2">
            <img src="v3.jpg" alt="Photo 3">
            <img src="v4.jpg" alt="Photo 4">
            <img src="v5.jpg" alt="Photo 4">
            <img src="auroville-india-21st-september-2019-world-cleanup-day-children-and-teachers-clean-the-area-all-around-the-school-picking-up-all-the-garbage-2ATMNHN.jpg" alt="Photo 4">
        </div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>If you have any questions, feel free to reach out!</p>
        <div class="contact">
            <p><i class="fas fa-envelope"></i> Email us at: <a href="https://mail.google.com/mail/u/2/#inbox" target="_blank">VolunteerLpu@gmail.com</a></p>
            <p><i class="fas fa-phone-alt"></i> Call us at: +91 9876512345</p>
            <div class="footer-container">
                Follow us on social media:
                <div class="social-media-links">
                  <a href="https://facebook.com/your-volunteer-recruitment-page" target="_blank" class="social-icon facebook-icon">
                    <img src="facebok logo.jpg" alt="Facebook">
                  </a>
                  <a href="https://www.instagram.com/volunteerslpu/" target="_blank" class="social-icon instagram-icon">
                    <img src="instagram logo.jpg" alt="Instagram">
                  </a>
                  <a href="https://twitter.com/your-volunteer-recruitment-page" target="_blank" class="social-icon twitter-icon">
                    <img src="twitter.jpg" alt="Twitter">
                  </a>
                  <a href="https://linkedin.com/your-volunteer-recruitment-page" target="_blank" class="social-icon linkedin-icon">
                    <img src="linkedin-logo-linkedin-symbol-linkedin-icon-free-free-vector.jpg" alt="LinkedIn">
                  </a>
                </div>
                
              </div>
        </div>
    </section>

    <!-- Footer Section with Social Media Links -->
<footer>
    <p>&copy; 2024 Volunteer Recruitment</p>
  </div>
</footer>

    <script>
        // Close form popup on click outside of the form
        window.onclick = function(event) {
            var forms = document.querySelectorAll('.form-popup');
            forms.forEach(function(form) {
                if (event.target === form) {
                    form.style.display = 'none';
                }
            });
        };
    </script>
    
</body>
</html>
