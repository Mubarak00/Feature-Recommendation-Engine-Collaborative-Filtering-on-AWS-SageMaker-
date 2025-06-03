# Feature-Recommendation-Engine-Collaborative-Filtering-on-AWS-SageMaker-

## Project Summary
Designed and deployed a collaborative-filtering recommendation engine to increase feature adoption within a digital product platform. The solution suggested personalized services to users based on historical interaction data.

## Problem Statement
Many users were unaware of the full suite of services available to them. The business wanted to boost engagement and adoption of underutilized features through intelligent recommendations tailored to user behavior.

## Tools & Technologies Used
- **Language & Libraries**: Python, Pandas, Scikit-learn  
- **Machine Learning**: Alternating Least Squares (ALS)  
- **Infrastructure**: AWS SageMaker, Flask (for endpoint interaction)  
- **Data Source**: Anonymized user-feature interaction logs from PostgreSQL

## Modeling Approach
- Created a user-item matrix from usage logs (implicit feedback: feature clicks, frequency)  
- Applied ALS for matrix factorization to learn user and feature embeddings  
- Generated top-N personalized feature suggestions per user

## Deployment
- Trained and deployed the model using AWS SageMaker  
- Built a lightweight Flask API to serve real-time recommendations  
- Integrated recommendations into the product UI as dynamic feature tiles

## Results & Impact
- **12% increase in feature adoption**  
- Enhanced user engagement through personalized experience  
- Improved visibility for high-value, underused services

## Role
- Led end-to-end development from data engineering to deployment  
- Collaborated with product teams to align recommendations with UX placement  
- Monitored adoption metrics via integrated analytics

## Code Availability
Due to confidentiality and client restrictions, source code and datasets are not publicly available.
