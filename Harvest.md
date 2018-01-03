## 2017 时间轴
- for循环的应用，求取各个位数的数字
      - 百位数除以100，可以取得百位数上的数字
      - 百位数除以10取余可以，取得个位上的数字
      - 百位数除以10，取整，将百位数转变为十位数，再除以10取余数，可以的十位数
      
## 2017/12/29 9:31:42
- 如何获取一个数组中的序号对称值：
     - q:[].Length-1-i(q,i为序号)
     - 学会分析：尝试将一组数据逐个写出来，观察其中的规律

## 2017/12/30 9:39:29 
- C++的输入与输出，计算机案列：
     - 引入类库:`#include <iostream>` 
     - 输出：`cout <<`
     - 输入：`cin >>`
     - 命名空间与库的关系：
          - 在C++中被整理好方便引入使用的所有库为标准库
          - 命名空间：`using namespace std;` **std**是c++标准库中的所有标识符所定义的地方（在std中定义了各种库和方法），因此它们存在的关系：std>c++标准库
          - 另类写法可在标识符前添加命名空间名+“：：”：`std::cout`

## 2017/12/31 1:51:30 
- 板绘--手部临摹，发现画画先将图形以几何体的方式打草稿，再细致地画，效率会更高；
- C#,函数的写法和调用。
- C++，cin.get(),可以暂停控制台，直到接受下一个命令。
- Gist的使用方法，申请Gist仓库，获取对应的Access_Token码和Gist_id

## 2018/1/1 10:30:54 
- 关于`bool`的类型的编程方法实际应用理解，判断当前某个对象的当前如何


 ```c#    
            bool isDead=true;
            if（isDead）{
            cout<<"游戏结束处理"<<endl；
            } 
```
- c++中给一个变量在控制台输入：
```c#   
         int a;//声明变量
         cin>>a;//在控制台中赋值
```

- 参数数组（**Params**）与数组参数的区别      
      - 数组参数，正常的参数方法，需要根据定义的参数，匹配需需要用到的数据，自定义构造数组
      - 参数数组（**Params**）， 添加关键字（**Params**），让多个数据输入时，自动编译成数组，免去用户自定义构造数组（同时如果接受的数据是一个数组也可以接受）
  

  
## 2018/1/2 21:15:28
-  结构函数，存放于结构体内的函数为结构函数。结构体，用于存放一些常用的变量（在结构体内称为属性），同时也可以存放函数方法，该函数方法也可以直接使用结构体内的属性名:bowtie:
 
```c#
        struct CustomerName
        {
           //结构体，用于存储一些常用的变量的名（在结构体自身来说，这是它自己的属性）
           public Name firstName;
           public Name lastName;

           public string GetName()

           {
                return firstName + " " + lastName;
           }
        }
```

- switch语句中多个case调用相同的方法体写法：

```c#
        switch (num)
            {
            case 0:
            Console.WriteLine("当前战斗中");
            break;
                case 1:
                    Console.WriteLine("游戏暂停");
                    break;
                case 2:
                    Console.WriteLine("游戏胜利");
                    break;
                case 3:
                    Console.WriteLine("游戏失败");
                    break;
                case 4:
                //case 5:   当两个case语句放在一起，显示同样的结果
                    Console.WriteLine("游戏失败");
                    break;
                default:
                    Console.WriteLine("当前state超出了游戏状态的取值范围");
                    break;
                                }


```

- Markdown github扩展语法
  - 不同程序语句的高亮显示
  - 清单列表（- [x] \(option) content） 
  

1/3/2018 3:01:37 PM 
- **函数的重载**  函数重新加载方法体
    - 两个函数的函数体方法不变
    - 两个函数的名字一致
    - 两个函数的变量数据类型不一样

**原函数:**
```c#
static int Plus(params int[] array){
            int sum=0;
            for (int i = 0; i < array.Length; i++)
            {
                sum +=array[i];
            }
            return sum;
        }

```

**重载的函数:**
```c#
static double Plus(params double[] array){
            double sum=0;
            for (int i = 0; i < array.Length; i++)
            {
                sum +=array[i];
            }
            return sum;
        }
```
**调用函数:**
```c#
 static void Main(string[] args)
        {
            int sum=Plus(45,52,45,24,52);
            double sum2=Plus(45.2,45,2,2.3);
            Console.Write(sum+"\n"+sum2);
        }
```