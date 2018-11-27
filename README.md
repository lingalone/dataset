# dataset

本项目用于集中存储部分小的数据集，用于colab等云平台使用。

获取方案：
```python
    #文件夹目录
    
    data_path=
    if not os.path.isdir(data_path):
        os.makedirs(data_path)
    zip_path = os.path.join(data_path, "data.zip")
    urllib.request.urlretrieve(zip_url, zip_path)
    data_zip = zipfile.ZipFile(zip_path)
    data_zip.extractall(path=data_path)
    data_zip.close()
```
