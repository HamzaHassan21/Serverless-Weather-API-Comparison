🌐 AWS Lambda vs Lambda@Edge: Edge Computing Performance Analysis
📌 Overview

This project explores the performance differences between AWS Lambda (centralised) and Lambda@Edge (edge-based) by leveraging the OpenWeather API. It demonstrates how serverless functions behave when executed in a single AWS region versus globally distributed edge locations via CloudFront.

The goal is to provide actionable, real-world insights into latency, scalability, and responsiveness, showing the advantages of edge computing for globally distributed applications.

🎯 Objectives

Build two serverless systems:

Centralised Lambda via API Gateway

Lambda@Edge via CloudFront

Integrate the OpenWeather API for dynamic, location-aware responses.

Test latency, performance, and cold starts using Postman.

Monitor execution times, scalability, and cold starts with CloudWatch.

Compare results through graphs, tables, and analysis.

🏗️ Architecture
Centralised Lambda
Client → API Gateway → Lambda → OpenWeather API → Response


Metrics tracked with CloudWatch.

Execution occurs in a single AWS region.

Lambda@Edge
Client → CloudFront → Lambda@Edge → OpenWeather API → Response


Executes functions at the nearest edge location.

Supports location-aware, low-latency responses.

🔧 Tools & Technologies

AWS Lambda – serverless compute

Lambda@Edge – serverless compute at the edge

Amazon CloudFront – global content delivery network

API Gateway – centralised Lambda entry point

CloudWatch – monitoring latency, execution, and cold starts

Postman – request simulation and testing

OpenWeather API – real-time weather data

Python – function development

GitHub – version control and project publishing

📊 Testing & Methodology

Simulated requests from multiple regions using Postman.

Measured latency, execution times, and cold starts.

Monitored backend behaviour with CloudWatch Logs.

Compared results under controlled conditions to ensure fairness.

📈 Expected Outcomes

Lambda@Edge will demonstrate lower latency due to proximity to users.

CloudFront caching will reduce repeated request times.

Execution times for the function will remain similar, but network latency will highlight the advantages of edge computing.

📚 References

McGrath, G. & Brenner, P. (2017). Serverless Computing: Design, Implementation, and Performance. IEEE ICDCSW.

Satyanarayanan, M. (2017). The Emergence of Edge Computing. IEEE Computer.

AWS Documentation: Lambda, Lambda@Edge, CloudFront, CloudWatch

OpenWeather API Documentation

🚀 Publishing Intent

This project will be shared on:

GitHub – technical transparency and portfolio showcase

LinkedIn – highlight applied cloud engineering skills

🙌 Author

Hamza Hassan
Final-year Computer Science student | Cloud & DevOps enthusiast | Passionate about building scalable, efficient, and globally distributed cloud systems
