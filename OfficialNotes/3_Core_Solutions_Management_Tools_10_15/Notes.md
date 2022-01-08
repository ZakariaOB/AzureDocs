# Describe core solutions available in Azure

## Describe the benefits and usage of Internet of Things (IoT) Hub, IoT Central, and Azure Sphere

- **IoT** enables devices to gather and then relay information for data analysis. Smart devices are equipped with sensors that collect data. A few common sensors that measure attributes of the physical world include:

    - Environmental sensors that capture temperature and humidity levels.
    - Barcode, QR code, or optical character recognition (OCR) scanners.
    - Geo-location and proximity sensors.
    - Light, color, and infrared sensors.
    - Sound and ultrasonic sensors.
    - Motion and touch sensors.
    - Accelerometer and tilt sensors.
    - Smoke, gas, and alcohol sensors.
    - Error sensors to detect when there's a problem with the device.
    - Mechanical sensors that detect anomalies or deformations.
    - Flow, level, and pressure sensors for measuring gasses and liquids.


- **IoT** Let's suppose your company manufactures and operates smart refrigerated vending machines. What kinds of information would you want to monitor? You might want to ensure that:

Each machine is operating without any errors.
The machines haven't been compromised.
The machines' refrigeration systems are keeping their contents within a certain temperature range.
You're notified when products reach a certain inventory level so you can restock the machines.
If the hardware of your vending machines can collect and send this information in a standard message, the messages each machine sends can be received, stored, organized, and displayed by using Azure IoT services.


- **Azure IoT Hub** is a managed service that's hosted in the cloud and that acts as a central message hub for bi-directional communication between your IoT application and the devices it manages. You can use Azure IoT Hub to build IoT solutions with reliable and secure communications between millions of IoT devices and a cloud-hosted solution back end. You can connect virtually any device to your IoT hub.

- **IoT Hub monitoring** helps you maintain the health of your solution by tracking events such as device creation, device failures, and device connections.

- **Azure IoT Central** builds on top of IoT Hub by adding a dashboard that allows you to connect, monitor, and manage your IoT devices. The visual user interface (UI) makes it easy to quickly connect new devices and watch as they begin sending telemetry or error messages. You can watch the overall performance across all devices in aggregate, and you can set up alerts that send notifications when a specific device needs maintenance. Finally, you can push firmware updates to the device.

- **Azure Sphere** creates an end-to-end, highly secure IoT solution for customers that encompasses everything from the hardware and operating system on the device to the secure method of sending messages from the device to the message hub. Azure Sphere has built-in communication and security features for internet-connected devices. => May be think about some usages

- **Azure Sphere** provides a complete solution for scenarios where security is critical. In this scenario, security is ideal, but not a critical priority. Although Azure Sphere provides an end-to-end solution that includes hardware, Tailwind Traders will use hardware from a third-party vendor. So, in this scenario, Azure Sphere is not necessary


## Explore big data and analytics

- Big data is a field of technology that helps with extraction, processing and analysis of information that is too large or complex to deal with using traditionnal software

- Big data parameters (As mush as we go high with thoses fields we start considering Big data)
     - ***Velocity*** : Real time, near real time, periodic , Batch
     - ***Volume***   : MB, GB, TB, PB
     - ***VARIETY***  : Databases, (photo/audio), (video/social)


- Data comes in all types of forms and formats. When we talk about big data, we're referring to large volumes of data. In this Tailwind Traders scenario, data is collected from the GPS sensors, which includes location information, data from weather systems, and many other sources that generate large amounts of data. This amount of data becomes increasingly hard to make sense of and to base decisions on. The volumes are so large that traditional forms of processing and analysis are no longer appropriate.

- Open-source cluster technologies have been developed, over time, to try to deal with these large datasets. Microsoft Azure supports a broad range of technologies and services to provide big data and analytic solutions, including Azure Synapse Analytics, Azure HDInsight, Azure Databricks, and Azure Data Lake Analytics.

- **Azure Synapse Analytics (formerly Azure SQL Data Warehouse)** is a limitless analytics service that  brings together enterprise data warehousing and big data analytics. You can query data on your terms by using either serverless or provisioned resources at scale. You have a unified experience to  ingest, prepare, manage, and serve data for immediate business intelligence and machine learning needs.

- **Azure HDInsight** is a fully managed, open-source analytics service for enterprises. It's a cloud service that makes it easier, faster, and more cost-effective to process massive amounts of data. You can run popular open-source frameworks and create cluster types such as Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services. HDInsight also supports a broad range of scenarios such as extraction, transformation, and loading (ETL), data warehousing, machine learning, and IoT.

- **Azure Databricks** helps you unlock insights from all your data and build artificial intelligence solutions. You can set up your Apache Spark environment in minutes, and then autoscale and collaborate on shared projects in an interactive workspace. Azure Databricks supports Python, Scala, R, Java, and SQL, as well as data science frameworks and libraries including TensorFlow, PyTorch, and scikit-learn.

- **Azure Data Lake Analytics** is an on-demand analytics job service that simplifies big data. Instead of deploying, configuring, and tuning hardware, you write queries to transform your data and extract valuable insights. The analytics service can handle jobs of any scale instantly by setting the dial for how much power you need. You only pay for your job when it's running, making it more cost-effective.

## Describe the benefits and usage of Azure Machine Learning, Cognitive Services and Azure Bot Service

- **Azure Machine** Learning is a platform for making predictions. It consists of tools and services that allow you to connect to data to train and test models to find one that will most accurately predict a future result. After you've run experiments to test the model, you can deploy and use it in real time via a web API endpoint.
  - With Azure Machine Learning, you can:
     - Create a process that defines how to obtain data, how to handle missing or bad data, how to split  the data into either a training set or test set, and deliver the data to the training process.
     - Train and evaluate predictive models by using tools and programming languages familiar to data  scientists.
     - Create pipelines that define where and when to run the compute-intensive experiments that are  required to score the algorithms based on the training and test data.
     - Deploy the best-performing algorithm as an API to an endpoint so it can be consumed in real time by  other applications.
  

- **Azure Cognitive Services** provides prebuilt machine learning models that enable applications to see, hear, speak, understand, and even begin to reason. Use Azure Cognitive Services to solve general problems, such as analyzing text for emotional sentiment or analyzing images to recognize objects or faces. You don't need special machine learning or data science knowledge to use these services. Developers access Azure Cognitive Services via APIs and can easily include these features in just a few lines of code.
  
     - While Azure Machine Learning requires you to bring your own data and train models over that data, Azure Cognitive Services, for the most part, provides pretrained models so that you can bring in your live data to get predictions on.
     - Azure Cognitive Services can be divided into the following categories:
        - Language services: 
           Allow your apps to process natural language with prebuilt scripts, evaluate      sentiment, and learn how to recognize what users want.
        - Speech services: 
            Convert speech into text and text into natural-sounding speech. Translate from one      language to another and enable speaker verification and recognition.
        - Vision services: 
            Add recognition and identification capabilities when you're analyzing pictures,        videos, and other visual content.
        - Decision services: 
            Add personalized recommendations for each user that automatically improve each       time they're used, moderate content to monitor and remove offensive or risky content, and detect    abnormalities in your time series data.


- **Azure Bot Service and Bot Framework** are platforms for creating virtual agents that understand and reply to questions just like a human. Azure Bot Service is a bit different from Azure Machine Learning and Azure Cognitive Services in that it has a specific use case. Namely, it creates a virtual agent that can intelligently communicate with humans. Behind the scenes, the bot you build uses other Azure services, such as Azure Cognitive Services, to understand what their human counterparts are asking for.

- Bots can be used to shift simple, repetitive tasks, such as taking a dinner reservation or gathering profile information, on to automated systems that might no longer require direct human intervention. Users converse with a bot by using text, interactive cards, and speech. A bot interaction can be a quick question and answer, or it can be a sophisticated conversation that intelligently provides access to services.


## Describe the benefits and usage of serverless computing solutions that include Azure Functions and Logic Apps 

- **Event driven app** After consulting with several of your fellow developers at Tailwind Traders, you've determined that some of your application logic is event driven. In other words, for a large amount of time, your application is waiting for a particular input before it performs any processing. To reduce your costs, you want to avoid having to pay for the time that your application is waiting for input. With that in mind, you've decided to investigate Azure Functions to see if it can help.

- **Serverless computing** is the abstraction of servers, infrastructure, and operating systems. With serverless computing, Azure takes care of managing the server infrastructure and the allocation and deallocation of resources based on demand. Infrastructure isn't your responsibility. Scaling and performance are handled automatically. You're billed only for the exact resources you use. There's no need to even reserve capacity.

- **Azure Functions** When you're concerned only about the code running your service, and not the underlying platform or infrastructure, using Azure Functions is ideal. Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.

   - Functions scale automatically based on demand, so they're a solid choice when demand is variable. For example, you    might receive messages from an IoT solution that's used to monitor a fleet of delivery vehicles. You'll likely have more data arriving during business hours.
   
   - Using a virtual machine-based approach, you'd incur costs even when the virtual machine is idle. With functions,  Azure runs your code when it's triggered and automatically deallocates resources when the function is finished. In this    model, you're only charged for the CPU time used while your function runs.
   
   - Functions can be either stateless or stateful. When they're stateless (the default), they behave as if they're    restarted every time they respond to an event. When they're stateful (called Durable Functions), a context is passed    through the function to track prior activity.
   
   - Functions are a key component of serverless computing. They're also a general compute platform for running any type of code. If the needs of the developer's app change, you can deploy the project in an environment that isn't serverless. This flexibility allows you to manage scaling, run on virtual networks, and even completely isolate the functions.

- **Azure Logic Apps** Logic apps are similar to functions. Both enable you to trigger logic based on an event. Where functions execute code, logic apps execute workflows that are designed to automate business scenarios and are built from predefined logic blocks.
    - Every Azure logic app workflow starts with a trigger, which fires when a specific event happens or when newly available data meets specific criteria. Many triggers include basic scheduling capabilities, so developers can specify how regularly their workloads will run. Each time the trigger fires, the Logic Apps engine creates a logic app instance that runs the actions in the workflow. These actions can also include data conversions and flow controls, such as conditional statements, switch statements, loops, and branching.
    - You create logic app workflows by using a visual designer on the Azure portal or in Visual Studio. The workflows are persisted as a JSON file with a known workflow schema.
    - Azure provides more than 200 different connectors and processing blocks to interact with different services. These resources include the most popular enterprise apps. You can also build custom connectors and workflow steps if the service you need to interact with isn't covered. You then use the visual designer to link connectors and blocks together. You pass data through the workflow to do custom processing, often all without writing any code.
    - As an example, let's say a ticket arrives in Zendesk. You could:
          - Detect the intent of the message with cognitive services.
          - Create an item in SharePoint to track the issue.
          - Add the customer to your Dynamics 365 CRM system if they aren't already in your database.
          - Send a follow-up email to acknowledge their request.
          - All of those actions could be designed in a visual designer, which makes it easy to see the logic flow. For this reason, it's ideal for a business analyst role.


- **Functions vs. Logic Apps**

   - Functions and Logic Apps can both create complex orchestrations. An orchestration is a collection of functions or steps that are executed to accomplish a complex task.
   - With Functions, you write code to complete each step.
   - With Logic Apps, you use a GUI to define the actions and how they relate to one another.
     You can mix and match services when you build an orchestration, calling functions from logic apps and calling logic  apps from functions. Here are some common differences between the two.


## Describe the benefits and usage of Azure DevOps, GitHub, GitHub Actions, and Azure DevTest Labs

- Benefits and usage of Azure DevOps, GitHub, GitHub Actions, and Azure 
DevTest Labs => I think you should know that
- **Azure DevTest Labs** is a service that enables developers to efficiently self-manage virtual machines (VMs) and Platform as a service (PaaS) resources without waiting for approvals. DevTest Labs creates labs consisting of pre-configured bases or Azure Resource
- What is the usage of Azure test labs : Managing a sandbox environnement for developers/testers(Paas)