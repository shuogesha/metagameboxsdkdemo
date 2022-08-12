# metagameboxsdkdemo
metagameboxsdk Android sdk demo project

#Apache Maven
maven.apache.org 


```
<dependency>
  <groupId>io.github.shuogesha</groupId>
  <artifactId>metagameboxsdk</artifactId>
  <version>0.1.0</version>
  <type>aar</type>
</dependency>


```


#Gradle Groovy DSL
gradle.org 


```
implementation 'io.github.shuogesha:metagameboxsdk:0.1.0'

```


#Gradle Kotlin DSL
github.com/gradle/kotlin-dsl



```
implementation("io.github.shuogesha:metagameboxsdk:0.1.0")


```


#问题：安卓11、sdk29以上无法调起，AndroidManifest.xml配置如下：


```
<queries> 
    <package android:name="com.metadreamer.MetaGameBox" />
</queries>

```



```
平台版本	SDK版本	版本名称
Android Sv2 Preview	Sv2	Preview
Android 12.0	30	S
Android 11.0	29	R
Android 10.0	28	Q
Android 9.0	27	Pie
Android 8.0  	 26  	 Oreo
Android 7.1	25	 Nougat
Android 7.0	24	 Nougat
Android 6.0	23	Marshmallow
Android 5.1	22	Lollipop
Android 5.0	21	Lollipop
Android 4.4	19	  KITKAT
Android 4.3	18	JELLY_BEAN_MR2
Android 4.2, 4.2.2	17	JELLY_BEAN_MR1
Android 4.1, 4.1.1	16	JELLY_BEAN
Android 4.0.3, 4.0.4	15	ICE_CREAM_SANDWICH_MR1
Android 4.0, 4.0.1, 4.0.2	14	 ICE_CREAM_SANDWICH
Android 3.2	13	HONEYCOMB_MR2
Android 3.1.x	12	HONEYCOMB_MR1
Android 3.0.x	11	HONEYCOMB
Android 2.3.4	10	GINGERBREAD_MR1
Android 2.3.3	    10 	GINGERBREAD_MR1
Android 2.3.2 	9	GINGERBREAD
Android 2.3.1	9	 GINGERBREAD
Android 2.3	9	   GINGERBREAD
Android 2.2.x 	8	 FROYO
Android 2.1.x	7	 ECLAIR_MR1
Android 2.0.1 	6	 ECLAIR_0_1
Android 2.0 	5	ECLAIR
Android 1.6  	4	DONUT
Android 1.5	3	 CUPCAKE
Android 1.1	2	 BASE_1_1
Android 1.0	1	BASE 

```
