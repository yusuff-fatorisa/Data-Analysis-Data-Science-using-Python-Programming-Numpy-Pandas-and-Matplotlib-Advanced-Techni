### Hello, welcome to another lesson on python and the data science libraries ( Numpy, Pandas and Matplotlib). This is another dummy dataset that i worked on as i learned and grow on this career path. I want you to connect deeply with these dataset and feel encouraged about what you're doing. We all do it a little poorly until we get better. That's why i share my journey and my growth process. 

## So, Let's get started !!!

### The first step is to import numpy and pandas libraries and load in the dataset. I also read the first 10 lines of the imported data as well as the last 10 using the .head() and .tail() functions respectively. This is for me to have an idea of wha my Dataset looks like.


```python
import numpy as np
import pandas as pd
filez = pd.read_excel("Excursion Portfolio.xls")
filez.head(10)
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
      <th>Unnamed: 0</th>
      <th>Unnamed: 1</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
      <th>Unnamed: 6</th>
      <th>Unnamed: 7</th>
      <th>Unnamed: 8</th>
      <th>Unnamed: 9</th>
      <th>Unnamed: 10</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>3</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>S/N</td>
      <td>Name</td>
      <td>Status</td>
      <td>Amount Paid</td>
      <td>T-shirt</td>
      <td>NaN</td>
      <td>Comments</td>
    </tr>
    <tr>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Type</td>
      <td>Amount</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>6</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>7</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2</td>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>9</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4</td>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez.tail(10)
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
      <th>Unnamed: 0</th>
      <th>Unnamed: 1</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
      <th>Unnamed: 6</th>
      <th>Unnamed: 7</th>
      <th>Unnamed: 8</th>
      <th>Unnamed: 9</th>
      <th>Unnamed: 10</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>48</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>43</td>
      <td>Shekinah Ajibola</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>49</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>44</td>
      <td>Adanu David</td>
      <td>Member</td>
      <td>9000</td>
      <td>NIL</td>
      <td>NIL</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>50</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>45</td>
      <td>Oche Muscle</td>
      <td>Member</td>
      <td>9500</td>
      <td>NIL</td>
      <td>NIL</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>51</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>46</td>
      <td>Ocheje Jeremiah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>52</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>47</td>
      <td>Oguntowo Basit Ifedolapo</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>53</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>48</td>
      <td>Simeon Iganga</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100 Level</td>
    </tr>
    <tr>
      <td>54</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49</td>
      <td>Caleb Onuoja Aaron</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>55</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TOTAL</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>537500</td>
      <td>NaN</td>
      <td>80700</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>56</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>57</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Total Members Registered</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



### I also checked other properties of the dataset which includes its shape size dimension and the data types respectively


```python
filez.shape
```




    (58, 11)




```python
filez.size
```




    638




```python
filez.ndim
```




    2




```python
filez.dtypes
```




    Unnamed: 0     float64
    Unnamed: 1     float64
    Unnamed: 2     float64
    Unnamed: 3     float64
    Unnamed: 4      object
    Unnamed: 5      object
    Unnamed: 6      object
    Unnamed: 7      object
    Unnamed: 8      object
    Unnamed: 9      object
    Unnamed: 10     object
    dtype: object



### Next, i renamed the columns of the dataset to make it more relatable. And after that i deleted the columns that contains unrelevant information ( the columns that contained "nan" in all its rows)


```python
filez.columns = ['COL1','COL2','COL3','COL4','S/N','NAME','STATUS','AMOUNT_PAID','TSHIRT_TYPE','TSHIRT_AMOUNT','COMMENTS']
```


```python
filez.head(15)
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
      <th>COL1</th>
      <th>COL2</th>
      <th>COL3</th>
      <th>COL4</th>
      <th>S/N</th>
      <th>NAME</th>
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
      <th>COMMENTS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>3</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>S/N</td>
      <td>Name</td>
      <td>Status</td>
      <td>Amount Paid</td>
      <td>T-shirt</td>
      <td>NaN</td>
      <td>Comments</td>
    </tr>
    <tr>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Type</td>
      <td>Amount</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>6</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>7</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2</td>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3</td>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>9</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4</td>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>10</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5</td>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>11</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6</td>
      <td>Adole John A.</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>12</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7</td>
      <td>Faleti Ayodeji Peter</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>13</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8</td>
      <td>Ayantoye Ridwan Ayomide</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>9</td>
      <td>Marvellous  T. Isaac</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez1 = filez.drop(['COL1','COL2','COL3','COL4','S/N','COMMENTS'], axis =1)
```


```python
filez1.head(15)
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
      <th>NAME</th>
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>3</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Name</td>
      <td>Status</td>
      <td>Amount Paid</td>
      <td>T-shirt</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Type</td>
      <td>Amount</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Adole John A.</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Faleti Ayodeji Peter</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Ayantoye Ridwan Ayomide</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>14</td>
      <td>Marvellous  T. Isaac</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez1.tail(10)
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
      <th>NAME</th>
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>48</td>
      <td>Shekinah Ajibola</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>49</td>
      <td>Adanu David</td>
      <td>Member</td>
      <td>9000</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>50</td>
      <td>Oche Muscle</td>
      <td>Member</td>
      <td>9500</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>51</td>
      <td>Ocheje Jeremiah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>52</td>
      <td>Oguntowo Basit Ifedolapo</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>53</td>
      <td>Simeon Iganga</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>54</td>
      <td>Caleb Onuoja Aaron</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>55</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>537500</td>
      <td>NaN</td>
      <td>80700</td>
    </tr>
    <tr>
      <td>56</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>57</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



### Next , i dropped all the rows which contains "nan" all across the dataset or unrelevant data


```python
filez2 = filez1.drop([ 0,1,2,3,4,5,55,56,57])
```


```python
filez2.head(10)
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
      <th>NAME</th>
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>6</td>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Adole John A.</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Faleti Ayodeji Peter</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Ayantoye Ridwan Ayomide</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>14</td>
      <td>Marvellous  T. Isaac</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>15</td>
      <td>Shenge Raphael Saarshatar</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez2.tail(10)
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
      <th>NAME</th>
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>45</td>
      <td>Daleng Elisha Nandi</td>
      <td>Member</td>
      <td>9000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>46</td>
      <td>Ukande Aondongu Cephas</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>47</td>
      <td>De-Gold David Tarki</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>48</td>
      <td>Shekinah Ajibola</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>49</td>
      <td>Adanu David</td>
      <td>Member</td>
      <td>9000</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>50</td>
      <td>Oche Muscle</td>
      <td>Member</td>
      <td>9500</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>51</td>
      <td>Ocheje Jeremiah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>52</td>
      <td>Oguntowo Basit Ifedolapo</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>53</td>
      <td>Simeon Iganga</td>
      <td>Member</td>
      <td>12000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>54</td>
      <td>Caleb Onuoja Aaron</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



### Next, I made the "NAME" column the Index label. And i dropped the column after this step

#### Note that this step of setting a column as an index can also be achieved by using the "set_index()" method will you'll learn in later lessons


```python
filez2.index = filez2["NAME"]
```


```python
filez2.head()
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
      <th>NAME</th>
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
    <tr>
      <th>NAME</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Victor T. Na'Allah</td>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Olajide Mattew</td>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Abel Modu Timothy</td>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Egwim Jones Udojuaku</td>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez3 = filez2.drop("NAME", axis = "columns")
```


```python
filez3.head()
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
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
    <tr>
      <th>NAME</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez3.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 49 entries, Victor T. Na'Allah to Caleb Onuoja Aaron
    Data columns (total 4 columns):
    STATUS           49 non-null object
    AMOUNT_PAID      48 non-null object
    TSHIRT_TYPE      39 non-null object
    TSHIRT_AMOUNT    39 non-null object
    dtypes: object(4)
    memory usage: 980.0+ bytes


### Next i checked if there are null values on the Dataset and where excatly they are located


```python
filez3.isnull().sum()
```




    STATUS            0
    AMOUNT_PAID       1
    TSHIRT_TYPE      10
    TSHIRT_AMOUNT    10
    dtype: int64




```python
filez3["AMOUNT_PAID"].head(10)
```




    NAME
    Victor T. Na'Allah             12000
    Olajide Mattew                 12000
    Abel Modu Timothy              12000
    Egwim Jones Udojuaku           12000
    Nwachukwu Emmanuel Benedict    12000
    Adole John A.                  12000
    Faleti Ayodeji Peter           12000
    Ayantoye Ridwan Ayomide        12000
    Marvellous  T. Isaac           12000
    Shenge Raphael Saarshatar      12000
    Name: AMOUNT_PAID, dtype: object



### I filled the null values in the "AMOUNT PAID" column with 0, and set inplace to be True. And i checked to confirm if the change has been effected


```python
filez3["AMOUNT_PAID"].fillna(0, inplace = True)
```


```python
filez3.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 49 entries, Victor T. Na'Allah to Caleb Onuoja Aaron
    Data columns (total 4 columns):
    STATUS           49 non-null object
    AMOUNT_PAID      49 non-null int64
    TSHIRT_TYPE      39 non-null object
    TSHIRT_AMOUNT    39 non-null object
    dtypes: int64(1), object(3)
    memory usage: 1.1+ KB



```python
filez3["TSHIRT_TYPE"].head()
```




    NAME
    Victor T. Na'Allah             Long Sleeve
    Olajide Mattew                 Long Sleeve
    Abel Modu Timothy              Long Sleeve
    Egwim Jones Udojuaku           Long Sleeve
    Nwachukwu Emmanuel Benedict    Long Sleeve
    Name: TSHIRT_TYPE, dtype: object



### If filled the null values contained in the "T-SHIRT TYPE" column with Long Sleeve and set inplace to True.
### I replaced the null values contained in "T-SHIRT AMOUNT" accordingly

#### I also checked to comfirm the change has been effected


```python
filez3["TSHIRT_TYPE"].fillna("Long Sleeve", inplace = True)
```


```python
filez3.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 49 entries, Victor T. Na'Allah to Caleb Onuoja Aaron
    Data columns (total 4 columns):
    STATUS           49 non-null object
    AMOUNT_PAID      49 non-null int64
    TSHIRT_TYPE      49 non-null object
    TSHIRT_AMOUNT    39 non-null object
    dtypes: int64(1), object(3)
    memory usage: 1.1+ KB



```python
filez3["TSHIRT_AMOUNT"].head()
```




    NAME
    Victor T. Na'Allah             2500
    Olajide Mattew                 2500
    Abel Modu Timothy              2500
    Egwim Jones Udojuaku           2500
    Nwachukwu Emmanuel Benedict    2500
    Name: TSHIRT_AMOUNT, dtype: object




```python
filez3["TSHIRT_AMOUNT"].fillna(2500, inplace = True)
```


```python
filez3.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 49 entries, Victor T. Na'Allah to Caleb Onuoja Aaron
    Data columns (total 4 columns):
    STATUS           49 non-null object
    AMOUNT_PAID      49 non-null int64
    TSHIRT_TYPE      49 non-null object
    TSHIRT_AMOUNT    49 non-null object
    dtypes: int64(1), object(3)
    memory usage: 1.1+ KB



```python
filez3
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
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
    <tr>
      <th>NAME</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Adole John A.</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Faleti Ayodeji Peter</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Ayantoye Ridwan Ayomide</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Marvellous  T. Isaac</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Shenge Raphael Saarshatar</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Reuben O.Enoch</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Mercy Ajayi</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Michael Kpoco</td>
      <td>Ex-Exco</td>
      <td>7000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Saad</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Terzungwe Caleb</td>
      <td>Ex-Exco</td>
      <td>5000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Faith</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Gonet Zion</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Hawwau Adeboyin Adeyemo\nFor =&gt; Jubrin Omeiza</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nicholas Otonoku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Timothy Ignitus Agbor</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Madumche Chidibere</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nwokocha Ethelbert</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Effiong Ubon Alasi</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Daniel Overcomer</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Aguwa Wisdom</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Ganiyu Mujeeb</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Hezekiel Joel</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Shitu Mustapha Ibrahim</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Orogu Francis Israel</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Agha Elizabeth</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Muhammed Zainab</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Isaac Priscilla</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Paul Elizabeth Ladi</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Omaji Samuel Owoicho</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Esinome Abraham</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Umeh Audu Ayigba</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Sarah Kauna Edoja</td>
      <td>Member</td>
      <td>8000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Ibrahim Hussein Chado</td>
      <td>Member</td>
      <td>10000</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>Fatima Ganiyu</td>
      <td>Member</td>
      <td>0</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>Daleng Elisha Nandi</td>
      <td>Member</td>
      <td>9000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Ukande Aondongu Cephas</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>De-Gold David Tarki</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Shekinah Ajibola</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Adanu David</td>
      <td>Member</td>
      <td>9000</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>Oche Muscle</td>
      <td>Member</td>
      <td>9500</td>
      <td>NIL</td>
      <td>NIL</td>
    </tr>
    <tr>
      <td>Ocheje Jeremiah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Oguntowo Basit Ifedolapo</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Simeon Iganga</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Caleb Onuoja Aaron</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez3["TSHIRT_TYPE"].unique()
```




    array(['Long Sleeve', 'Short Sleeve', 'NIL'], dtype=object)




```python
filez3["TSHIRT_AMOUNT"].unique()
```




    array([2500, 2100, 'NIL'], dtype=object)



### Checking the info of the Dataset, it's revealed that there are some values that are wrong. Like "NIL", and they are replaced accordingly using the replace function.

#### Note that this not a null value and requires a different treatment from "nan". If it were to be null values, "dropna" / "fillna" wolud have taken care of it


```python
filez3["TSHIRT_TYPE"].replace({"NIL" : "No Sleeve"}, inplace = True)

```


```python
filez3["TSHIRT_AMOUNT"].replace({"NIL" : 0}, inplace = True)
```


```python
filez3
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
      <th>STATUS</th>
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_TYPE</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
    <tr>
      <th>NAME</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Victor T. Na'Allah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Olajide Mattew</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Abel Modu Timothy</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Egwim Jones Udojuaku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nwachukwu Emmanuel Benedict</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Adole John A.</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Faleti Ayodeji Peter</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Ayantoye Ridwan Ayomide</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Marvellous  T. Isaac</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Shenge Raphael Saarshatar</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Reuben O.Enoch</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Mercy Ajayi</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Michael Kpoco</td>
      <td>Ex-Exco</td>
      <td>7000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Saad</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Terzungwe Caleb</td>
      <td>Ex-Exco</td>
      <td>5000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Faith</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Gonet Zion</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Hawwau Adeboyin Adeyemo\nFor =&gt; Jubrin Omeiza</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nicholas Otonoku</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Timothy Ignitus Agbor</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Madumche Chidibere</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Nwokocha Ethelbert</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Effiong Ubon Alasi</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Daniel Overcomer</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Aguwa Wisdom</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Ganiyu Mujeeb</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Hezekiel Joel</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Shitu Mustapha Ibrahim</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Orogu Francis Israel</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Agha Elizabeth</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Muhammed Zainab</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Isaac Priscilla</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Paul Elizabeth Ladi</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Omaji Samuel Owoicho</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Esinome Abraham</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Umeh Audu Ayigba</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Sarah Kauna Edoja</td>
      <td>Member</td>
      <td>8000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Ibrahim Hussein Chado</td>
      <td>Member</td>
      <td>10000</td>
      <td>No Sleeve</td>
      <td>0</td>
    </tr>
    <tr>
      <td>Fatima Ganiyu</td>
      <td>Member</td>
      <td>0</td>
      <td>No Sleeve</td>
      <td>0</td>
    </tr>
    <tr>
      <td>Daleng Elisha Nandi</td>
      <td>Member</td>
      <td>9000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Ukande Aondongu Cephas</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>De-Gold David Tarki</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Shekinah Ajibola</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Adanu David</td>
      <td>Member</td>
      <td>9000</td>
      <td>No Sleeve</td>
      <td>0</td>
    </tr>
    <tr>
      <td>Oche Muscle</td>
      <td>Member</td>
      <td>9500</td>
      <td>No Sleeve</td>
      <td>0</td>
    </tr>
    <tr>
      <td>Ocheje Jeremiah</td>
      <td>Member</td>
      <td>12000</td>
      <td>Short Sleeve</td>
      <td>2100</td>
    </tr>
    <tr>
      <td>Oguntowo Basit Ifedolapo</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Simeon Iganga</td>
      <td>Member</td>
      <td>12000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
    <tr>
      <td>Caleb Onuoja Aaron</td>
      <td>Ex-Exco</td>
      <td>8000</td>
      <td>Long Sleeve</td>
      <td>2500</td>
    </tr>
  </tbody>
</table>
</div>



### The file is ready for analysis, visualization or any other process.


### I checked a few of its properties to double check all I've done.



```python
filez3.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 49 entries, Victor T. Na'Allah to Caleb Onuoja Aaron
    Data columns (total 4 columns):
    STATUS           49 non-null object
    AMOUNT_PAID      49 non-null int64
    TSHIRT_TYPE      49 non-null object
    TSHIRT_AMOUNT    49 non-null int64
    dtypes: int64(2), object(2)
    memory usage: 1.3+ KB



```python
filez3.describe()
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
      <th>AMOUNT_PAID</th>
      <th>TSHIRT_AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>count</td>
      <td>49.000000</td>
      <td>49.000000</td>
    </tr>
    <tr>
      <td>mean</td>
      <td>10969.387755</td>
      <td>2157.142857</td>
    </tr>
    <tr>
      <td>std</td>
      <td>2319.321388</td>
      <td>676.387463</td>
    </tr>
    <tr>
      <td>min</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <td>25%</td>
      <td>12000.000000</td>
      <td>2100.000000</td>
    </tr>
    <tr>
      <td>50%</td>
      <td>12000.000000</td>
      <td>2500.000000</td>
    </tr>
    <tr>
      <td>75%</td>
      <td>12000.000000</td>
      <td>2500.000000</td>
    </tr>
    <tr>
      <td>max</td>
      <td>12000.000000</td>
      <td>2500.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
filez3.shape
```




    (49, 4)




```python
filez3.size
```




    196




```python
filez3.dtypes
```




    STATUS           object
    AMOUNT_PAID       int64
    TSHIRT_TYPE      object
    TSHIRT_AMOUNT     int64
    dtype: object




```python
filez3.ndim
```




    2



### Now, you can write the file back into a document. In this case, i choose to write it back to an excel file


```python
filez3.to_excel("ExcurPort Document.xlsx")
```


```python

```

This document has been successfully prepared for analysis.
And I'm really excited 😁 😊😄 about that.
It's also been successfully written back to an excel file.
And that's another giant feat achieved.
I'll keep the document safe for visualization analysis when I'm done and ready with Matplotlib.
I thank God for this that I've been able to achieve.
#ThankfulHeart.
#GratefulHeart
#JourneyToGreatAndExtraordinaryFeats.
#TheBecomingOfAWorldReveredDataScientist
#TheMakingOfADataAnalyst

### This brings this lesson to an end. The best way to learn is by doing, so get started and get practicing. It's only a matter of improved effort and you'd have developed your skills to take on giant projects.

### Wishing you Goodspeed and Happy Learning


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```
