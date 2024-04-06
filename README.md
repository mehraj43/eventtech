EventTech: Tech Event Creation and Booking Platform
Project Overview
EventTech is a sophisticated platform designed to revolutionize the way tech events are created, managed, and attended. This platform facilitates event organizers in setting up online or onsite events, which can be either free or priced. It incorporates an intuitive booking system for users, along with real-time updates to event organizers about ticket purchases. Deployed on Vercel, EventTech aims to provide a seamless and user-friendly experience for tech communities.

Purpose
The purpose of this project is to provide a comprehensive solution for the tech community to host and attend events, enhancing networking and learning opportunities. This platform bridges the gap between event organizers and attendees, providing features to manage events efficiently.

Scope
Event creation, editing, and deletion by organizers
Booking system for attendees
Real-time updates to organizers about ticket sales
Support for online and onsite events
Integration of payment processing for priced events
Technology Stack
EventTech leverages a modern technology stack to ensure a robust, scalable, and efficient platform:

Frontend: Next.js, TailwindCSS for a responsive and aesthetically pleasing user interface.
Backend: Next.js API routes serve as the backend, handling business logic and database operations.
Database: MongoDB Atlas (Free Tier), providing a scalable and flexible NoSQL database solution.
Payment Processing: Stripe, offering a secure and efficient way to handle payments for priced events.
Authentication: Clerk, ensuring secure user authentication and management.
Additional Tools: Shadcn for UI components, enhancing the visual and interactive aspects of the platform.
Project Setup
Prerequisites
Node.js (version 12.x or later)
A MongoDB Atlas account
Stripe account for payment processing
Clerk account for user authentication
Vercel account for deployment
Local Environment Setup
Clone the Repository:
git clone https://github.com/yourusername/eventtech.git
cd eventtech
Install Dependencies:
npm install
Environment Variables: Create a .env.local file at the root of your project and add the following keys:
NEXT_PUBLIC_SERVER_URL=http://localhost:3000
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
WEBHOOK_SECRET=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/
MONGODB_URI=
UPLOADTHING_SECRET=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
Run the Development Server:
npm run dev
Access the application at http://localhost:3000.
Features
Event Management
Create Event: Organizers can create events, specifying details like title, description, date, location (for onsite events), and price (for priced events).
Edit Event: Event details can be modified post-creation.
Delete Event: Events can be removed from the platform.
Booking System
Users can book tickets for events. For priced events, payment is processed through Stripe.
Organizers receive real-time notifications about ticket purchases.
User Authentication
User authentication is managed via Clerk, ensuring a secure login and signup process.
API Endpoints
The platform's functionality is exposed through RESTful API endpoints, handled by Next.js API routes. Below are some of the critical endpoints:

Event Creation: https://eventme-nine.vercel.app/events/create - This endpoint allows event organizers to create new events.
Event Edit: https://eventme-nine.vercel.app/events/[eventId]/update - This endpoint enables event organizers to update the details of an existing event.
Event Delete: The delete event functionality is triggered by a button click on the event management page (https://eventme-nine.vercel.app/profile). This action sends a request to the backend to delete the specified event.
Deployment
EventTech is deployed on Vercel, ensuring high availability and performance. The deployment process involves connecting your GitHub repository to Vercel and configuring environment variables via the Vercel dashboard.

Log in to your Vercel account and click on "New Project".
Import your GitHub repository and select it for deployment.
Configure environment variables as per your .env.local file in the Vercel project settings.
Deploy your application.
Conclusion
EventTech serves as an end-to-end solution for the tech community to engage and grow through events. This documentation aims to guide you through the project's intricacies, setup, and deployment, ensuring a comprehensive understanding of its capabilities and functionalities.