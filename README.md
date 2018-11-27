# dataset

本项目用于集中存储部分小的数据集，用于colab等云平台使用。

zip, tgz 获取方案：
```python
    # 导入包
    import tarfile
    import zipfile
    from six.moves import urllib
    #文件夹目录
    
    # 相关配置项
    data_path = os.path.join("datasets", "xxxxxxx")
    zip_file_name = 'xxxxxxx.zip'
    tgz_file_name = 'xxxxxxx.tgz'
    zip_url = 'https://raw.githubusercontent.com/sujeek/chinese_nlp/master/xxxxxx.zip'
    tgz_url = 'https://raw.githubusercontent.com/sujeek/chinese_nlp/master/xxxxxx.tgz'
    
    # 对应目录检测
    if not os.path.isdir(data_path):
        os.makedirs(data_path)
        
    #zip 文件下载解压    
    zip_path = os.path.join(data_path, file_name)
    urllib.request.urlretrieve(zip_url, zip_path)
    data_zip = zipfile.ZipFile(zip_path)
    data_zip.extractall(path=data_path)
    data_zip.close()

    #tgz 文件下载解压   
    tgz_path = os.path.join(data_path, tgz_file_name)
    urllib.request.urlretrieve(tgz_url, tgz_path)
    housing_tgz = tarfile.open(tgz_path)
    housing_tgz.extractall(path=housing_path)
```



