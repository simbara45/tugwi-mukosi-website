<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>News & Events - Tugwi Mukosi Secondary School</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
        }

        body {
            background-color: #f9fafb;
            color: #1e293b;
            line-height: 1.6;
        }

        /* header / navigation (same as main site) */
        .top-bar {
            background-color: #2e7d32;
            color: white;
            padding: 0.5rem 5%;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            font-size: 0.9rem;
            border-bottom: 3px solid #ffffff;
        }

        .contact-info span {
            margin-right: 1.8rem;
        }

        .contact-info i {
            margin-right: 0.4rem;
            color: #ffffff;
        }

        .social-icons a {
            color: white;
            margin-left: 1rem;
            transition: color 0.2s;
            font-size: 1rem;
        }

        .social-icons a:hover {
            color: #f5f5f5;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.8rem 5%;
            background-color: white;
            box-shadow: 0 4px 12px rgba(46,125,50,0.1);
            flex-wrap: wrap;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo img {
            height: 70px;
            width: auto;
            max-width: 200px;
            object-fit: contain;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            font-weight: 500;
        }

        .nav-links a {
            text-decoration: none;
            color: #1e293b;
            transition: color 0.2s;
            font-size: 1.1rem;
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: #2e7d32;
        }

        .btn-enrol {
            background-color: #2e7d32;
            color: white !important;
            padding: 0.6rem 1.8rem;
            border-radius: 40px;
            font-weight: 600;
            border: 2px solid #2e7d32;
            transition: all 0.2s;
        }

        .btn-enrol:hover {
            background-color: transparent;
            color: #2e7d32 !important;
        }

        /* Page Header */
        .page-header {
            background: linear-gradient(130deg, #1b5e20 0%, #2e7d32 100%);
            color: white;
            padding: 3rem 5%;
            text-align: center;
        }

        .page-header h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .page-header p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto;
            opacity: 0.9;
        }

        /* News Articles */
        .news-container {
            padding: 4rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .news-article {
            background: white;
            border-radius: 30px;
            margin-bottom: 3rem;
            box-shadow: 0 10px 30px -10px rgba(46,125,50,0.2);
            overflow: hidden;
            border-left: 6px solid #2e7d32;
        }

        .news-header {
            padding: 2rem 2rem 1rem;
        }

        .news-date {
            color: #2e7d32;
            font-weight: 600;
            font-size: 1rem;
            display: block;
            margin-bottom: 0.5rem;
        }

        .news-title {
            font-size: 2rem;
            color: #2e7d32;
            margin-bottom: 0.5rem;
        }

        .news-meta {
            color: #64748b;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .news-image {
            width: 100%;
            height: 300px;
            background-size: cover;
            background-position: center;
        }

        .news-content {
            padding: 2rem;
        }

        .news-content h3 {
            color: #2e7d32;
            margin: 1.5rem 0 1rem;
        }

        .news-content p {
            margin-bottom: 1.2rem;
            color: #334155;
        }

        .news-content ul, .news-content ol {
            margin-left: 2rem;
            margin-bottom: 1.2rem;
        }

        .back-button {
            display: inline-block;
            background-color: #2e7d32;
            color: white;
            text-decoration: none;
            padding: 0.8rem 2rem;
            border-radius: 40px;
            margin: 2rem 0;
            font-weight: 600;
            transition: background 0.2s;
        }

        .back-button:hover {
            background-color: #1b5e20;
        }

        .back-button i {
            margin-right: 0.5rem;
        }

        /* Footer */
        footer {
            background-color: #1b5e20;
            color: #ffffff;
            padding: 3rem 5% 1rem;
            margin-top: 2rem;
        }

        .footer-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
            justify-content: space-between;
        }

        .footer-col {
            flex: 1 1 200px;
        }

        .footer-col h4 {
            color: white;
            margin-bottom: 1.2rem;
            font-size: 1.2rem;
            border-bottom: 2px solid #ffffff;
            padding-bottom: 0.5rem;
        }

        .footer-col p, .footer-col a {
            color: #e0e0e0;
            text-decoration: none;
            display: block;
            margin-bottom: 0.7rem;
            transition: color 0.2s;
        }

        .footer-col a:hover {
            color: #ffffff;
            padding-left: 5px;
        }

        .footer-logo {
            margin-bottom: 1rem;
        }

        .footer-logo img {
            height: 60px;
            width: auto;
            max-width: 180px;
            object-fit: contain;
            background-color: white;
            padding: 8px;
            border-radius: 10px;
        }

        .copyright {
            text-align: center;
            border-top: 1px solid #2e7d32;
            margin-top: 3rem;
            padding-top: 1.5rem;
            color: #ffffff;
        }

        @media (max-width: 800px) {
            .nav-links {
                display: none;
            }
            .page-header h1 {
                font-size: 2.2rem;
            }
            .news-title {
                font-size: 1.6rem;
            }
        }
    </style>
</head>
<body>
    <!-- top contact bar (same as homepage) -->
    <div class="top-bar">
        <div class="contact-info">
            <span><i class="fas fa-phone-alt"></i> +263 775 493 621</span>
            <span><i class="fas fa-envelope"></i> tugwimukosi2026@gmail.com</span>
            <span><i class="fas fa-map-marker-alt"></i> P.O. Box 3244, Ngundu, Chivi, Masvingo</span>
        </div>
        <div class="social-icons">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-whatsapp"></i></a>
        </div>
    </div>

    <!-- main navigation -->
    <nav>
        <div class="logo">
            <img src="https://i.postimg.cc/mgrJZmxN/logo.jpg" alt="Tugwi Mukosi Secondary School Logo">
        </div>
        <div class="nav-links">
            <a href="index.html">Home</a>
            <a href="#">About</a>
            <a href="#">Academics</a>
            <a href="#">Admissions</a>
            <a href="news.html" class="active">News</a>
            <a href="#">Contact</a>
        </div>
        <a href="#" class="btn-enrol">Enrol now</a>
    </nav>

    <!-- Page Header -->
    <section class="page-header">
        <h1>School News & Events</h1>
        <p>Stay updated with the latest happenings at Tugwi Mukosi Secondary School</p>
    </section>

    <!-- News Articles -->
    <div class="news-container">
        <!-- Cultural Day Article -->
        <article class="news-article">
            <div class="news-header">
                <span class="news-date">📅 March 15, 2025</span>
                <h2 class="news-title">Cultural Day Celebration 2025</h2>
                <div class="news-meta">
                    <i class="fas fa-user"></i> By: Culture Committee | 
                    <i class="fas fa-tag"></i> Event, Culture
                </div>
            </div>
            <div class="news-image" style="background-image: linear-gradient(145deg, #2e7d32, #ffffff); background-blend-mode: overlay; background-color: #c8e6c9;"></div>
            <div class="news-content">
                <p>On March 15, 2025, Tugwi Mukosi Secondary School came alive with vibrant colors, rhythmic drums, and joyful singing as we celebrated our annual Cultural Day. The event, held under the theme "Our Culture, Our Heritage," showcased the rich diversity and talent of our students.</p>
                
                <h3>Highlights of the Day</h3>
                <ul>
                    <li><strong>Traditional Dances:</strong> Students performed traditional dances from various Zimbabwean cultures, including Jerusarema, Mbakumba, and Muchongoyo. The crowd was especially captivated by the Form 2 students' energetic performance.</li>
                    <li><strong>Cultural Fashion Show:</strong> Learners modeled traditional attire representing different ethnic groups, explaining the significance of each garment.</li>
                    <li><strong>Storytelling Session:</strong> Elders from the local community shared folk tales and proverbs, emphasizing moral values and our cultural heritage.</li>
                    <li><strong>Traditional Cuisine:</strong> Parents and teachers prepared traditional dishes including sadza, mopane worms, groundnuts, and various wild fruits for everyone to taste.</li>
                </ul>

                <h3>Competition Winners</h3>
                <p>The inter-house competition was fierce but friendly. Here are the winners:</p>
                <ul>
                    <li><strong>Best Traditional Dance:</strong> Mukuvisi House</li>
                    <li><strong>Best Cultural Display:</strong> Runde House</li>
                    <li><strong>Best Traditional Attire:</strong> Tokwe House</li>
                    <li><strong>Overall Winners:</strong> Mukuvisi House</li>
                </ul>

                <h3>Message from the Headmaster</h3>
                <p>"Our Cultural Day was a resounding success," said Mr. Chikwanha, the Headmaster. "It is heartwarming to see our young ones embracing their heritage with such pride and enthusiasm. This is exactly what our motto 'Our Culture, Our Heritage' means – preserving who we are while we pursue academic excellence."</p>

                <p>We thank all parents, teachers, and community members who made this day possible. Your support makes events like these memorable for our children.</p>

                <p><strong>Photos from the event will be available in the school gallery next week.</strong></p>
            </div>
        </article>

        <!-- First Graduation Ceremony -->
        <article class="news-article">
            <div class="news-header">
                <span class="news-date">📅 April 30, 2025</span>
                <h2 class="news-title">First Graduation Ceremony - Class of 2025</h2>
                <div class="news-meta">
                    <i class="fas fa-user"></i> By: Academic Office | 
                    <i class="fas fa-tag"></i> Graduation, Achievement
                </div>
            </div>
            <div class="news-image" style="background-image: linear-gradient(145deg, #1b5e20, #81c784); background-blend-mode: overlay; background-color: #a5d6a7;"></div>
            <div class="news-content">
                <p>Tugwi Mukosi Secondary School will celebrate a historic milestone on April 30, 2025 – our very first graduation ceremony! We are proud to honor our pioneer Form 4 class who will be completing their O-Level education.</p>

                <h3>Ceremony Details</h3>
                <ul>
                    <li><strong>Date:</strong> Wednesday, April 30, 2025</li>
                    <li><strong>Time:</strong> 9:00 AM - 2:00 PM</li>
                    <li><strong>Venue:</strong> School Assembly Hall</li>
                    <li><strong>Theme:</strong> "Laying Foundations, Building Futures"</li>
                </ul>

                <h3>Program Schedule</h3>
                <ol>
                    <li><strong>9:00 AM:</strong> Arrival and Registration of Guests</li>
                    <li><strong>9:30 AM:</strong> Procession of Graduands and Staff</li>
                    <li><strong>10:00 AM:</strong> Opening Prayer and National Anthem</li>
                    <li><strong>10:15 AM:</strong> Welcome Address by Headmaster, Mr. Chikwanha</li>
                    <li><strong>10:30 AM:</strong> Guest of Honor Speech - District Schools Inspector</li>
                    <li><strong>11:00 AM:</strong> Presentation of Graduates</li>
                    <li><strong>12:00 PM:</strong> Special Awards and Prizes</li>
                    <li><strong>12:30 PM:</strong> Vote of Thanks by Head Girl and Head Boy</li>
                    <li><strong>1:00 PM:</strong> Lunch and Entertainment</li>
                </ol>

                <h3>Graduating Class Statistics</h3>
                <ul>
                    <li><strong>Total Graduates:</strong> 85 students</li>
                    <li><strong>Subjects Offered:</strong> Mathematics, English, Science, History, Geography, Shona, Agriculture, Commerce</li>
                    <li><strong>University-bound:</strong> Many graduates have applied to Form 5 programs across Masvingo province</li>
                </ul>

                <h3>Special Awards Categories</h3>
                <ul>
                    <li>Best Overall Student</li>
                    <li>Best in Sciences</li>
                    <li>Best in Humanities</li>
                    <li>Best in Agriculture</li>
                    <li>Best in Sports</li>
                    <li>Most Improved Student</li>
                    <li>Leadership Award</li>
                    <li>Cultural Ambassador Award</li>
                </ul>

                <p><strong>All parents, guardians, and community members are cordially invited to attend this historic event. Please RSVP by April 25, 2025 through the school office.</strong></p>
            </div>
        </article>

        <!-- Sports Day -->
        <article class="news-article">
            <div class="news-header">
                <span class="news-date">📅 May 20, 2025</span>
                <h2 class="news-title">Annual Sports Day 2025</h2>
                <div class="news-meta">
                    <i class="fas fa-user"></i> By: Sports Department | 
                    <i class="fas fa-tag"></i> Sports, Competition
                </div>
            </div>
            <div class="news-image" style="background-image: linear-gradient(145deg, #2e7d32, #a5d6a7); background-blend-mode: overlay; background-color: #c8e6c9;"></div>
            <div class="news-content">
                <p>Get ready for a day of athletic excellence! The Tugwi Mukosi Secondary School Annual Sports Day will be held on May 20, 2025 at the school sports ground. This year, all four houses will compete for the coveted Sports Trophy.</p>

                <h3>Events Lineup</h3>
                <ul>
                    <li><strong>Track Events:</strong> 100m, 200m, 400m, 800m, 1500m, 4x100m relay</li>
                    <li><strong>Field Events:</strong> Long jump, High jump, Shot put, Discus</li>
                    <li><strong>Team Sports:</strong> Football (soccer), Netball, Volleyball</li>
                    <li><strong>Traditional Games:</strong> Nhodo, Dhunduru, Tsoro</li>
                </ul>

                <h3>House Competition</h3>
                <p>The four houses competing are:</p>
                <ul>
                    <li><strong>Mukuvisi House</strong> (Green) - Current champions</li>
                    <li><strong>Runde House</strong> (White)</li>
                    <li><strong>Tokwe House</strong> (Green & White stripes)</li>
                    <li><strong>Save House</strong> (White with green trim)</li>
                </ul>

                <h3>Schedule</h3>
                <ul>
                    <li><strong>8:00 AM:</strong> Opening Ceremony - March Past</li>
                    <li><strong>8:30 AM:</strong> Track Events (Heats)</li>
                    <li><strong>10:30 AM:</strong> Field Events</li>
                    <li><strong>12:00 PM:</strong> Lunch Break</li>
                    <li><strong>1:30 PM:</strong> Team Sports Matches</li>
                    <li><strong>3:00 PM:</strong> Finals (Track Events)</li>
                    <li><strong>4:00 PM:</strong> Prize Giving and Closing</li>
                </ul>

                <h3>Preparation Tips for Athletes</h3>
                <ul>
                    <li>Train regularly with your house team</li>
                    <li>Eat healthy and stay hydrated</li>
                    <li>Get enough rest the night before</li>
                    <li>Wear proper sports shoes</li>
                    <li>Wear your house colors with pride!</li>
                </ul>

                <p><strong>Parents and community members, come cheer for your favorite house! Food and drinks will be available for purchase.</strong></p>
            </div>
        </article>

        <!-- Parent-Teacher Conference -->
        <article class="news-article">
            <div class="news-header">
                <span class="news-date">📅 June 10, 2025</span>
                <h2 class="news-title">Parent-Teacher Conference - Term 2</h2>
                <div class="news-meta">
                    <i class="fas fa-user"></i> By: Administration | 
                    <i class="fas fa-tag"></i> Parents, Academic
                </div>
            </div>
            <div class="news-image" style="background-image: linear-gradient(145deg, #ffffff, #2e7d32); background-blend-mode: overlay; background-color: #e8f5e9;"></div>
            <div class="news-content">
                <p>The Term 2 Parent-Teacher Conference will be held on June 10, 2025. This is an important opportunity for parents to meet with teachers, discuss student progress, and strengthen the partnership between home and school.</p>

                <h3>Conference Details</h3>
                <ul>
                    <li><strong>Date:</strong> Tuesday, June 10, 2025</li>
                    <li><strong>Time:</strong> 2:00 PM - 6:00 PM</li>
                    <li><strong>Venue:</strong> School Classrooms (by department)</li>
                    <li><strong>Format:</strong> One-on-one meetings with subject teachers</li>
                </ul>

                <h3>What to Expect</h3>
                <ul>
                    <li>Review your child's Term 2 progress reports</li>
                    <li>Discuss strengths and areas for improvement</li>
                    <li>Learn about upcoming exams and assignments</li>
                    <li>Meet all subject teachers in one afternoon</li>
                    <li>Get strategies to support learning at home</li>
                </ul>

                <h3>Teacher Availability by Department</h3>
                <ul>
                    <li><strong>Languages (English, Shona):</strong> Rooms 1-3</li>
                    <li><strong>Sciences (Math, Biology, Chemistry):</strong> Rooms 4-7</li>
                    <li><strong>Humanities (History, Geography):</strong> Rooms 8-9</li>
                    <li><strong>Practical (Agriculture, Commerce):</strong> Rooms 10-11</li>
                </ul>

                <h3>Tips for a Productive Conference</h3>
                <ol>
                    <li>Come with specific questions about your child's progress</li>
                    <li>Bring a pen and paper to take notes</li>
                    <li>Ask how you can support learning at home</li>
                    <li>Discuss any concerns early in the term</li>
                    <li>Arrive early to avoid long queues</li>
                </ol>

                <h3>Important Dates After Conference</h3>
                <ul>
                    <li><strong>June 15-30:</strong> Revision week</li>
                    <li><strong>July 1-12:</strong> End of Term Exams</li>
                    <li><strong>July 15:</strong> Last day of Term 2</li>
                    <li><strong>September 2:</strong> First day of Term 3</li>
                </ul>

                <p><strong>Attendance is strongly encouraged. If you cannot attend, please contact the class teacher to schedule an alternative meeting.</strong></p>
            </div>
        </article>

        <a href="index.html" class="back-button"><i class="fas fa-arrow-left"></i> Back to Homepage</a>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div class="footer-col">
                <div class="footer-logo">
                    <img src="https://i.postimg.cc/mgrJZmxN/logo.jpg" alt="Tugwi Mukosi Secondary School Logo">
                </div>
                <p><i class="fas fa-map-marker-alt"></i> P.O. Box 3244, Ngundu<br>Chivi, Masvingo, Zimbabwe</p>
                <p><i class="fas fa-phone-alt"></i> +263 775 493 621</p>
                <p><i class="fas fa-envelope"></i> tugwimukosi2026@gmail.com</p>
            </div>
            <div class="footer-col">
                <h4>Quick links</h4>
                <a href="index.html">Home</a>
                <a href="#">About</a>
                <a href="#">Academics</a>
                <a href="#">Admissions</a>
                <a href="news.html">News</a>
                <a href="#">Contact</a>
            </div>
            <div class="footer-col">
                <h4>Our programs</h4>
                <a href="#">Form 1-4 (O-Level)</a>
                <a href="#">Form 5-6 (A-Level)</a>
                <a href="#">Cultural studies</a>
                <a href="#">Sports academy</a>
                <a href="#">Agriculture</a>
            </div>
            <div class="footer-col">
                <h4>Stay connected</h4>
                <p>Get updates on school news and events.</p>
                <div class="newsletter">
                    <input type="email" placeholder="Your email">
                    <button><i class="fas fa-paper-plane"></i></button>
                </div>
            </div>
        </div>
        <div class="copyright">
            &copy; 2025 Tugwi Mukosi Secondary School. All rights reserved. <br>
            <span style="font-size: 0.8rem; color: #a5d6a7;">"Our Culture Our Heritage"</span>
        </div>
    </footer>
</body>
</html>
