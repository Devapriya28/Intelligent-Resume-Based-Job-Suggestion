# 🧠 Intelligent Resume-Driven Job Recommendation & Skill-Gap Analysis System

Powered by OpenAI • RAG • AWS Lambda • Streamlit • MongoDB Atlas

This project is an end-to-end AI-powered job recommendation platform that intelligently analyzes resumes, extracts skills, retrieves real-time job openings, identifies skill gaps, and generates personalized career insights using a fully automated pipeline.

## 🚀 Key Features
✔ Smart Resume Upload & Secure Processing

Resume upload via Streamlit UI

Files stored securely in AWS S3 with metadata

Lambda-based virus scan & validation

S3 event trigger automatically starts processing workflow

## ✔ AI-Powered Resume Understanding

AWS Textract / Comprehend for structured text extraction

Amazon Titan Embeddings for generating resume vectors

OpenAI models used for:

Skill extraction & summarization

Education & work experience parsing

Achievement interpretation

Processed profile stored in MongoDB Atlas with embeddings

## ✔ RAG-Based Job Retrieval Layer

Fetches live job listings from Adzuna, JSearch, Indeed APIs

Embeds job descriptions & performs semantic similarity search

LLM (Claude/OpenAI) enriches each job with:

Summary

Required skills

Responsibilities

## ✔ Hybrid Job Ranking Engine

Multi-criteria scoring:

final_score = 0.55 * semantic_similarity 
            + 0.25 * keyword_overlap 
            + 0.10 * recency_weight 
            + 0.10 * popularity_score

## ✔ Interactive Streamlit Dashboard

Displays Top 20 job recommendations

Skill-gap heatmaps & match explanations

Course recommendations via Coursera API

Daily auto-refresh via API Gateway → Lambda

User feedback loop continuously improves ranking accuracy

## 🏗 System Architecture
Stage 1 — Resume Upload & Pre-Processing

Streamlit → S3 → Lambda (virus scan & validation)

Stage 2 — Resume Parsing & Embedding

Textract/Comprehend → Titan Embeddings → OpenAI summarization → MongoDB storage

Stage 3 — RAG Retrieval Layer

Job APIs → Embeddings → Vector search → LLM-based job enrichment

Stage 4 — Job Matching & Ranking

Semantic ranking + keyword scoring + recency + popularity → Skill-gap computation → Match explanation

Stage 5 — Visualization & Continuous Learning

Streamlit dashboard → Analytics → Automated daily updates → Feedback-driven model refinement

## 📊 Outcomes & Impact

Highly contextual job matches using hybrid semantic ranking

Automatically generated personalized summaries

End-to-end automated pipeline from S3 → Lambda → MongoDB → Streamlit

Analytics including:

Average match score

Skill-gap distribution

Industry/role fit insights# Intelligent-Resume-Based-Job-Suggestion
