## Activity File: Exploring Kibana

* You are a DevOps professional and have set up monitoring for one of your web servers. You are collecting all sorts of web log data and it is your job to review the data regularly to make sure everything is running smoothly. 

* Today, you notice something strange in the logs and you want to take a closer look.

* Your task: Explore the web server logs to see if there's anything unusual. Specifically, you will:

:warning: **Heads Up**: These sample logs are specific to the time you view them. As such, your answers will be different from the answers provided in the solution file. 

---

### Instructions

1. Add the sample web log data to Kibana.

![Picture12](https://user-images.githubusercontent.com/94946212/160518140-bcd515c2-c73b-4278-be1a-e513b4437a99.png)

![image](https://user-images.githubusercontent.com/94946212/160518255-13ed6f08-c150-470b-bf37-6bf1f7c2c9fa.png)


2. Answer the following questions:

    - In the last 7 days, how many unique visitors were located in India?
    
    ![image](https://user-images.githubusercontent.com/94946212/160518300-02bda95d-893b-4df4-8ecf-07813b7a04c5.png)


    - In the last 24 hours, of the visitors from China, how many were using Mac OSX?

    ![image](https://user-images.githubusercontent.com/94946212/160518339-7033f30b-36fd-4d01-99ee-3c65e2c94227.png)


    - In the last 2 days, what percentage of visitors received 404 errors? How about 503 errors?
    
    ![image](https://user-images.githubusercontent.com/94946212/160518365-11454eaf-a5b8-44d6-b41b-5ef601d8357c.png)

    - In the last 7 days, what country produced the majority of the traffic on the website? China
    
    
    - Of the traffic that's coming from that country, what time of day had the highest amount of activity? 12-1 PM
    
    ![image](https://user-images.githubusercontent.com/94946212/160518490-cc6a9a96-04e1-410d-9b64-2693df72ac26.png)

    
    - List all the types of downloaded files that have been identified for the last 7 days, along with a short description of each file type (use Google if you 
    aren't sure about a particular file type).
   
   ![image](https://user-images.githubusercontent.com/94946212/160518631-86725e6b-8f8c-4cad-89de-36282d962d41.png)


3. Now that you have a feel for the data, Let's dive a bit deeper. Look at the chart that shows Unique Visitors Vs. Average Bytes.
     - Locate the time frame in the last 7 days with the most amount of bytes (activity).
     
    ![image](https://user-images.githubusercontent.com/94946212/160518682-fdf4cff0-0ce4-4f53-928f-31d874e74d9a.png)

    - In your own words, is there anything that seems potentially strange about this activity? One person is using a large amount of bytes that is higher than  
     everyone else

     ![image](https://user-images.githubusercontent.com/94946212/160518744-2ccf3dc8-ba8f-43ff-abfe-e7b5a57b8a2f.png)

4. Filter the data by this event.

  ![image](https://user-images.githubusercontent.com/94946212/160519008-2120e2b0-f78e-4b82-a5f6-f1a5470adfd8.png)

     - What is the timestamp for this event? 03/13/2022 @ 19:55
     - What kind of file was downloaded? RPM
   
   ![image](https://user-images.githubusercontent.com/94946212/160519349-df587e51-64b7-4b4d-a652-002f6bfcfb87.png)

     - From what country did this activity originate?  India
     - What HTTP response codes were encountered by this visitor? 200
     
    ![image](https://user-images.githubusercontent.com/94946212/160519526-79f143b2-694b-4f6b-bdec-6c16956b8262.png)


5. Switch to the Kibana Discover page to see more details about this activity.
     - What is the source IP address of this activity? 33.143.166.159
     - What are the geo coordinates of this activity? { "lat": 43.34121, "lon": -73.6103075 }
     - What OS was the source machine running? Windows 8
     - What is the full URL that was accessed?  https://artifacts.elastic.co/downloads/beats/metricbeat/metricbeat-6.3.2-i686.rpm
     - From what website did the visitor's traffic originate? Facebook

    ![image](https://user-images.githubusercontent.com/94946212/160519555-5ebdd289-b13e-4024-b764-a3acdd886d06.png)
    
    ![image](https://user-images.githubusercontent.com/94946212/160520212-d2ef7be7-82e7-4c0f-9d75-aa2224ea030e.png)



6. Finish your investigation with a short overview of your insights. 

     - What do you think the user was doing?
     -A user is downloading a Linux package from the website that is monitored
     - Was the file they downloaded malicious? If not, what is the file used for?
     - It is not for sure if it is malicious, in some cases it could be an update from a sysadmin and they are the ones creating the traffic. You would need more 
     information to figure if it is malicious.
     - Is there anything that seems suspicious about this activity? Not yet, without further investigation
     - Is any of the traffic you inspected potentially outside of compliance guidlines? Because it is a referral link from Facebook, it is most likely not in compliance to post updates from Facebook. This person could be further investigated in order to see if it is indeed suspicious activity

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  
