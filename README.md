# Feature Recommendation Engine (Collaborative Filtering on AWS SageMaker)

## Project Summary
Designed and deployed a collaborative-filtering recommendation engine to increase feature adoption within a digital product platform. The solution suggested personalized services to users based on historical interaction data.

## Problem Statement
Many users were unaware of the full suite of services available to them. The business wanted to boost engagement and adoption of underutilized features through intelligent recommendations tailored to user behavior.

## Tools & Technologies Used
- **Language & Libraries**: Python, Pandas, Scikit-learn  
- **Machine Learning**: Alternating Least Squares (ALS)  
- **Infrastructure**: AWS SageMaker, Flask (API), PostgreSQL  
- **Cloud Services**: SageMaker (training + endpoint), S3 (model artifacts), CloudWatch (monitoring)

## Modeling Approach
- Generated a user-feature interaction matrix from anonymized event logs (clicks, usage frequency)
- Applied ALS matrix factorization to learn user/item latent embeddings
- Tuned model for top-N implicit feedback recommendations

## API Endpoint (Simulated Example)
```
POST /recommend
{
  "user_id": "12345"
}
```
**Response**
```json
{
  "recommended_features": ["PayPal.Me", "One Touch", "Bill Pay"]
}
```

## System Architecture Overview
```
User Event Logs ─▶ PostgreSQL ─▶ ETL Script ─▶ ALS Model (SageMaker) ─▶ Flask API ─▶ Product UI
                                                     │
                                               CloudWatch Logs
```

## Deployment Details
- Trained model on AWS SageMaker using distributed GPU instance
- Deployed as a real-time inference endpoint
- Flask-based microservice served recommendations via REST API
- Integrated with product UI for seamless real-time suggestions

## Results & Impact
- **12% increase in feature adoption** across 30-day post-deployment cohort
- Drove increased visibility and usage of premium PayPal services
- Supported product-led growth by improving onboarding and in-app engagement

## Monitoring & Feedback Loop
- Logged recommendation response times and user click-throughs
- Created dashboards to track adoption per feature over time
- Incorporated A/B testing for recommendation layout optimization

## Challenges & Learnings
- Tackled cold start issue by building a fallback popularity-based recommender
- Tuned ALS hyperparameters to balance diversity and relevance in suggestions
- Learned the importance of aligning UX with model output for conversion

## My Role
- Led full-cycle development from ETL through deployment and metrics monitoring
- Collaborated with product managers and designers to ensure in-product adoption
- Coordinated deployment with MLOps team to scale with minimal latency

## Code Availability
Due to confidentiality and client restrictions, source code and datasets are not publicly available. Synthetic examples may be published in a future companion repo.
