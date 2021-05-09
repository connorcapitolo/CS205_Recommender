# CS205_Recommender

## step-by-step guide for running Python
1. From the GitHub repository, copy over the python script to the EMR cluster

   $ scp -i ~/.ssh/your_.pem_file_here python/recommender.py  hadoop@y*our_Master_public_DNS_here*:/home/hadoop
   
2. Log in to the EMR cluster again

   $ ssh -i ~/.ssh/your_.pem_file_here hadoop@*your_Master_public_DNS_here*
   
3. Now, upload the MovieLens dataset you want to use to the EMR cluster; for this example, we will upload the Movielens 20mL dataset

   1. If uploading the dataset from the public S3 bucket to the EMR cluster home repository
    
       $ aws s3 cp s3://als-recommender-data/data/ratings_20ml.csv .
       
   2. If uploading from the GitHub repository
   
       $ scp -i ~/.ssh/your_.pem_file_here data/mldataset.csv  hadoop@y*our_Master_public_DNS_here*:/home/hadoop
       
    

