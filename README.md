# Fashion Embeddings Application

This repository contains code for an application that computes embeddings for a fashion dataset, stores them using PINECONE, and links them with text tags and image ids in a database. The application is wrapped in a FAST API, supporting two main functions: retrieving the closest image based on a text description and finding similar images to a given image. Additionally, a Streamlit app is provided to interact with the FAST API.

## Step 1: Retrieve Data

Datasets used for this project can be found at the following source:
- [Google Drive](https://drive.google.com/drive/folders/0B7EVK8r0v71pQ2FuZ0k0QnhBQnc?resourcekey=0-NWldFxSChFuCpK4nzAIGsg)

## Step 2: Application Design

The application follows these steps:
1. Compute embeddings for the dataset and store them using PINECONE.
2. Store images from Step 1 in Amazon S3.
3. Build a database linking image ids to text tags and embeddings.

## Step 3: FAST API

The FAST API has two main functions:

### a. Retrieve Closest Image based on Text Description
- Endpoint: `/get_image_by_text`
- Method: POST
- Input: JSON with text description
- Output: JSON with the closest image information

### b. Find Similar Images to a Given Image
- Endpoint: `/get_similar_images`
- Method: POST
- Input: JSON with either an uploaded image or a URL
- Output: JSON with information on three similar images

## Step 4: Streamlit App

The Streamlit app allows users to input text or upload an image and calls the corresponding FAST API function to get results.

