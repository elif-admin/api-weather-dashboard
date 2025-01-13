# 30 Days DevOps Challenge - Weather Dashboard

Day 1: Building a weather data collection system using AWS S3 and OpenWeather API

# Weather Data Collection System - DevOps Day 1 Challenge

In this project, I'll show you how to run an API application using Python on AWS. The application fetches weather data for three cities from OpenWeather.
Prerequisites
Before you start, make sure you have:
•	An AWS account. If you don't have one, sign up here.
•	A GitHub repository with your source code. If you don’t have a GitHub account,sign up here.
•	A code editor. For this tutorial, I used VS Code.

Step 1: Write the Python Code and Requirements
First, we need the Python code and dependencies required for the project. You can easily access these by cloning the public repository from the ShaeInTheCloud GitHub page.
Clone the repository to your local environment:
git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard  
 ![image](https://github.com/user-attachments/assets/3b7e992c-ecd4-4aa2-a551-09aa3ec41c60)

The repository includes the __init__.py and weather_dashboard.py files that we’ll use. The structure should be as below:
 
Next, create a requirements.txt file to list the dependencies for the project:
boto3==1.26.137  
python-dotenv==1.0.0  
requests==2.28.2  
You can create this file either manually using your preferred editor (e.g., VS Code) or directly via the terminal:
echo "boto3==1.26.137\npython-dotenv==1.0.0\nrequests==2.28.2" > requirements.txt  
 
Or you can write the commands in the file directly using vscode.
 
Install the dependencies using the following command:
pip install -r requirements.txt  
Additionally, create a .gitignore file to exclude sensitive or unnecessary files (e.g., .env and __pycache__) when pushing to a repository.
 
Or like that:
 
Step 2: Configure AWS Credentials
To interact with AWS, configure your credentials by following this guide. You’ll need your AWS Access Key and AWS Secret Key.
Step 3: Sign Up for OpenWeather
Sign up on OpenWeather to obtain your API key. After signing in, navigate to your dashboard to find the API key.
 
You can see the API key here:
 
Configure environment variables to securely store your API key and S3 bucket name:
echo "OPENWEATHER_API_KEY=your_api_key" >> .env  
echo "AWS_BUCKET_NAME=your_bucket_name" >> .env  
Replace your_api_key and your_bucket_name with your actual API key and desired S3 bucket name.
 
Step 4: Run the Python Code
With everything set up, you’re ready to run the application. Navigate to the src directory and execute the Python script:
python weather_dashboard.py  
The script will fetch weather data for the specified cities and store it in an AWS S3 bucket.
 
Verify the Results
Check your terminal output for the fetched weather data. You can also visit your S3 bucket to confirm that the data has been stored successfully.
 
 
Final Step: What We Learned
Through this project, you learned how to:
1.	Work with APIs like OpenWeather to fetch real-time data.
2.	Use Python libraries such as requests, boto3, and dotenv to handle HTTP requests, AWS interactions, and environment variables.
3.	Configure AWS credentials and automate the creation of S3 buckets.
4.	Secure sensitive information using environment variables and .gitignore.
5.	Organize project files, install dependencies, and deploy a functional Python application.
This hands-on experience highlights the integration of Python programming with cloud services, providing a foundation for future projects involving APIs and AWS.
That’s it! You've now completed a hands-on project to create a weather dashboard API using Python and AWS.
If you have any questions, feel free to share them in the comments.


