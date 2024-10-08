# API-ISS_Overhead

## Overview

This Python script checks if the International Space Station (ISS) is overhead and sends an email notification if it's nighttime at your location. It uses two APIs to determine if the ISS is overhead and if it is nighttime:


<img src="https://github.com/user-attachments/assets/ee0df77a-e501-4e75-b9e3-43d4b682027b" alt="description" width="600" />


1. **ISS API**: Provides the current coordinates (latitude and longitude) of the ISS.
2. **Sunset API**: Provides the sunrise and sunset times for a given latitude and longitude.

- **ISS API Website**: [Open Notify ISS Location Now](http://open-notify.org/Open-Notify-API/ISS-Location-Now/)
- **Sunset API Website**: [Sunrise Sunset API](https://sunrise-sunset.org/api)

## Prerequisites

- Python 3.x
- `requests` library
- `smtplib` for sending emails

## Environment Variables

Set the following environment variables in your system:

- `MY_LAT`: Your latitude (e.g., 52.5200 for Berlin)
- `MY_LNG`: Your longitude (e.g., 13.4050 for Berlin)
- `my_email`: Your email address (e.g., example@gmail.com)
- `my_password`: Your email password or app-specific password

## Installation & Usage

To set up and run the script:

1. **Clone the Repository**:

   ```bash
   git clone <repository-url>

2. **Navigate to the project directory**: 
   ```bash
    cd <project-directory>
   
3. **Install the required Python libraries**:
   ```bash
   pip install requests

4. **Make sure you have set up the environment variables as described**.
   
5. **Run the script**:
   ```bash 
   python <script-name>.py

## How It Works:

- Checks ISS Position: The script uses the ISS API to get the current position of the ISS and checks if it is within 5 degrees of your location.
- Checks Day/Night Status: The script uses the Sunset API to determine if it is currently nighttime at your location.
- Send Notification: If the ISS is overhead and it's nighttime, an email is sent to notify you.

