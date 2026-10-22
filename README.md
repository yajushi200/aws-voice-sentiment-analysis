# ☁️ Voice-Based Sentiment Analysis on AWS

**A serverless pipeline that turns spoken customer feedback into sentiment insights.**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=flat-square&logo=awslambda&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazons3&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-Sentiment-blueviolet?style=flat-square)

---

## The problem

Businesses collect voice feedback but rarely analyze it at scale. Listening to recordings by hand is slow, so customer insights get lost.

## The solution

Customers upload voice feedback. The system transcribes it, scores the sentiment (positive, neutral or negative), and produces a spoken summary and dashboard for business managers.

## Architecture

```
Voice upload ──► S3 bucket
                   │ (event)
                   ▼
               AWS Lambda  ── orchestrates the flow
                   │
                   ├── Amazon Transcribe   speech → text
                   ├── Amazon Comprehend   text → sentiment
                   └── Amazon Polly        results → audio summary
                   │
                   ▼
           REST API (AWS Chalice) ──► Dashboard
```

## Why these services

- **Serverless and pay-per-use**: Lambda and S3 keep costs low and scale with volume
- **Managed AI services**: Transcribe, Comprehend and Polly need little custom model work
- **Accessible output**: Polly turns results into audio summaries for managers

## My contribution

I researched Amazon Comprehend's capabilities and **configured the sentiment analysis pipeline**.

## Documentation

📄 [Design document](https://github.com/yajushi200/MyPortfolio/blob/main/AWS_SentimentAnalysis.pdf): architecture, component, ER and communication diagrams, workflow and implementation plan.

## Team

Group 2: Juwon Ajana, **Yajushi Garg**, Adarsh Sindhu Prabhan, Kabir Rooprai and Vineet Sharma.

> Source code will be added to this repository.
