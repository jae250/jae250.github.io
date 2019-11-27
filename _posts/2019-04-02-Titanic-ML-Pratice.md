---
layout: post
title: Titanic ML Practice
tags:
  - coding
  - Machine Learning
---



##### To use data files in Google Drive, install PyDrive in colab.

```css

!pip install -U -q PyDrive
from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive
from google.colab import auth
from oauth2client.client import GoogleCredentials

# 1. Authenticate and create the PyDrive client.
auth.authenticate_user()
gauth = GoogleAuth()
gauth.credentials = GoogleCredentials.get_application_default()
drive = GoogleDrive(gauth)

```
##### Enter verification code in the link to verfy.

> Go to the following link in your browser:

> Enter verification code:

#####  Download test.csv to colab account

```
file_id = 'find the file ID in google drive'
downloaded = drive.CreateFile({'id': file_id})
downloaded.GetContentFile('test.csv')
```

##### Download train.csv

```
file_id = 'find the file ID in google drive'
downloaded = drive.CreateFile({'id': file_id})
downloaded.GetContentFile('train.csv')
```

##### Check out test.csv and train.csv have been downloaded

```
!ls -al
```

##### import panda

```
import pandas as pd
train = pd.read_csv('train.csv')
test = pd.read_csv('test.csv')
```

TBC
