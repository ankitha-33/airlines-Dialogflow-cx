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

![Booking Intent](https://github.com/user-attachments/assets/44a46fb3-dcb8-41bc-83a7-5941d1a11b2d)


3. Lounge Access -
   By using this Intent the user can Indentify if they are eligible to access the lounge

![Lounge Access](https://github.com/user-attachments/assets/3f8496c2-db47-4b14-b9a1-b97fde437543)

4. Queries-
   In this intent we do have a sub topics as 
>> Queries for students >> Queries for any restriction rules >> Queries regarding the Baggs and weights
And the flow are as shown below - 

>>Queries for students- 
![studentqueries](https://github.com/user-attachments/assets/9bf1f2dd-982c-4201-b973-6424fa24b378)

>>Queries for any restrictiosn - 
![restrictionqueries](https://github.com/user-attachments/assets/548d9737-1fb8-4448-bd60-eb597a289986)

>>Queries for Bags and Laguage weights - 
![weight queries](https://github.com/user-attachments/assets/6cce5ab4-5f64-431f-afa8-78a239f5e628)

5. The flow for booking a flight or to check the flight availability is as follows - 
>>Happy flow - 

![book flight](https://github.com/user-attachments/assets/4e904454-fcb9-4530-881f-bd04a1287337)
![book flight](https://github.com/user-attachments/assets/66a11a18-5ece-472b-aa48-e4854ef7d6f7)
![book flight](https://github.com/user-attachments/assets/267c8cf7-6d85-4baf-a45e-b94508995722)
![book flight](https://github.com/user-attachments/assets/5d06723e-7d96-4544-95db-026bef8bca2e)


Here the custom payload is the card which displays the booking  availability for the critiera the user mentiond in the happy flow.



Now let's try the flow for booking a flight by providing both source and destination source as the same  - 

![Book](https://github.com/user-attachments/assets/1c1ea443-633c-4e34-97fa-fb4174a05599)

Here both source and destination is considerd to be the same "Delhi", in the screenshot provided you can observe that when source is mentiond as Delhi and also the destination Delhi, the destination is considerd as "Null". This is because the parameter perset is given a condition as "NULL" for the condition id "$Session.params.source == $session.params.destination" .

![conditional Route](https://github.com/user-attachments/assets/f6195f71-651b-4b36-bb1e-f44cad4cae61)
![conditional Route](https://github.com/user-attachments/assets/bda92960-30e5-429d-9d09-aaf1b147aa5f)
![condidtional flow ](https://github.com/user-attachments/assets/d0437672-d509-4ec9-a214-127f020ae10a)
