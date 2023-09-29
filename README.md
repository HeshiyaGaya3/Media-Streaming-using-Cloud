# Media-Streaming-using-Cloud
Problem Definition:
"Media streaming with cloud streaming" refers to the challenge or task of setting up and managing the delivery of audio and video content to end-users using cloud-based infrastructure and services. This involves various steps and considerations, including content storage, encoding, delivery, security, scalability, player integration, analytics, cost management, and global reach. The goal is to stream media content efficiently and reliably to a wide audience while optimizing the user experience and managing the associated costs.
Nowadays people prefer online platforms more than normal cable channels. A survey conducted during December 2,2019 suggests that more than 65% of TV cable subscribers prefer online streaming.
![image](https://github.com/HeshiyaGaya3/Media-Streaming-using-Cloud/assets/114100105/dccd04df-6c04-4af0-8ebe-062f237265ab)
Live streaming has become an integral part of the marketing strategy for many brands and individuals due to its high level of engagement and unlimited interaction it offers . It is one of the most powerful ways to reach and interact with your audience . Here are some reasons why live streaming is considered important:
1.	Engagement: Live streaming has the highest rate of engagement among all content types . It allows viewers to post comments in real-time, creating an opportunity for interaction with the presenter and other viewers . This instant gratification fosters a deep connection between the viewers and the presenter, creating a sense of community .
2.	Interaction: Live streaming offers a level of interaction that no other platform or marketing strategy can match . Viewers can ask questions, provide feedback, and engage with the presenter during the live stream . This real-time interaction brings the audience closer to the presenter and opens up a great communication channel .
3.	Human Connection: Live streaming brings a human element to content creation. The fact that it is live means that anything can happen at any time, making it more authentic and relatable . Viewers can identify with presenters and feel a genuine connection with them .
4.	Flexibility: Unlike traditional TV, live streaming offers more flexibility in terms of content accessibility. Viewers can watch live streams on their mobile devices and often have the option to watch recorded versions later .
5.	Reach: Live streaming has a huge user base and growing popularity, making it an effective way to reach thousands or more new customers with just a click of a button .

Design Thinking:

Select a Cloud Provider:
To choose a cloud provider that offers media streaming capabilities. Popular choices include Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP), or specialized media streaming providers like Vimeo, Brightcove, or IBM Watson Media. Consider factors like cost, geographic reach, and service offerings when making your selection.

Content Preparation:
To prepare media content by encoding and transcoding it into suitable formats and bitrates for adaptive streaming. Most cloud streaming providers offer encoding/transcoding services or integrations with third-party tools.

Cloud Storage:
By Uploading media content to the cloud storage provided by your chosen cloud provider. Ensure proper organization and access controls to manage your content effectively.

Content Security:
Implementing security measures to protect your media content. This may include content encryption, token-based access control, and DRM solutions to prevent unauthorized access and piracy.

CDN Integration:
To set up integration with a Content Delivery Network (CDN) to distribute your media content efficiently to end-users. Configure caching, edge server locations, and CDN settings for optimal performance and low latency.

Player Integration:
Embedding a media player into your web or mobile applications using the provided SDKs or APIs from your cloud streaming service. Customize the player to match your brand and user experience requirements.

Scalability and Elasticity:
To Configure auto-scaling rules to handle varying levels of traffic. Ensure that your cloud infrastructure can automatically scale up or down based on demand to maintain a smooth streaming experience during peak periods.

Monitoring and Analytics:
To implement monitoring and analytics tools to track the performance of your media streaming service. Monitor viewer statistics, user engagement, and error logs to identify and address issues promptly.

Cost Management:
To monitor and manage costs by setting up budget alerts and optimizing resource usage and ensure that we understand the pricing structure of your cloud provider to avoid unexpected expenses.

Testing and Quality Assurance:
To conduct thorough testing of our media streaming service before going live. Test on various devices and network conditions to ensure a consistent and high-quality user experience.

Documentation and Training:
To document our setup and configurations, including security policies and procedures. Provide training to our team members responsible for managing and maintaining the media streaming service.

Launch and Monitor:
To launch our media streaming service to the public or our intended audience. Continuously monitor its performance and user feedback to make improvements and adjustments as needed.

Scaling and Optimization:
As audience grows or requirements change, we have to be prepared to scale our cloud streaming infrastructure accordingly. Optimize our setup based on performance data and user behavior.

Stay Informed:
Keeping abreast of industry trends and updates in cloud streaming technology. Cloud services evolve rapidly, and staying informed can help you take advantage of new features and improvements.

Customer Support and Feedback:
Being responsive to user feedback and provide excellent customer support. Address issues promptly to maintain a positive user experience.

SYSTEM DESIGN:
1.	Video ingestion:
As the first step let’s consider uploading data to the platform by creators. Let’s say they upload a video at 4K resolution and .mp4 format to some storage along with title, description, and tag. The storage should be secure, resilient, scalable, and cost effective. For this an ideal storage cloud service is Amazon s3 service. 

2.	Database:
We need a database to store all tags, descriptions, and title which we’ll need it when we search for a particular video. Using relational database will be a problem as they are not horizontally scalable. So for that we’ll use a NOSQL database called ElasticSearch which is used for storing text fields and optimize search for that fields.

SYSTEM ARCHITECTURE


![cad2](https://github.com/HeshiyaGaya3/Media-Streaming-using-Cloud/assets/114100105/14370f41-f3d6-4f31-8b15-83d27598707c)


3.	Video encoding:

Even if we upload in 4K resolution not everyone can watch in that resolution. It depends on the specs of the device which they are using to view the content. So this 4K resolution needs to be converted into different forms to be consumed by different devices. For this we use AWS service called Element Media Convert.

4.	Adult content detection:

For this we will be using an AIML service from amazon called amazon recognition. It gets the video analyses every frame against a presorted database and detects the adult content.

5.	Content Delivery Network:

Content Delivery Network(CDN) refers to a geographically distributed group of servers located at different places which work together to provide fast delivery of content. This is not only scalable but provides a very low latency to the end user.



                               

