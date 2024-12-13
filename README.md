# UPCI Project Docs

## Database design

![Mermaid design](https://mermaid.ink/svg/pako:eNqNVU1v2zAM_SuCzy5QYMAOuaVLgxXLgmBJdxhyUS06FmJJhj66GUn_-yhH_laA-mKLfKQeHyn5kmSKQbJIQK84PWkqjpLg82pAG3K5LfzDpW2MLyuy-9GbQTrR2A91BeSY_ARplU6JfwOkZMkEl8ekDzBWc3kia66N3VIBM8-G3nE8C8rLmXVXKAlbJ95Az33UmL9Ks-_UFHOnVjkvYccz6zS8_tr0CAv_LHniCuWoinoW-SKtVsxlliv5mzNQXfDHUd4-bjIs35ExfeMlt_VUy6Fvoql33xKgYz1wMGqhDSxhhasBZy6A7C3V9sDF1P4sWW_tSG7AGCVnXb6ZY31eOU190djnL48p-fo4bCyDjAtaoq48m-70pNQZlZttFex36geY1H9XmBHtqWKNAmGnsWaNnvusAOZKYDE9W99Y0zAHf5QSGy7PE5WwCdYZ1KiLTsk3JaoSbPNJZQYlWlvxOpV2tBZY3UylYI-o1Os3Kjp0YimUk3ZHOYsIEpKOi274B09fhssy1DYlaxy8CO2tsjznWTMZM-5DZ6SAcKOsP1VXw26YMNw5zcWQkgOe2tFAtqUOQ_p6O_63q-56fXhQl9jBXeAWBTVt6hG8G2wPEvQMcdhYIo_VkAF_7-GRfX3s9RoS-Zhc6RbeHt0YDZXnoIGR_t7t3A382g-ah5c4wYi2Ko6OkcfxP52QVbTWUfKK1oYE3kmaCNDYK4a_m2ZMMFMBeLASD2VUnz3sA3HUWbWvZZYsrHaQJlq5U5EscloaXLnKtzb8rjprRaU_kGH98R_wBSWG)
[Edit](https://mermaid.live/edit#pako:eNqNVU1v2zAM_SuCzy5QYMAOuaVLgxXLgmBJdxhyUS06FmJJhj66GUn_-yhH_laA-mKLfKQeHyn5kmSKQbJIQK84PWkqjpLg82pAG3K5LfzDpW2MLyuy-9GbQTrR2A91BeSY_ARplU6JfwOkZMkEl8ekDzBWc3kia66N3VIBM8-G3nE8C8rLmXVXKAlbJ95Az33UmL9Ks-_UFHOnVjkvYccz6zS8_tr0CAv_LHniCuWoinoW-SKtVsxlliv5mzNQXfDHUd4-bjIs35ExfeMlt_VUy6Fvoql33xKgYz1wMGqhDSxhhasBZy6A7C3V9sDF1P4sWW_tSG7AGCVnXb6ZY31eOU190djnL48p-fo4bCyDjAtaoq48m-70pNQZlZttFex36geY1H9XmBHtqWKNAmGnsWaNnvusAOZKYDE9W99Y0zAHf5QSGy7PE5WwCdYZ1KiLTsk3JaoSbPNJZQYlWlvxOpV2tBZY3UylYI-o1Os3Kjp0YimUk3ZHOYsIEpKOi274B09fhssy1DYlaxy8CO2tsjznWTMZM-5DZ6SAcKOsP1VXw26YMNw5zcWQkgOe2tFAtqUOQ_p6O_63q-56fXhQl9jBXeAWBTVt6hG8G2wPEvQMcdhYIo_VkAF_7-GRfX3s9RoS-Zhc6RbeHt0YDZXnoIGR_t7t3A382g-ah5c4wYi2Ko6OkcfxP52QVbTWUfKK1oYE3kmaCNDYK4a_m2ZMMFMBeLASD2VUnz3sA3HUWbWvZZYsrHaQJlq5U5EscloaXLnKtzb8rjprRaU_kGH98R_wBSWG)

## Stack recommedations

### Backend Recommendations

#### Programming Language:
-  Node.js: Asynchronous, scalable, and widely used for real-time applications. Great for handling notifications (emails, texts) and scheduling.
-  Python (Django/Flask): Offers robust frameworks and is excellent for developing data-driven applications. Django’s built-in admin panel can be leveraged for analytics and payroll tasks.

#### Framework:
-  Express.js (for Node.js): Lightweight and highly customizable.
-  Django: Full-stack framework with ORM, authentication, and admin capabilities out of the box.
-  NestJS: A modular and scalable framework for Node.js that supports TypeScript.

#### Database:
-  PostgreSQL: A relational database that supports advanced queries and JSON data types, which is ideal for storing structured mentor/mentee data.
-  MySQL: Another reliable choice for relational data, with good performance for medium-scale applications.
-  Redis (optional): For caching availability data or session management.

#### APIs and Communication:
-  REST: Simple to implement for standard CRUD operations (e.g., scheduling, user management).
-  GraphQL: If you need flexible querying for user profiles, availability, and bookings.

#### Notifications and Scheduling:
-  Twilio: For SMS notifications.
-  SendGrid: For email confirmations and reminders.
-  Agenda.js or Celery: For task scheduling (e.g., sending reminders).

#### Authentication:
-  OAuth2/JWT: For secure login and session management. Libraries like Passport.js (Node.js) or Django REST Framework's JWT support are great choices.


### Frontend Recommendations

#### Framework:

-  React.js: Highly interactive and flexible, with reusable components for mentor profiles, lesson scheduling, and booking pages.
-  Next.js: Built on React but optimized for server-side rendering (SSR), which is great for SEO and fast initial load times.

#### State Management:

-  Redux/Context API (React): For managing state like user authentication and session details.

#### Styling:

-  Tailwind CSS: Utility-first CSS framework that speeds up styling and ensures a modern design.
-  Material-UI: A React component library with pre-designed, accessible components.

#### Integration with Backend:

-  Use Axios or Fetch API for HTTP requests.
-  ApolloClient if GrapQL was selected for communication
-  Real-time updates with Django Channels or Socket.io if live scheduling updates are required.


## Other Tools and Technologies

### Deployment:

#### Backend:
-  AWS (Elastic Beanstalk, Lambda): Scalable and reliable for handling server workloads.
-  Heroku: Easy-to-use for small to medium projects.

#### Frontend:
-  Vercel: Optimized for React/Next.js apps.

#### DevOps and CI/CD:
-  GitHub Actions: Automate tests and deployment.
-  Docker: Containerize the application for easier deployment.

#### Analytics:
-  Google Analytics: For tracking frontend user interactions.
-  Custom Dashboard: Build with Chart.js or D3.js for mentor analytics.


#### Payment Gateway:
-  Stripe: Simple to integrate and handles one-time payments efficiently.
-  PayPal: Popular and trusted by users globally.
Note: All gateway systems need to approve the project codebase which can add up to a month in development times


### Recommended Stack Combination
-  Frontend: Next.js + Tailwind CSS + Context API
-  Backend: Node.js with Express.js + PostgreSQL
-  Notifications: Twilio + SendGrid
-  Hosting: AWS (backend) + Vercel (frontend)
-  Payment: Stripe

This stack ensures scalability, flexibility, and modern usability for both mentors and mentees. 
