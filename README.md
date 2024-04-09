**ISS Tracker and Notification System**

This project utilizes Python to create an automated system that tracks the International Space Station (ISS) and sends email notifications when the ISS is overhead during nighttime.

**Overview**
The script continuously checks two conditions:

**Nighttime Check:** Utilizes the requests library to fetch sunset and sunrise times based on latitude and longitude using the Sunrise-Sunset API. It determines whether it is currently nighttime at a specified location.
**ISS Overhead Check:** Fetches the current latitude and longitude of the ISS using the Open Notify API. Compares the ISS coordinates with a predefined location to check if the ISS is within a certain proximity.
When both conditions are met (i.e., it's nighttime and the ISS is overhead), the script sends an email notification using Gmail SMTP to a specified recipient.

**Features**
**Automated Tracking:** The script runs continuously in an infinite loop with a sleep interval, checking for the ISS overhead and nighttime conditions.
**API Integration:** Utilizes external APIs (Open Notify and Sunrise-Sunset) to gather real-time data for ISS position and sunrise/sunset times.
**Email Notifications:** Sends email notifications using SMTP when the specified conditions are met.
Error Handling: Includes robust error handling to manage potential issues with API requests and email sending processes.

**Setup and Usage**
Clone the repository to your local machine.
Install the required Python libraries (requests, smtplib) using pip:

**pip install requests**

Update the MY_LAT, MY_LONG, my_email, and password variables in the script with your desired location coordinates and Gmail credentials.

Run the script:
**python issoverhead.py**
Keep the script running in the background to monitor the ISS position and receive notifications.

**Dependencies**
Python 3.x
requests library for making HTTP requests
smtplib library for sending emails

**Notes**
Ensure that your Gmail account allows less secure apps or generates an app password for SMTP authentication.
The script is designed to run continuously in the background, so make sure to terminate it when not needed.
