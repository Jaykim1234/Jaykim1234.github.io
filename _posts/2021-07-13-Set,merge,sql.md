 

## **Set**

![image-20210713122917920](C:\Users\USER01\AppData\Roaming\Typora\typora-user-images\image-20210713122917920.png)

**data** tmp_data1;

​    set c.ctbs0413_02_disease;

​    set c.ctbs0413_04_drug;

**run**;



**proc** **contents** data=tmp_data1 ; **run**;

 

![image-20210713122828899](C:\Users\USER01\AppData\Roaming\Typora\typora-user-images\image-20210713122828899.png)

**data** tmp_data2;

​    set c.ctbs0413_02_disease c.ctbs0413_04_drug;

**run**;

 

**proc** **contents** data=tmp_data2 ; **run**;

![image-20210713122838956](C:\Users\USER01\AppData\Roaming\Typora\typora-user-images\image-20210713122838956.png)

**data** tmp_data3;

​    set c.ctbs0413_02_disease c.ctbs0413_04_drug;

​    by DS1_ASTH

run;

![image-20210713122848568](C:\Users\USER01\AppData\Roaming\Typora\typora-user-images\image-20210713122848568.png)

**data** tmp_data3;

​    MERGE c.ctbs0413_02_disease c.ctbs0413_04_drug;

​    by DS1_ASTH

run;

Source

https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=hsj2864&logNo=220624094325



## SQL

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

**PROC** **SQL**;

CREATE TABLE TMP_TEST AS

SELECT C.DS1_ALLER C.DS1_ALLERAG C.DS1_ASTH

FROM C. tmp_data3;

**QUIT**;