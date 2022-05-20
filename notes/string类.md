## string类:

1. 初始化: 

    ​	string str = "123123"; 

    ​	string str("123123"); 

    ​	string str(char, count); //初始化count个char字符

    ​	//**特别的, 虽然不能用某个字符初始化string对象, 但是可以给其赋值**

    

2. 常用函数: 

    ​	特别的: 

    ​		1). 如果可操作的字符个数不足num个, 则会操作至串尾.

    ​		2). *count: 如果查找的内容为一个字符串, 则查找内容改为**内容串的前count个字符**.  (感觉不常用, 就不写在表格了.)
    
    注: 表格中带*的为有默认填充值, npos表示unsigned int的最大值(可以认为是到串尾)

|                函数名称                 |                           函数作用                           |        默认参数         |
| :-------------------------------------: | :----------------------------------------------------------: | :---------------------: |
|      ==getline(cin, str, \*终止字符)==      |                 **读取字符**直至读到终止字符                 |          '\n'           |
|        ==str.length() / str.size()==        |                        得到字符串长度                        |          NULL           |
|  ==str.assign(目标串, *index, *num)==   |             **拷贝串**, 从index开始连续num个字符             | *index = 0, *num = npos |
|  ==str.append(目标串, *index, *num)==   |       **追加串**, 将目标串从下标index开始追加num个字符       | *index = 0, *num = npos |
|      ==str.substr(*index, *num)==       |            **得到子串**, 以index开始连续num个字符            | *index = 0, *num = npos |
| ==str.c_str()== | **得到传统C语言的字符串**, 返回类型是const char*, 且以'\0'结尾. |  |
|   ==str.find(内容, *index, *count)==    | **找查字符(串)**, 在串中从下标index开始, 从前往后找查. 若成功找查, 则返回首次出现的下标, 否则返回npos. |       *index = 0        |
|     str.rfind(内容, *index, *count)     | **找查字符(串)**, 在串中从下标index开始, 从后往前找查. 若成功找查, 则返回首次出现的下标, 否则返回npos. |       *index = npos       |
| str.find_first_of(内容, *index, *count) | **找查字符**, 从前往后, 查找的内容为一个字符串, 则返回**字符串中任一字符**首次出现的下标. |       *index = 0        |
| str.find_last_of(内容, *index, *count)  | **找查字符**, 同理于find_first_of(), 从后往前, 找查内容字符首次出现的下标 | *index = npos |
|         str.find_first_not_of(内容, *index, *count)          | **找查字符**, 从前往后, 找查不在内容串中的字符首次出现的下标. |       *index = 0        |
|          str.find_last_not_of(内容, *index, *count)          | **找查字符**, 从后往前, 找查不在内容串中的字符首次出现的下标. |      *index = npos      |
| str.erase(begin(), end()); earse(index, num); erase(iterator); |          **删除字符(串)**, 也可以删除部分. 自由发挥          |           略            |
|                        str.replace()                         | **替换字符(串)**, 自由发挥, 例子str.replace(1, 4, "123456",4, 5) |           略            |
|                         str.insert()                         |                  **插入字符(串)**, 自由发挥                  |           略            |

	3. 字符串流处理: 有 istringstream和 ostringstream. 也可以用stringstream.


