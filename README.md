Airline Booking- Dialogflow -CX

This repository contains the implementation of a Dialogflow-based chatbot designed for airline booking and support services. The bot assists users with various functionalities, such as flight availability and scheduling, booking status, flight status, lounge availability, and baggage inquiries.

Use Case Overview
The chatbot provides a conversational interface that helps users with the following main features:

Flight Availability & Scheduling: Users can check the availability and schedules of flights by providing source and destination details.
Booking Status: Users can view their booking status by entering their boarding pass or booking reference number.
Flight Status: Allows users to check the status of specific flights by flight number or route.
Lounge Availability: Users can check lounge access based on their booking reference number.
Baggage Inquiries: The chatbot provides information on excess baggage policies, student privileges, and restricted items.
Key Features
Natural Language Understanding: Uses Dialogflow's NLU capabilities to understand user queries and provide relevant responses.
Multimedia Responses: Displays booking and flight schedules in a multimedia format for easy viewing.
Conditional Logic: Includes logic for different user inputs, such as asking for specific information in a step-by-step flow based on previous responses.
Fallback and Redirect Handling: Handles unrecognized inputs gracefully by redirecting users to the main menu or asking for clarification.
Workflow Summary
Flight Queries: The chatbot asks for details such as source, destination, and departure date to check flight schedules.
Booking Status: Users input their booking reference to view the current status of their reservation.
Flight Status: Provides real-time flight status based on flight number or route.
Lounge Availability: Checks if lounge access is available for users with specific bookings.
Baggage Assistance: Offers detailed guidance on baggage rules, including allowances for students, excess baggage fees, and prohibited items.
Installation
Clone the repository.
Set up Dialogflow and import the intents and entities.
Deploy the webhook server if using custom API integrations.
Connect Dialogflow to your preferred messaging platform (e.g., WhatsApp, Facebook Messenger).
Requirements
Google Dialogflow
Node.js / Python (for webhook integration)
Optional: Cloud Functions or a similar hosting platform for serverless deployment
Usage
After setting up, users can interact with the chatbot to get real-time information and assistance with flight-related queries.

Contributing
Please open issues or submit pull requests to contribute. The project is open for enhancements, including additional airline services and multi-language support.


1. Welcome page - 
When we start the flow as "Hi", "Hello", "what are you ?", "what can you do" etc, the bot responses as shown  -
![Welcome Page](https://github.com/user-attachments/assets/9ee3cf47-5f0e-4cf9-be55-f7479e68a0d2)

2. Booking status Intent- 
When the user want to check the status of their booking if it's cancelled/completed/pending, user questions the bot asking for the status for their booking. The flow is shown below - 

![Booking Intent](https://github.com/user-attachments/assets/ea5a6f56-ed89-49ec-a4bb-ac76da699929](https://github.com/user-attachments/assets/44a46fb3-dcb8-41bc-83a7-5941d1a11b2d)



