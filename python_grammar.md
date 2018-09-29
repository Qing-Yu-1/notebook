### np.random.choice的用法
```
import numpy as np

# 参数意思分别 是从a 中以概率P，随机选择3个, p没有指定的时候相当于是一致的分布
a1 = np.random.choice(a=5, size=3, replace=False, p=None)
print(a1)
# 非一致的分布，会以多少的概率提出来
a2 = np.random.choice(a=5, size=3, replace=False, p=[0.2, 0.1, 0.3, 0.4, 0.0])
print(a2)
# replacement 代表的意思是抽样之后还放不放回去，如果是False的话，那么出来的三个数都不一样，如果是True的话， 有可能会出现重复的，因为前面的抽的放回去了
```
### 统计字符出现的次数
```python
a = '小明456fgdddhhh55adbyjjjjj'
m ={}
for ch in a :       # 从a字符串里面取值
    if ch in m :        # 取出来的值如果在 m 里面
        m[ch] +=1      # m字典里面的元素 统计加1
    else:
        m[ch] =1
print(m)

#输出
{'小': 1, '明': 1, '4': 1, '5': 3, '6': 1, 'f': 1, 'g': 1, 'd': 4, 'h': 3, 'a': 1, 'b': 1, 'y': 1, 'j': 5}
```
### 整型强制转换
```
整型使用整型强制转换之后还是整型
```
