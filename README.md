打包至pip install供他人使用
===
### 打包作業
請先上"人類最強設置指引"的github(連官方都認可的指引)，並copy其setup.py檔至根目錄<br>  
https://github.com/navdeep-G/setup.py<br>  
並於內更改成自己專案的形式<br>
![image](https://user-images.githubusercontent.com/101057598/168760001-d7c558a4-7e9d-4882-8a50-2f3060417475.png)<br>
![image](https://user-images.githubusercontent.com/101057598/168760009-264daa65-50a4-4995-a047-e439ea5ceb49.png)<br>
### 上傳至pypi作業  
https://packaging.python.org/en/latest/guides/distributing-packages-using-setuptools/<br>
py -m pip install twine<br>
### LICENSE.txt
https://choosealicense.com/<br>
主要是讓別人知道你的檔案權限如何，選定後創建LICENSE.txt貼上其文字<br>
### 後續流程，我這邊會貼上當時的筆記，若未來有需要我會改天再整理並簡化該內容　
python setup.py sdist (且於路徑資料夾內使用)<br>
![image](https://user-images.githubusercontent.com/101057598/168761550-92407f6c-ced0-421d-b35e-1f5eea11b875.png)<br>
python setup.py bdist_wheel<br>
![image](https://user-images.githubusercontent.com/101057598/168761575-8f658bf0-3e59-412c-904c-7efa86ad2b5b.png)<br>
 要更新<br>
Pip install –upgrade setuptools<br>
發現還是有錯，則安裝wheel <br>
Pip install wheel<br>
#### 所以: pip install wheel → pip install --upgrade setuptools → python setup.py bdist_wheel
Note: 若只有built distribution(wheel)  →別人僅能使用，不能更改原始碼<br>
最後辦帳號 + add api (api僅出現一次)<br>
![image](https://user-images.githubusercontent.com/101057598/168761905-ed1d65f4-48f8-4e03-b7af-b975ade9cc23.png)<br> 
於檔案目錄輸入 %homepath% 存檔檔名輸入.pypirc<br>
<the token value, including the `pypi-` prefix> 為要替代掉的地方<br>
最後上傳<br>
 ![image](https://user-images.githubusercontent.com/101057598/168761983-19a9cb5c-a0ee-4b46-bd22-adf8cd4b879b.png)<br>
 成功了<br>
 ![image](https://user-images.githubusercontent.com/101057598/168762011-664c5001-dde4-4c27-aa6d-7b25fc805d6f.png)<br> 

