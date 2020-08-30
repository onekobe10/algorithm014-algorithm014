### 1. Java 递归模板
```
public void recur(int level, int param) { 
  // terminator 
  if (level > MAX_LEVEL) { 
    // process result 
    return; 
  }
  // process current logic 
  process(level, param); 
  // drill down 
  recur( level: level + 1, newParam); 
  // restore current status 
 
}
```

### 2. 总结
1. 头递归如果不使用缓存则时间复杂度比较高
2. 使用尾递归从低到高计算每个计算出来的结果都立刻使用到，比头递归效率更高
3. 避免人肉递归，只找最小重复单元