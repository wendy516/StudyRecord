### 自定义View



#### 知识点1：MeasureSpec

* exactly   ：确切的大小  

* at_most ：大小不可超过某数值，如match_parent，最大不能超过你爸爸

* UNSPECIFIED ：不对View大小做限制，系统使用

```
android:layout_width="100dp" //exactly     
android:layout_width="match_parent" //at_most
android:layout_width="wrap_content"
```



#### 面试题

**Q1：LayoutParams 是什么？与MeasureSpec有关系吗？**



