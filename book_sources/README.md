# Cytoturing SDK Overview - 0.1.0 
Welcome to Cytoturing SDK.  
Cytoturing, the SDK for FCS file provides an automated way to run your analysis. 

## Prerequisites
---
Python 3.8.10 or newer.
## Features
---
### User authentication
get_access_token(email, password)

> Args:  
> &nbsp;&nbsp;&nbsp;&nbsp; email (str): email of the user.  
> &nbsp;&nbsp;&nbsp;&nbsp; password (str): password of the user.  
> Returns:    
> &nbsp;&nbsp;&nbsp;&nbsp; access_token (str): access token of the user.

<br/>
### Uploading fcs file
upload_file(access_token, file)

> Args:  
> &nbsp;&nbsp;&nbsp;&nbsp; access_token (str): access token of the user.  
> &nbsp;&nbsp;&nbsp;&nbsp; file (str): path and file name of the file you want to upload.  
> Returns:    
> &nbsp;&nbsp;&nbsp;&nbsp; file id (dict): unique id of the file you uploaded.

<br/>
### Prediction
run_predict(access_token, file_ids)

> Args:  
> &nbsp;&nbsp;&nbsp;&nbsp; access_token (str): access token of the user.  
> &nbsp;&nbsp;&nbsp;&nbsp; file ids (list): list of file ids in a sample.  
> Returns:    
> &nbsp;&nbsp;&nbsp;&nbsp; analysis id (str): prediction result of a target sample.  

<br/>
### Getting result
get_result(access_token, analysis_id)

> Args:  
> &nbsp;&nbsp;&nbsp;&nbsp; access_token (str): access token of the user.  
> &nbsp;&nbsp;&nbsp;&nbsp; analysis_id (str): id of a sample prediction.  
> Returns:    
> &nbsp;&nbsp;&nbsp;&nbsp; result (dict): prediction result of a target sample.  

