# PowerDesigner使用问题 #
## CheckModel遇到的问题 ##
### Reference do not have unique constraint name ###
- 原因：reference中的constraint name 重复
- 解决方法:双击reference 在 Integrity中吧constraint name 改成唯一

### references are reflexive and mandatory ###
- 原因：在reference的Integrity里勾上了Mandatory parent
- 解决方法：把勾去掉

### Object(cls_table) name(T_BCM_TEMPALTE) object reference not set to an instance of an object###
- 原因：索引定义加了一行，但是没有加上具体的列
- 解决方法：给索引加上具体的列






