```flow
st=>start: start
op=>operation: 选取结点构建数组
op1=>operation: 按顺序选取节点
cond1=>condition: 大于父节点&&未达到最顶端？
op2=>operation: 与父节点交换
cond2=>condition: 是否遍历所有结点？
op3=>operation: “删除”最顶端值
op4=>operation: 依次判断两个子节点大小，层层将较大值覆盖父节点
cond3=>condition: 是否到底部?
op5=>operation: 将之前的最大值覆盖数组底部
cond4=>condition: 所有元素已重组排序结束？
e=>end

st->op->op1->cond1
cond1(yes)->op2
cond1(no)->cond2
cond2(yes)->op3
cond2(no)->op1
op3->op4->cond3
cond3(yes)->op5
cond3(no)->op4
op5->cond4
cond4(yes)->e
cond4(no)->op3
```

