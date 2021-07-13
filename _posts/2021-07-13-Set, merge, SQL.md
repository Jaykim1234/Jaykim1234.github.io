 

## **Set**

![image](https://user-images.githubusercontent.com/78076248/125386100-ac68fc00-e3d6-11eb-8f76-cdb676efb109.png)

< **CODE** >

data tmp_data1;

​    set c.ctbs0413_02_disease;

​    set c.ctbs0413_04_drug;

run;
 
![image](https://user-images.githubusercontent.com/78076248/125386107-affc8300-e3d6-11eb-8b7f-c3381000370e.png)

< **CODE** >

data tmp_data2;

​    set c.ctbs0413_02_disease c.ctbs0413_04_drug;

run;

 

![image](https://user-images.githubusercontent.com/78076248/125386166-c7d40700-e3d6-11eb-8ef1-1882963d59f1.png)

< **CODE** >

data tmp_data3;

​    set c.ctbs0413_02_disease c.ctbs0413_04_drug;

​    by DS1_ASTH

run;


## **MERGE**

![image](https://user-images.githubusercontent.com/78076248/125386154-c276bc80-e3d6-11eb-955c-c7be88e8c9cc.png)

< **CODE** >

data tmp_data3;

​    MERGE c.ctbs0413_02_disease c.ctbs0413_04_drug;

​    by DS1_ASTH

run;


## **SQL**

![image](https://user-images.githubusercontent.com/78076248/125386182-d02c4200-e3d6-11eb-8a48-7d9ea2b50934.png)

< **CODE** >

PROC SQL;

CREATE TABLE TMP_TEST AS

SELECT C.DS1_ALLER C.DS1_ALLERAG C.DS1_ASTH

FROM C. tmp_data3;

QUIT;


Source

https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=hsj2864&logNo=220624094325
