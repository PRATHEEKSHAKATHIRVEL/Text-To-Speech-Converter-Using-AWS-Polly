This project demonstrates how to use Amazon Polly for converting text to speech 

AWS SERVICES USED 
1. AWS LAMBDA
2. AWS POLLY
3. AWS S3
4. IAM

 HOW TO RUN 

CREATE S3 BUCKETS:

 1.Input Bucket - Stores the text file(.txt)
 
 2.Output Bucket - Stores the generated mp3 speech files.
 
LAMBDA TRIGGER 

 1.When you upload a .txt file to the input bucket, it automatically triggers, it triggers the lambda function.
 
CREATE LAMBDA FUNCTION
 
 1. Create a fucntion in AWS Lambda.

 2. Upload the Python code that reads the file from S3, calls polly, and stores output in MP3.

 ATTACH  IAM ROLES
 
 1. Attach IAM roles with lambda function
    
      S3: GetObject - Input Bucket
    
      s3: PutObject - Output Bucket
    
      polly: SynthesizeSpeech - for using polly
    
    
  CONFIGURE S3 EVENT NOTIFICATION
  
  1.Create an event notification with EVENT TYPE - PUT.
  
  TEST THE SETUP
  
  1.Upload the text file into the input bucket.
  
  VERIFY WORKFLOW
  
  1.Check the output bucket for the MP3 file.
  
  2.Download and play the file.  


