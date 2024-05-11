# :chart_with_upwards_trend:# OTP_Generator-python # :chart_with_upwards_trend:

# Problem Statement:

Problem scenario


Your company is a providing taxi services to customer's to join that company has recently started online user verification process to fasten the verification process. As soon as users has to join , customers will be provided with services.

So your task is to develop an OTP (One-Time Password) verification system in Python. The system should generate a 6-digit OTP and send it to the user's email address for verification. Upon receiving the OTP, the user should enter it into the system for validation. If the entered OTP matches the generated OTP, access should be granted; otherwise, access should be denied.


# :closed_lock_with_key: # Project Requirements:#:closed_lock_with_key:


1) Implement a function to generate a 6-digit OTP randomly.

2) Develop a function to simulate sending the OTP to the user's email address.

3) Create a function to prompt the user to enter the OTP received in their email.

4) Implement a function to verify if the entered OTP matches the generated OTP.

5) Ensure proper error handling and user-friendly prompts throughout the system.

6) Allow the user to retry OTP entry in case of incorrect input.


# :key: **CODE--** # :key:

      def user():
        first_name=input("Enter the first name : ")
        last_name=input("Enter the last name : ")
        email=input("Enter the email id to which OTP will be send : ")
        return email



**#Implement a function to generate a 6-digit OTP randomly.**

      def generate_new_OTP():
        import random
        OTP=""
       o=""
        for i in range(0,6):
          o=str(random.randint(0,9))
          OTP=str(OTP+o)
        return OTP



**#Develop a function to simulate sending the OTP to the user's email address.**
   
      def simulate_send_otp_email(email_1, OTP_1):
          print("\n\n Entry to company server:")
          print(f'Email sent to: {email_1}')
          print(f'This OTP : {OTP_1}')


   **#Create a function to prompt the user to enter the OTP received in their email.**
   
      def email(email_1,OTP_1):
        print("\nsender=sender_email_address\n")
        print(f"Recieved : {email_1}")
        print("Message Body : OTP verification  ")
        print(f"This OTP is to verify the user. To join verify the OTP sent:{OTP_1}.")



   **#Implement a function to verify if the entered OTP matches the generated OTP.**

   
    def verify(OTP_1):

     for i in range(0,3):  #Allow the user to retry OTP entry in case of incorrect input.
       veri=input("\n\nEnter the OTP received on email : ")
       chance=2
       if veri==OTP_1:
         print("Verification completed. Thank you")
         break
       else:
         if chance >=1:
           print(f"\nInvalid password {2-i} chance left ")
           chance=2-i
         if chance <= 0:
            print("Your verification process is NOT completed.")
            print("If you want to connect to our page restart verification process again")
            print("For any other query, you can call your customer call centre : 044-12345678 / 044-87654321 ")
            break

            
      def task():
       email_1 =user()
       OTP_1=(generate_new_OTP())
       simulate_send_otp_email(email_1,OTP_1)
       email(email_1,OTP_1)
       verify(OTP_1)


**# main function is called here**
      
      
        task()



# :green_book: # OUTPUT-- # :green_book:

![Screen Shot 2024-04-12 at 12 23 49 AM](https://github.com/Sumit-Baviskar/OTP_Generator-python-/assets/153518735/ac38250a-2a89-47eb-9d41-5c9bee0d61a4)

![Screen Shot 2024-04-12 at 12 24 04 AM](https://github.com/Sumit-Baviskar/OTP_Generator-python-/assets/153518735/a704d607-f7ca-4255-b9b3-6a73d7de0bae)


# :green_book: # Project Deliverables: # :green_book:

Python script containing the implementation of the OTP verification system

This Python script implements a simple OTP (One-Time Password) verification system. It includes functions to generate a 6-digit OTP, send it to a user's email address, prompt the user to enter the OTP, and verify if the entered OTP matches the generated one


1)Documentation explaining the functionality of each function, how to run the program, and any dependencies required.

# :green_book: # Functionality of Each Function # :green_book:

a) **user()**: This function prompts the user to enter their first name, last name, and email address. It returns the entered email address.

b) **generate_new_OTP()**: Generates a random 6-digit OTP using the random module.

c) **simulate_send_otp_email(email_1, OTP_1)**: Simulates sending the OTP to the user's email address. It prints the email address and the generated OTP.

d) **email(email_1, OTP_1)**: Prints a message body containing the OTP and instructions for verification. It includes the received email address and OTP.

e) **verify(OTP_1)**: Prompts the user to enter the OTP received in their email. It allows the user to retry OTP entry in case of incorrect input.

f) **task()**: Combines the above functions to simulate the OTP verification process


# :green_book: # How to Run the Program: # :green_book:

Run the script in a Python environment. Follow the prompts to enter your first name, last name, and email address. An OTP will be generated and simulated to be sent to your email address. Check your email for the OTP and enter it when prompted. The system will verify the entered OTP and provide feedback.

Dependencies: The script requires the random module for generating OTPs and the smtplib, email.mime.multipart, and email.mime.text modules for simulating email sending

2)Test cases to ensure the system functions correctly under various scenarios, including correct and incorrect OTP entries.

# :green_book: # Test Cases: # :green_book:

Test the system under various scenarios, including:

1 ) Entering the correct OTP --> Entering the correct OTP which is send to email that should be entered ensure the verification is completed the process.

Entering an incorrect OTP --> There are 3 chances are given to the users .Everytime user enter a password wrong customer is displayed " invalid password" meassage and number of chances left count on screen

Exceeding the maximum number of attempts.(there 3 attempts) --> If users enters invald password 3 times . A message is display to restart the verification process to join the page Or the company's customer call centre number is diplayed to the user.
