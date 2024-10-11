---
layout: essay
type: essay
title: "The UI Odyssey"
# All dates must be YYYY-MM-DD format!
date: 2024-10-10
published: true
labels:
  - UI Framework 
  - Bootstrap5
  - PMP
---


-------------------------------------------

## UI Frameworks + Application

User Interface (UI) Frameworks are collections of ready-to-use parts, styles, and tools that make it easier to build user interfaces for web applications. They help developers to create apps in a quick and efficient manner without them having to start from scratch. Regardless of your background, understanding UI frameworks can be incredibly beneficial. For those interested in starting a business, investing in a well-designed website is crucial. A user-friendly interface can increase reputation and improve overall user experience, which’ll attract more customers. 

However, the challenge lies in the need to regularly update the website in order to stay current with trends, technological advances and customer’s expectations. Choosing to withhold updates may lead to a decline in user engagements and credibility. Rather than creating an impressive preliminary website, consider starting off with the basic foundations and slowly build towards more complex features with each update. Essentially, it should foster good habits of continuous improvement.

This approach will lead to long-term success. While the process may be difficult at times, even frustrating, as long as they maintain that passion for learning and adapting, the fruits of their hard earned effort will flourish. Furthermore, their business will stand out amongst the competition as they constantly work towards gradual improvement.  


## My Experience

When I first learned about UI frameworks through Bootstrap 5, I found it easy at first to connect with the concepts learned from HTML and CSS which made the syntax straight forwards. However, that opinion quickly changed as the practice WODs and actual WODs had me constantly switching between the display and VSCode. It became a cycle of hunting down the anomalies, then modifying the code until it was somewhat similar or identical to the example provided. 

Through this experience, I learned that it takes a lot of repetition and practice to understand web development. Each adjustment had taught me something new and I found myself slowly appreciating the many wondrous features that Bootstrap 5 contained. Whenever I received a “Did Not Finish” (DNF) on the WODS, it was disappointing but managed to motivate me to push harder and improve. These challenges became more exciting as the obstacles seemed too difficult to solve, but every failure had brought me closer to success. Becoming a skilled developer is more than just acquiring technical skills, it’s about building resilience and possessing a resilient love for learning. 

```
index.html
<head>
   <base href="https://www.jadedynastyhawaii.com/">
   <meta charset="utf-8">
   <meta name="robots" content="index, follow">
   <meta name="keywords" content="Roast Duck, Ginger Chicken">
   <meta name="description" content="Jade Dynasty Seafood Restaurant on the 4th floor of the Ala Moana Shopping Center">
   <title>Jade Dynasty Seafood Restaurant</title>
   <link rel="icon" href="/templates/jade/favicon.ico">
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">


   <style>
       body {
           background-color: #f8f9fa;
       }
       #header {
           background-color: #8B0000;
           padding: 1rem 0;
           box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
       }
       #header .navbar {
           margin: 0;
       }
       .nav-link {
           color: #ffffff !important;
           transition: color 0.3s;
           text-decoration: none;
       }
       .nav-link:hover {
           color: #000000 !important;
       }
       #slideshow img {
           width: 100%;
           height: auto;
       }
       #menu-title, #menu-recommendations {
           font-size: 1.5rem;
           color: gold;
           margin-bottom: 0.75rem;
       }
       .menu-container {
           border: 4px solid #8B0000;
           padding: 1rem;
           border-radius: 0.5rem;
           background-color: #8B0000;
           color: #ffffff;
       }
       .menu-link {
           color: #ffffff;
           text-decoration: none;
       }
       .menu-link:hover {
           text-decoration: underline;
       }
       ul {
           list-style-type: none;
           padding: 0;
       }
       li {
           margin-bottom: 1.5rem;
       }
       #footer {
           background-color: #ffffff;
           padding: 2rem 0;
           box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
       }
   </style>


   <script src="//code.jquery.com/jquery-1.11.0.min.js"></script>
   <script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
   <script src="/templates/jade/sbox/shadowbox.js"></script>
   <script>
       $(document).ready(function () {
           Shadowbox.init();
       });
   </script>
</head>


<body>
   <div class="container-fluid">
       <header id="header" class="d-flex justify-content-between align-items-center px-3">
           <div id="dyn_logo" class="h4 text-white">Jade Dynasty Seafood Restaurant</div>
           <nav class="navbar navbar-expand-lg navbar-light">
               <div class="collapse navbar-collapse" id="navbarNav">
                   <ul class="navbar-nav">
                       <li class="nav-item"><a class="nav-link" href="/">Home</a></li>
                       <li class="nav-item"><a class="nav-link" href="/about">About</a></li>
                       <li class="nav-item"><a class="nav-link" href="/press">Press</a></li>
                       <li class="nav-item"><a class="nav-link" href="/directions">Directions</a></li>
                       <li class="nav-item"><a class="nav-link" href="/contact">Contact Us</a></li>
                       <li class="nav-item dropdown">
                           <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">Social Media</a>
                           <ul class="dropdown-menu">
                               <li><a class="dropdown-item" href="https://www.facebook.com/" target="_blank">Facebook</a></li>
                               <li><a class="dropdown-item" href="https://www.instagram.com/" target="_blank">Instagram</a></li>
                               <li><a class="dropdown-item" href="https://twitter.com/" target="_blank">Twitter</a></li>
                               <li><a class="dropdown-item" href="https://www.youtube.com/" target="_blank">YouTube</a></li>
                           </ul>
                       </li>
                   </ul>
               </div>
           </nav>
       </header>


       <div id="slideshow" class="my-4">
           <img src="https://www.jadedynastyhawaii.com/images/stories/header/dyn_header.png" alt="Restaurant Slideshow">
       </div>


       <main class="mb-4">
           <div class="row">
               <div class="col-md-4 menu-container">
                   <h2 id="menu-title">Menus</h2>
                   <ul>
                       <li><a class="menu-link" href="/fathers-day">Father's Day</a></li>
                       <li><a class="menu-link" href="/dim-sum">Dim Sum</a></li>
                       <li><a class="menu-link" href="/dinner">Main Menu</a></li>
                       <li><a class="menu-link" href="/party-packages">Parties</a></li>
                   </ul>
                   <h3 id="menu-recommendations">Menu Recommendations</h3>
                   <ul>
                       <li>Garlic Cucumber with Jelly Fish...... $10.75</li>
                       <li>Honey Garlic Ribs...... $22.95</li>
                       <li>Deep-fried Oysters with Garlic in Lettuce Wrap (4 Pcs)...... $21.95</li>
                       <li>Crab Meat & Fish Maw Soup...... $22.95</li>
                       <li>Simmered Clams in Supreme Broth...... $22.75</li>
                       <li>Steamed Soft Tofu w/ Assorted Seafood & Veg. in Bamboo Steamer...... $19.75</li>
                       <li>Braised Tofu & Seafood in Hot Pot...... $20.95</li>
                       <li>Sautéed Fresh Scallop & Bamboo Fungus with Egg...... $23.95</li>
                       <li>Honey Walnut Shrimp...... $22.95</li>
                       <li>Dynasty Tea-Smoked Tiger Prawns...... $25.95</li>
                       <li>Stew Beef Brisket & Tendon in Hot Pot...... $23.95</li>
                       <li>Stir-fried Mixed Vegetable w/Cashew Nuts...... $16.75</li>
                       <li>Fried Rice with Pork, Vegetable & Shrimp Paste...... $19.50</li>
                       <li>Stir-Fried Vermicelli Noodle(Singapore Style)...... $17.95</li>
                       <li>Goji Berry Gelatin...... $4.50</li>
                   </ul>
               </div>
               <div class="col-md-8">
                   <div id="homeContent" class="p-3 border rounded bg-light">
                       <img class="img-fluid" src="/images/JDFrontPage.jpg" alt="Restaurant Interior">
                   </div>
               </div>
           </div>
       </main>


       <footer id="footer" class="text-center">
           <div class="container">
               <p class="mt-3">© 2024 Jade Dynasty Seafood Restaurant</p>
           </div>
       </footer>
   </div>


   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
```

```
style.css
.soc-icon {
   transition: box-shadow 0.3s ease, transform 0.3s ease;
}


.soc-icon:hover {
   box-shadow: 0 0 10px rgba(255, 255, 0, 1); /* Yellow glow */
   transform: scale(1.1); /* Slightly increase size */
}
```

For the Your Choice Assignment, I decided to recreate the [Jade Dynasty Seafood Restaurant](https://www.jadedynastyhawaii.com/)'s website, providing a more modern take on the website and more interactive and fun features.

Changes
---------
1. Adding a neat dark red header to match with the color scheme of Dark Red, White and Black
2. Incorporation a column of the far left with the original Menus section but adding in a new section called Menu Recommendations where the restraunt may add their specials or popular dishes to attract customers attention rather immediately.
3. Getting rid of repetitive information such as the two phone numbers and the footer with three social medias.  I just kept their trademark.

