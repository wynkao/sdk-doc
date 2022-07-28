# Quick Start
Here are examples of how to use our SDK to run your analysis.
## Get access token
---
```py
import cytoturing as ct

email = 'your email'
password = 'your password'
auth_client = ct.client('authentication')
access_token = auth_client.get_access_token(email, password)
```

## Upload data
---
```py
import cytoturing as ct

dir_path = 'path of your file folder'
file_names = [List of your file names]
file_ids = []
for file_name in file_names:
    file = f'{dir_path}\\{file_name}'
    file_client = ct.client('file_handler')
    file_id = file_client.upload_file(access_token, file)
    file_ids.append(file_id
print('file_ids:', file_ids)
```
## Run prediction
---
```py
import cytoturing as ct

file_ids = [list of your file ids]
analysis_client = ct.client('analysis')
analysis_id = analysis_client.run_predict(access_token, file_ids)
print('analysis_id: ', analysis_id)
```
## Get result
---
```py
import cytoturing as ct

analysis_client = ct.client('analysis')
result = analysis_client.get_result(access_token, analysis_id)
print(result)
```