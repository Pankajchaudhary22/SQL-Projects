```python
import pandas as pd
import pandasql as ps
```


```python
a=pd.read_csv("titanic.csv")
```


```python
ps.sqldf("select * from a order by a.Pclass limit 10")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>12</td>
      <td>1</td>
      <td>1</td>
      <td>Bonnell, Miss. Elizabeth</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>113783</td>
      <td>26.5500</td>
      <td>C103</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24</td>
      <td>1</td>
      <td>1</td>
      <td>Sloper, Mr. William Thompson</td>
      <td>male</td>
      <td>28.0</td>
      <td>0</td>
      <td>0</td>
      <td>113788</td>
      <td>35.5000</td>
      <td>A6</td>
      <td>S</td>
    </tr>
    <tr>
      <th>5</th>
      <td>28</td>
      <td>0</td>
      <td>1</td>
      <td>Fortune, Mr. Charles Alexander</td>
      <td>male</td>
      <td>19.0</td>
      <td>3</td>
      <td>2</td>
      <td>19950</td>
      <td>263.0000</td>
      <td>C23 C25 C27</td>
      <td>S</td>
    </tr>
    <tr>
      <th>6</th>
      <td>31</td>
      <td>0</td>
      <td>1</td>
      <td>Uruchurtu, Don. Manuel E</td>
      <td>male</td>
      <td>40.0</td>
      <td>0</td>
      <td>0</td>
      <td>PC 17601</td>
      <td>27.7208</td>
      <td>None</td>
      <td>C</td>
    </tr>
    <tr>
      <th>7</th>
      <td>32</td>
      <td>1</td>
      <td>1</td>
      <td>Spencer, Mrs. William Augustus (Marie Eugenie)</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17569</td>
      <td>146.5208</td>
      <td>B78</td>
      <td>C</td>
    </tr>
    <tr>
      <th>8</th>
      <td>35</td>
      <td>0</td>
      <td>1</td>
      <td>Meyer, Mr. Edgar Joseph</td>
      <td>male</td>
      <td>28.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17604</td>
      <td>82.1708</td>
      <td>None</td>
      <td>C</td>
    </tr>
    <tr>
      <th>9</th>
      <td>36</td>
      <td>0</td>
      <td>1</td>
      <td>Holverson, Mr. Alexander Oskar</td>
      <td>male</td>
      <td>42.0</td>
      <td>1</td>
      <td>0</td>
      <td>113789</td>
      <td>52.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
  </tbody>
</table>
</div>




```python
ps.sqldf("select * from a  where a.Age>40 or a.Fare>60 ")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>2</th>
      <td>12</td>
      <td>1</td>
      <td>1</td>
      <td>Bonnell, Miss. Elizabeth</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>113783</td>
      <td>26.5500</td>
      <td>C103</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>16</td>
      <td>1</td>
      <td>2</td>
      <td>Hewlett, Mrs. (Mary D Kingcome)</td>
      <td>female</td>
      <td>55.0</td>
      <td>0</td>
      <td>0</td>
      <td>248706</td>
      <td>16.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>28</td>
      <td>0</td>
      <td>1</td>
      <td>Fortune, Mr. Charles Alexander</td>
      <td>male</td>
      <td>19.0</td>
      <td>3</td>
      <td>2</td>
      <td>19950</td>
      <td>263.0000</td>
      <td>C23 C25 C27</td>
      <td>S</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>233</th>
      <td>864</td>
      <td>0</td>
      <td>3</td>
      <td>Sage, Miss. Dorothy Edith "Dolly"</td>
      <td>female</td>
      <td>NaN</td>
      <td>8</td>
      <td>2</td>
      <td>CA. 2343</td>
      <td>69.5500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>234</th>
      <td>866</td>
      <td>1</td>
      <td>2</td>
      <td>Bystrom, Mrs. (Karolina)</td>
      <td>female</td>
      <td>42.0</td>
      <td>0</td>
      <td>0</td>
      <td>236852</td>
      <td>13.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>235</th>
      <td>872</td>
      <td>1</td>
      <td>1</td>
      <td>Beckwith, Mrs. Richard Leonard (Sallie Monypeny)</td>
      <td>female</td>
      <td>47.0</td>
      <td>1</td>
      <td>1</td>
      <td>11751</td>
      <td>52.5542</td>
      <td>D35</td>
      <td>S</td>
    </tr>
    <tr>
      <th>236</th>
      <td>874</td>
      <td>0</td>
      <td>3</td>
      <td>Vander Cruyssen, Mr. Victor</td>
      <td>male</td>
      <td>47.0</td>
      <td>0</td>
      <td>0</td>
      <td>345765</td>
      <td>9.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>237</th>
      <td>880</td>
      <td>1</td>
      <td>1</td>
      <td>Potter, Mrs. Thomas Jr (Lily Alexenia Wilson)</td>
      <td>female</td>
      <td>56.0</td>
      <td>0</td>
      <td>1</td>
      <td>11767</td>
      <td>83.1583</td>
      <td>C50</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
<p>238 rows × 12 columns</p>
</div>




```python
ps.sqldf("select * from a where a.Fare between 20 and 40")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8</td>
      <td>0</td>
      <td>3</td>
      <td>Palsson, Master. Gosta Leonard</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>349909</td>
      <td>21.0750</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10</td>
      <td>1</td>
      <td>2</td>
      <td>Nasser, Mrs. Nicholas (Adele Achem)</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>237736</td>
      <td>30.0708</td>
      <td>None</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>12</td>
      <td>1</td>
      <td>1</td>
      <td>Bonnell, Miss. Elizabeth</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>113783</td>
      <td>26.5500</td>
      <td>C103</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>14</td>
      <td>0</td>
      <td>3</td>
      <td>Andersson, Mr. Anders Johan</td>
      <td>male</td>
      <td>39.0</td>
      <td>1</td>
      <td>5</td>
      <td>347082</td>
      <td>31.2750</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>17</td>
      <td>0</td>
      <td>3</td>
      <td>Rice, Master. Eugene</td>
      <td>male</td>
      <td>2.0</td>
      <td>4</td>
      <td>1</td>
      <td>382652</td>
      <td>29.1250</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>195</th>
      <td>881</td>
      <td>1</td>
      <td>2</td>
      <td>Shelley, Mrs. William (Imanita Parrish Hall)</td>
      <td>female</td>
      <td>25.0</td>
      <td>0</td>
      <td>1</td>
      <td>230433</td>
      <td>26.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>196</th>
      <td>886</td>
      <td>0</td>
      <td>3</td>
      <td>Rice, Mrs. William (Margaret Norton)</td>
      <td>female</td>
      <td>39.0</td>
      <td>0</td>
      <td>5</td>
      <td>382652</td>
      <td>29.1250</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>197</th>
      <td>888</td>
      <td>1</td>
      <td>1</td>
      <td>Graham, Miss. Margaret Edith</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>112053</td>
      <td>30.0000</td>
      <td>B42</td>
      <td>S</td>
    </tr>
    <tr>
      <th>198</th>
      <td>889</td>
      <td>0</td>
      <td>3</td>
      <td>Johnston, Miss. Catherine Helen "Carrie"</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>W./C. 6607</td>
      <td>23.4500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>199</th>
      <td>890</td>
      <td>1</td>
      <td>1</td>
      <td>Behr, Mr. Karl Howell</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>111369</td>
      <td>30.0000</td>
      <td>C148</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
<p>200 rows × 12 columns</p>
</div>




```python
ps.sqldf('''select * from a where a.Name like "%Mr%" ''')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>6</td>
      <td>0</td>
      <td>3</td>
      <td>Moran, Mr. James</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>330877</td>
      <td>8.4583</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>642</th>
      <td>884</td>
      <td>0</td>
      <td>2</td>
      <td>Banfield, Mr. Frederick James</td>
      <td>male</td>
      <td>28.0</td>
      <td>0</td>
      <td>0</td>
      <td>C.A./SOTON 34068</td>
      <td>10.5000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>643</th>
      <td>885</td>
      <td>0</td>
      <td>3</td>
      <td>Sutehall, Mr. Henry Jr</td>
      <td>male</td>
      <td>25.0</td>
      <td>0</td>
      <td>0</td>
      <td>SOTON/OQ 392076</td>
      <td>7.0500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>644</th>
      <td>886</td>
      <td>0</td>
      <td>3</td>
      <td>Rice, Mrs. William (Margaret Norton)</td>
      <td>female</td>
      <td>39.0</td>
      <td>0</td>
      <td>5</td>
      <td>382652</td>
      <td>29.1250</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>645</th>
      <td>890</td>
      <td>1</td>
      <td>1</td>
      <td>Behr, Mr. Karl Howell</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>111369</td>
      <td>30.0000</td>
      <td>C148</td>
      <td>C</td>
    </tr>
    <tr>
      <th>646</th>
      <td>891</td>
      <td>0</td>
      <td>3</td>
      <td>Dooley, Mr. Patrick</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>370376</td>
      <td>7.7500</td>
      <td>None</td>
      <td>Q</td>
    </tr>
  </tbody>
</table>
<p>647 rows × 12 columns</p>
</div>




```python
ps.sqldf("select * from a where a.Age is null")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>6</td>
      <td>0</td>
      <td>3</td>
      <td>Moran, Mr. James</td>
      <td>male</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>330877</td>
      <td>8.4583</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>1</th>
      <td>18</td>
      <td>1</td>
      <td>2</td>
      <td>Williams, Mr. Charles Eugene</td>
      <td>male</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>244373</td>
      <td>13.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20</td>
      <td>1</td>
      <td>3</td>
      <td>Masselmani, Mrs. Fatima</td>
      <td>female</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>2649</td>
      <td>7.2250</td>
      <td>None</td>
      <td>C</td>
    </tr>
    <tr>
      <th>3</th>
      <td>27</td>
      <td>0</td>
      <td>3</td>
      <td>Emir, Mr. Farred Chehab</td>
      <td>male</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>2631</td>
      <td>7.2250</td>
      <td>None</td>
      <td>C</td>
    </tr>
    <tr>
      <th>4</th>
      <td>29</td>
      <td>1</td>
      <td>3</td>
      <td>O'Dwyer, Miss. Ellen "Nellie"</td>
      <td>female</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>330959</td>
      <td>7.8792</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>172</th>
      <td>860</td>
      <td>0</td>
      <td>3</td>
      <td>Razi, Mr. Raihed</td>
      <td>male</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>2629</td>
      <td>7.2292</td>
      <td>None</td>
      <td>C</td>
    </tr>
    <tr>
      <th>173</th>
      <td>864</td>
      <td>0</td>
      <td>3</td>
      <td>Sage, Miss. Dorothy Edith "Dolly"</td>
      <td>female</td>
      <td>None</td>
      <td>8</td>
      <td>2</td>
      <td>CA. 2343</td>
      <td>69.5500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>174</th>
      <td>869</td>
      <td>0</td>
      <td>3</td>
      <td>van Melkebeke, Mr. Philemon</td>
      <td>male</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>345777</td>
      <td>9.5000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>175</th>
      <td>879</td>
      <td>0</td>
      <td>3</td>
      <td>Laleff, Mr. Kristo</td>
      <td>male</td>
      <td>None</td>
      <td>0</td>
      <td>0</td>
      <td>349217</td>
      <td>7.8958</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>176</th>
      <td>889</td>
      <td>0</td>
      <td>3</td>
      <td>Johnston, Miss. Catherine Helen "Carrie"</td>
      <td>female</td>
      <td>None</td>
      <td>1</td>
      <td>2</td>
      <td>W./C. 6607</td>
      <td>23.4500</td>
      <td>None</td>
      <td>S</td>
    </tr>
  </tbody>
</table>
<p>177 rows × 12 columns</p>
</div>




```python
ps.sqldf("select * from a where (a.Age>50 and a.Sex='male') or (a.Age>40 and a.Fare>40)")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>34</td>
      <td>0</td>
      <td>2</td>
      <td>Wheadon, Mr. Edward H</td>
      <td>male</td>
      <td>66.0</td>
      <td>0</td>
      <td>0</td>
      <td>C.A. 24579</td>
      <td>10.5000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>2</th>
      <td>36</td>
      <td>0</td>
      <td>1</td>
      <td>Holverson, Mr. Alexander Oskar</td>
      <td>male</td>
      <td>42.0</td>
      <td>1</td>
      <td>0</td>
      <td>113789</td>
      <td>52.0000</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>53</td>
      <td>1</td>
      <td>1</td>
      <td>Harper, Mrs. Henry Sleeper (Myna Haxtun)</td>
      <td>female</td>
      <td>49.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17572</td>
      <td>76.7292</td>
      <td>D33</td>
      <td>C</td>
    </tr>
    <tr>
      <th>4</th>
      <td>55</td>
      <td>0</td>
      <td>1</td>
      <td>Ostby, Mr. Engelhart Cornelius</td>
      <td>male</td>
      <td>65.0</td>
      <td>0</td>
      <td>1</td>
      <td>113509</td>
      <td>61.9792</td>
      <td>B30</td>
      <td>C</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>79</th>
      <td>852</td>
      <td>0</td>
      <td>3</td>
      <td>Svensson, Mr. Johan</td>
      <td>male</td>
      <td>74.0</td>
      <td>0</td>
      <td>0</td>
      <td>347060</td>
      <td>7.7750</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>80</th>
      <td>857</td>
      <td>1</td>
      <td>1</td>
      <td>Wick, Mrs. George Dennick (Mary Hitchcock)</td>
      <td>female</td>
      <td>45.0</td>
      <td>1</td>
      <td>1</td>
      <td>36928</td>
      <td>164.8667</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>81</th>
      <td>858</td>
      <td>1</td>
      <td>1</td>
      <td>Daly, Mr. Peter Denis</td>
      <td>male</td>
      <td>51.0</td>
      <td>0</td>
      <td>0</td>
      <td>113055</td>
      <td>26.5500</td>
      <td>E17</td>
      <td>S</td>
    </tr>
    <tr>
      <th>82</th>
      <td>872</td>
      <td>1</td>
      <td>1</td>
      <td>Beckwith, Mrs. Richard Leonard (Sallie Monypeny)</td>
      <td>female</td>
      <td>47.0</td>
      <td>1</td>
      <td>1</td>
      <td>11751</td>
      <td>52.5542</td>
      <td>D35</td>
      <td>S</td>
    </tr>
    <tr>
      <th>83</th>
      <td>880</td>
      <td>1</td>
      <td>1</td>
      <td>Potter, Mrs. Thomas Jr (Lily Alexenia Wilson)</td>
      <td>female</td>
      <td>56.0</td>
      <td>0</td>
      <td>1</td>
      <td>11767</td>
      <td>83.1583</td>
      <td>C50</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
<p>84 rows × 12 columns</p>
</div>




```python
ps.sqldf("select a.Age as person_age,a.Name as person_name from a")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>person_age</th>
      <th>person_name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>22.0</td>
      <td>Braund, Mr. Owen Harris</td>
    </tr>
    <tr>
      <th>1</th>
      <td>38.0</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>26.0</td>
      <td>Heikkinen, Miss. Laina</td>
    </tr>
    <tr>
      <th>3</th>
      <td>35.0</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
    </tr>
    <tr>
      <th>4</th>
      <td>35.0</td>
      <td>Allen, Mr. William Henry</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>27.0</td>
      <td>Montvila, Rev. Juozas</td>
    </tr>
    <tr>
      <th>887</th>
      <td>19.0</td>
      <td>Graham, Miss. Margaret Edith</td>
    </tr>
    <tr>
      <th>888</th>
      <td>NaN</td>
      <td>Johnston, Miss. Catherine Helen "Carrie"</td>
    </tr>
    <tr>
      <th>889</th>
      <td>26.0</td>
      <td>Behr, Mr. Karl Howell</td>
    </tr>
    <tr>
      <th>890</th>
      <td>32.0</td>
      <td>Dooley, Mr. Patrick</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 2 columns</p>
</div>




```python
ps.sqldf("select a.Fare, a.Fare*32 from a")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Fare</th>
      <th>a.Fare*32</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7.2500</td>
      <td>232.0000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>71.2833</td>
      <td>2281.0656</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7.9250</td>
      <td>253.6000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>53.1000</td>
      <td>1699.2000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8.0500</td>
      <td>257.6000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>13.0000</td>
      <td>416.0000</td>
    </tr>
    <tr>
      <th>887</th>
      <td>30.0000</td>
      <td>960.0000</td>
    </tr>
    <tr>
      <th>888</th>
      <td>23.4500</td>
      <td>750.4000</td>
    </tr>
    <tr>
      <th>889</th>
      <td>30.0000</td>
      <td>960.0000</td>
    </tr>
    <tr>
      <th>890</th>
      <td>7.7500</td>
      <td>248.0000</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 2 columns</p>
</div>




```python
ps.sqldf("select a.Name, lower(a.Name) from a")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>lower(a.Name)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Braund, Mr. Owen Harris</td>
      <td>braund, mr. owen harris</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>cumings, mrs. john bradley (florence briggs th...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Heikkinen, Miss. Laina</td>
      <td>heikkinen, miss. laina</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>futrelle, mrs. jacques heath (lily may peel)</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Allen, Mr. William Henry</td>
      <td>allen, mr. william henry</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>Montvila, Rev. Juozas</td>
      <td>montvila, rev. juozas</td>
    </tr>
    <tr>
      <th>887</th>
      <td>Graham, Miss. Margaret Edith</td>
      <td>graham, miss. margaret edith</td>
    </tr>
    <tr>
      <th>888</th>
      <td>Johnston, Miss. Catherine Helen "Carrie"</td>
      <td>johnston, miss. catherine helen "carrie"</td>
    </tr>
    <tr>
      <th>889</th>
      <td>Behr, Mr. Karl Howell</td>
      <td>behr, mr. karl howell</td>
    </tr>
    <tr>
      <th>890</th>
      <td>Dooley, Mr. Patrick</td>
      <td>dooley, mr. patrick</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 2 columns</p>
</div>




```python
ps.sqldf("select a.Fare, a.Ticket, a.Fare||a.Ticket as Fare_Ticket_no from a")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Fare</th>
      <th>Ticket</th>
      <th>Fare_Ticket_no</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7.2500</td>
      <td>A/5 21171</td>
      <td>7.25A/5 21171</td>
    </tr>
    <tr>
      <th>1</th>
      <td>71.2833</td>
      <td>PC 17599</td>
      <td>71.2833PC 17599</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7.9250</td>
      <td>STON/O2. 3101282</td>
      <td>7.925STON/O2. 3101282</td>
    </tr>
    <tr>
      <th>3</th>
      <td>53.1000</td>
      <td>113803</td>
      <td>53.1113803</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8.0500</td>
      <td>373450</td>
      <td>8.05373450</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>13.0000</td>
      <td>211536</td>
      <td>13.0211536</td>
    </tr>
    <tr>
      <th>887</th>
      <td>30.0000</td>
      <td>112053</td>
      <td>30.0112053</td>
    </tr>
    <tr>
      <th>888</th>
      <td>23.4500</td>
      <td>W./C. 6607</td>
      <td>23.45W./C. 6607</td>
    </tr>
    <tr>
      <th>889</th>
      <td>30.0000</td>
      <td>111369</td>
      <td>30.0111369</td>
    </tr>
    <tr>
      <th>890</th>
      <td>7.7500</td>
      <td>370376</td>
      <td>7.75370376</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 3 columns</p>
</div>




```python
ps.sqldf("select a.Name, substr(a.Name,3,7) as Sarting_4_Characters from a")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Sarting_4_Characters</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Braund, Mr. Owen Harris</td>
      <td>aund, M</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>mings,</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Heikkinen, Miss. Laina</td>
      <td>ikkinen</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>trelle,</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Allen, Mr. William Henry</td>
      <td>len, Mr</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>Montvila, Rev. Juozas</td>
      <td>ntvila,</td>
    </tr>
    <tr>
      <th>887</th>
      <td>Graham, Miss. Margaret Edith</td>
      <td>aham, M</td>
    </tr>
    <tr>
      <th>888</th>
      <td>Johnston, Miss. Catherine Helen "Carrie"</td>
      <td>hnston,</td>
    </tr>
    <tr>
      <th>889</th>
      <td>Behr, Mr. Karl Howell</td>
      <td>hr, Mr.</td>
    </tr>
    <tr>
      <th>890</th>
      <td>Dooley, Mr. Patrick</td>
      <td>oley, M</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 2 columns</p>
</div>




```python
ps.sqldf('''select a.Fare,
         case    
         when a.Fare<40 then 'General class'
         when a.Fare<70 then 'Sleeper class'
         when a.Fare <100 then '2nd_AC_class'
         when a.Fare<150 then 'premium class'
         when a.Fare<200 then 'Gold class'
         else
         'Platinum class'
         end as class_of_people from a limit 60''')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Fare</th>
      <th>class_of_people</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7.2500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>1</th>
      <td>71.2833</td>
      <td>2nd_AC_class</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7.9250</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>3</th>
      <td>53.1000</td>
      <td>Sleeper class</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8.0500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>5</th>
      <td>8.4583</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>6</th>
      <td>51.8625</td>
      <td>Sleeper class</td>
    </tr>
    <tr>
      <th>7</th>
      <td>21.0750</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>8</th>
      <td>11.1333</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>9</th>
      <td>30.0708</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>10</th>
      <td>16.7000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>11</th>
      <td>26.5500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>12</th>
      <td>8.0500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>13</th>
      <td>31.2750</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>14</th>
      <td>7.8542</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>16</th>
      <td>29.1250</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>17</th>
      <td>13.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>18</th>
      <td>18.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>19</th>
      <td>7.2250</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>20</th>
      <td>26.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>21</th>
      <td>13.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>22</th>
      <td>8.0292</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>23</th>
      <td>35.5000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>24</th>
      <td>21.0750</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>25</th>
      <td>31.3875</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>26</th>
      <td>7.2250</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>27</th>
      <td>263.0000</td>
      <td>Platinum class</td>
    </tr>
    <tr>
      <th>28</th>
      <td>7.8792</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>29</th>
      <td>7.8958</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>30</th>
      <td>27.7208</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>31</th>
      <td>146.5208</td>
      <td>premium class</td>
    </tr>
    <tr>
      <th>32</th>
      <td>7.7500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>33</th>
      <td>10.5000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>34</th>
      <td>82.1708</td>
      <td>2nd_AC_class</td>
    </tr>
    <tr>
      <th>35</th>
      <td>52.0000</td>
      <td>Sleeper class</td>
    </tr>
    <tr>
      <th>36</th>
      <td>7.2292</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>37</th>
      <td>8.0500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>38</th>
      <td>18.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>39</th>
      <td>11.2417</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>40</th>
      <td>9.4750</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>41</th>
      <td>21.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>42</th>
      <td>7.8958</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>43</th>
      <td>41.5792</td>
      <td>Sleeper class</td>
    </tr>
    <tr>
      <th>44</th>
      <td>7.8792</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>45</th>
      <td>8.0500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>46</th>
      <td>15.5000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>47</th>
      <td>7.7500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>48</th>
      <td>21.6792</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>49</th>
      <td>17.8000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>50</th>
      <td>39.6875</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>51</th>
      <td>7.8000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>52</th>
      <td>76.7292</td>
      <td>2nd_AC_class</td>
    </tr>
    <tr>
      <th>53</th>
      <td>26.0000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>54</th>
      <td>61.9792</td>
      <td>Sleeper class</td>
    </tr>
    <tr>
      <th>55</th>
      <td>35.5000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>56</th>
      <td>10.5000</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>57</th>
      <td>7.2292</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>58</th>
      <td>27.7500</td>
      <td>General class</td>
    </tr>
    <tr>
      <th>59</th>
      <td>46.9000</td>
      <td>Sleeper class</td>
    </tr>
  </tbody>
</table>
</div>




```python
ps.sqldf("select distinct a.Survived from a")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Survived</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
a
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>887</td>
      <td>0</td>
      <td>2</td>
      <td>Montvila, Rev. Juozas</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>211536</td>
      <td>13.0000</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>887</th>
      <td>888</td>
      <td>1</td>
      <td>1</td>
      <td>Graham, Miss. Margaret Edith</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>112053</td>
      <td>30.0000</td>
      <td>B42</td>
      <td>S</td>
    </tr>
    <tr>
      <th>888</th>
      <td>889</td>
      <td>0</td>
      <td>3</td>
      <td>Johnston, Miss. Catherine Helen "Carrie"</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>W./C. 6607</td>
      <td>23.4500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>889</th>
      <td>890</td>
      <td>1</td>
      <td>1</td>
      <td>Behr, Mr. Karl Howell</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>111369</td>
      <td>30.0000</td>
      <td>C148</td>
      <td>C</td>
    </tr>
    <tr>
      <th>890</th>
      <td>891</td>
      <td>0</td>
      <td>3</td>
      <td>Dooley, Mr. Patrick</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>370376</td>
      <td>7.7500</td>
      <td>NaN</td>
      <td>Q</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 12 columns</p>
</div>




```python

```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_7856/634118806.py in <module>
    ----> 1 ps.sqldf('''select a.Age,a.Fare,b.code,
          2          sum(a.Age)as traveller_age,
          3          max(a.Age)as maximum_age,
          4          min(a.Age)as minimum_age,
          5          avg(a.Age)as Average_age,
    

    ~\AppData\Local\Programs\Python\Python310\lib\site-packages\pandasql\sqldf.py in sqldf(query, env, db_uri)
        154     >>> sqldf("select avg(x) from df;", locals())
        155     """
    --> 156     return PandaSQL(db_uri)(query, env)
    

    ~\AppData\Local\Programs\Python\Python310\lib\site-packages\pandasql\sqldf.py in __call__(self, query, env)
         56                     continue
         57                 self.loaded_tables.add(table_name)
    ---> 58                 write_table(env[table_name], table_name, conn)
         59 
         60             try:
    

    ~\AppData\Local\Programs\Python\Python310\lib\site-packages\pandasql\sqldf.py in write_table(df, tablename, conn)
        119                        message='The provided table name \'%s\' is not found exactly as such in the database' % tablename)
        120         to_sql(df, name=tablename, con=conn,
    --> 121                index=not any(name is None for name in df.index.names))  # load index into db if all levels are named
        122 
        123 
    

    AttributeError: 'dict' object has no attribute 'index'



```python
b={'code':['S','C','Q'],'city':['Mumbai','Pune','Chennai']}
```


```python
b=pd.DataFrame(b)
```


```python
b
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>code</th>
      <th>city</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>S</td>
      <td>Mumbai</td>
    </tr>
    <tr>
      <th>1</th>
      <td>C</td>
      <td>Pune</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Q</td>
      <td>Chennai</td>
    </tr>
  </tbody>
</table>
</div>




```python
ps.sqldf('''select a.Embarked,a.Sex,b.city,
         sum(a.Age)as traveller_age,
         max(a.Age)as maximum_age,
         min(a.Age)as minimum_age,
         avg(a.Age)as Average_age,
         avg(a.Fare)as Average_fare
         from a
         left join b as b
         on a.Embarked=b.code
         group by a.Embarked,a.Sex,b.city''')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Embarked</th>
      <th>Sex</th>
      <th>city</th>
      <th>traveller_age</th>
      <th>maximum_age</th>
      <th>minimum_age</th>
      <th>Average_age</th>
      <th>Average_fare</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>None</td>
      <td>female</td>
      <td>None</td>
      <td>100.00</td>
      <td>62.0</td>
      <td>38.00</td>
      <td>50.000000</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>C</td>
      <td>female</td>
      <td>Pune</td>
      <td>1729.00</td>
      <td>60.0</td>
      <td>0.75</td>
      <td>28.344262</td>
      <td>75.169805</td>
    </tr>
    <tr>
      <th>2</th>
      <td>C</td>
      <td>male</td>
      <td>Pune</td>
      <td>2276.92</td>
      <td>71.0</td>
      <td>0.42</td>
      <td>32.998841</td>
      <td>48.262109</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Q</td>
      <td>female</td>
      <td>Chennai</td>
      <td>291.50</td>
      <td>39.0</td>
      <td>15.00</td>
      <td>24.291667</td>
      <td>12.634958</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Q</td>
      <td>male</td>
      <td>Chennai</td>
      <td>495.00</td>
      <td>70.5</td>
      <td>2.00</td>
      <td>30.937500</td>
      <td>13.838922</td>
    </tr>
    <tr>
      <th>5</th>
      <td>S</td>
      <td>female</td>
      <td>Mumbai</td>
      <td>5165.50</td>
      <td>63.0</td>
      <td>1.00</td>
      <td>27.771505</td>
      <td>38.740929</td>
    </tr>
    <tr>
      <th>6</th>
      <td>S</td>
      <td>male</td>
      <td>Mumbai</td>
      <td>11147.25</td>
      <td>80.0</td>
      <td>0.67</td>
      <td>30.291440</td>
      <td>21.711996</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
