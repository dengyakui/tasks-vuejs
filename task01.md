## 选择题：
1. A,B,C,D
2. B

## 简答题：
请简述 patchVnode 函数的执行过程

1. 执行 prepatch 钩子函数
2. 执行update钩子函数
3. 如果新节点有text属性且不等于旧节点，将文字更新到dom节点上
4. 获取新，旧节点的children子元素，
   - 如果都有子元素，且不相等，执行updateChildren更新子元素
   - 如果新节点有children， 旧节点没有，且有text属性，清空旧节点dom的text & 将新节点的children插入到dom节点下
   - 如果新节点没有children，旧节点有children，清空dom的childre元素
   - 如果新旧节点都没有children，且旧节点有text， 清空dom的text
5. 调用 postpatch 钩子函数
