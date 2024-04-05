# FishWatch 

![image](./images/FishWatch_Banner.gif)  

---

# [Table Of Contents](#table-of-contents-)
- [Prologue](#prologue-)
- [Our Insight](#our-insight-)
- [Lets Talk Business - FishWatch Key Requirements](#lets-talk-business---fishwatch-key-requirements-)
- [Solution Approach](#solution-approach-)
- [High Level Architecture](#high-level-architecture-)
- [Capabilities & Systems - Our BeeHives](#capabilities--systems---our-beehives-)
- [Decisions - Focus is Honey](#decisions---focus-is-honey-)
- [Operational Strategy - No Fishy Deals](#operational-strategy---no-fishy-deals-)
- [Evolve - You adapt change](#evolve---you-adapt-change-)

## Prologue  [🔝](#fishwatch)
Livestock Insights Incorporated, a pioneer in the field of livestock monitoring solutions, is expanding its expertise into the realm of aquaculture with the introduction of the FishWatch system. This innovative platform is strategically designed to transform the aquaculture industry by providing fish farmers with real-time insights into water quality, fish health, and environmental conditions. By leveraging advanced technology, FishWatch aims to enable proactive management and optimization of fish farm operations, thus enhancing the overall productivity and sustainability of aquaculture practices.The development of the FishWatch system is driven by the increasing demand for efficient and data-driven fish farming solutions. As the global population continues to grow, so does the demand for seafood. Aquaculture has emerged as a vital industry to meet this demand, but it faces challenges such as disease outbreaks, environmental pollution, and resource management. FishWatch addresses these challenges by offering a comprehensive monitoring solution that empowers fish farmers to make informed decisions, reduce risks, and maximize yields.

## Our Insight  [🔝](#fishwatch)

   ![image](./images/TheArchBees_Logo.png) 
  - [Kushagra Rana](https://www.linkedin.com/in/kushagrar/)
  - [Salil Sharma](https://www.linkedin.com/in/salil-sharma-36170b24/)
  - [Pratik Purohit](https://www.linkedin.com/in/pratik-kumar-purohit-a776844b/)
    
  We specialize in scalable and robust systems, committed to delivering cutting-edge solutions that cater to the unique needs of our clients. 

## Lets Talk Business - FishWatch Key Requirements [🔝](#fishwatch)
- Multitenancy for data isolation among different users.
- Scalability to handle increasing volumes of data and users.
- Real-time analysis and data processing for immediate insights.
- Data storage with support for AI and ML algorithms.
- Customizable dashboards for visualization and business intelligence.
- Text-to-speech and voice assistant features for enhanced user interaction.
- Voice search capabilities.
- A customizable alerting and notification system.
- Advanced analytics for comparison, benchmarking, and optimization.
- Reliable connectivity and networking solutions.
- Integration with hardware and low network devices like satellite communication systems.
- Extensibility for future enhancements.
- Robust security measures to protect data and system integrity.
- Compliance with regulations based on geographical locations.

## Solution Approach [🔝](#fishwatch)
Our methodology for designing the FishWatch system was centered around a comprehensive and collaborative approach. We began with a thorough analysis of the aquaculture industry's needs and the specific requirements outlined by Livestock Insights Incorporated.

- **Functional Design**: Based on the requirements, We focused on creating a solution that is not only technologically advanced but also practical and user-friendly for fish farmers.
  
![image](./diagrams/FishWatchSolutionApproach1.svg) 

<h4 align="center">Fig 1.1 FishWatch Solution Design 1</h4>

### Some Assumptions
- **Reliable Sensor Data**: Sensors and underwater cameras are assumed to provide accurate and reliable data for monitoring water quality and fish health.
- **Stable Connectivity in Remote Areas**: A minimum level of network availability is assumed in remote locations for data transmission to the cloud platform.
- **Scalable Cloud Infrastructure**: The cloud platform is assumed to have dynamic scaling capabilities to handle varying data volumes and user numbers.
- **User Adoption and Training**: Fish farmers are assumed to be receptive to adopting the FishWatch system, with adequate training provided for effective use.
- **Integration Compatibility**: Existing hardware and software systems at fish farms are assumed to support standard communication protocols and APIs for seamless integration.
- **Regulatory Compliance**: The FishWatch system is assumed to comply with all relevant data security, privacy, and environmental monitoring regulations.
- **Extensibility for Future Enhancements**: The system is designed to be extensible, with the assumption that future enhancements will not require a complete architectural overhaul.
- **Cross-Farm Insights**: For large customers, the system is assumed to be capable of aggregating and analyzing data across different farm locations to provide comprehensive insights.

## High Level Architecture [🔝](#fishwatch)

### Architecture Work for FishWatch
Our architectural work for the FishWatch system was guided by a deep understanding of the aquaculture industry's needs and the specific requirements of Livestock Insights Incorporated. we crafted a modular and scalable architecture that addresses the core objectives of real-time data processing & monitoring, data analysis, connectivity and user accessibility.

![image](./diagrams/FIshWatchSolutionApproach2.svg) 

<h4 align="center">Fig 1.2 FishWatch Solution Design 2</h4>

### Edge Layer
Includes sensors and cameras for data collection, and edge processors for local data analysis.

### Cloud Platform
- **Data Ingestion Service**: Manages incoming data.
- **Data Storage**: Utilizes time-series databases and data lakes.
- **Analytics Service**: Provides real-time and historical data analysis.
- **API Gateway**: Secures and manages API access.
- **Security Service**: Ensures authentication, authorization, and compliance.

### User Interfaces
Web and mobile applications for farm monitoring and management.

### High-Level Architecture Diagram
![High-Level Architecture](high-level-architecture-diagram.png)

## Capabilities & Systems - Our BeeHives [🔝](#fishwatch)
- **Data Ingestion Service**: Ensures reliable data collection, employing message queues for data spikes and processors for validation.
- **Data Storage**: 
  - **Time-Series Database**: Optimized for storing and querying sensor data.
  - **Data Lake**: Archives historical data and video feeds for deep analysis.
- **Analytics Service**: 
  - **Real-time Analytics**: Analyzes data streams for immediate insights.
  - **Machine Learning**: Develops models for predictive analytics and anomaly detection.
- **API Gateway**: 
  - Facilitates secure and efficient API management.
  - Routes API requests to appropriate services.
  - Enforces rate limiting for fair usage.
- **Security Service**: 
  - **Authentication**: Verifies user identities and manages sessions.
  - **Authorization**: Controls access based on user roles.
  - **Compliance**: Ensures adherence to regulatory standards.

## Decisions - Focus is Honey [🔝](#fishwatch)
- **Edge Computing**: Utilized for local data processing to reduce latency.
- **Microservices Architecture**: Adopted for scalability and flexibility.
- **Cloud Platform Choice**: Selected based on scalability and service offerings (e.g., AWS, Azure, GCP).
- **Data Storage Solutions**: Chosen for efficient data management (e.g., InfluxDB, TimescaleDB for time-series data; Hadoop, S3 for data lakes).
- **Analytics Tools**: Apache Kafka and Apache Flink for real-time data processing; TensorFlow, PyTorch for machine learning.
- **API Management**: Employed an API gateway for security and scalability.
- **Security Protocols**: Implemented industry-standard security practices (e.g., OAuth 2.0, JWT for authentication; HTTPS for data encryption).

## Operational Strategy - No Fishy Deals [🔝](#fishwatch)
- **Deployment**: Automated deployment pipelines for consistent and reliable updates to the FishWatch system.
- **Monitoring and Logging**: Utilized tools like Prometheus, Grafana, and the ELK Stack for system monitoring and log management.
- **Disaster Recovery**: Cloud-based backup and replication strategies to ensure data integrity and system availability.

## Evolve - You adapt change [🔝](#fishwatch)
- **Scalability Plans**: Designed to scale horizontally, allowing for increased capacity as the number of farms and data volume grows.
- **Extensibility Considerations**: Modular architecture enables the addition of new features and integration with emerging technologies.
- **Future Enhancements**: Potential integration with advanced sensors, IoT devices, and AI-driven analytics for enhanced fish health monitoring and environmental management.

---
