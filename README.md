ThemeColor
========

图像主题色提取（中位切分法），代码参考了 js 库 [quantize](https://github.com/olivierlesnicki/quantize)


使用
-------

```java
int[][] arrayOfPixels = new int[][]{
    {190, 197, 190},
    {202, 204, 200},
    {207, 214, 210},
    {211, 214, 211},
    {205, 207, 207}
};
int maximumColorCount = 4;

MMCQ mmcq = new MMCQ(arrayOfPixels, maximumColorCount);

```

- arrayOfPixels：要提取主题色的RGB像素数组
- maxiumColorCount：提取的主题颜色数量

palette() 方法返回主题颜色数组

``` java
List<int[]> palette = mmcq.palette();
// [[204, 204, 204], [208,212,212], [188,196,188], [212,204,196]]
```

map(pixel) 方法返回最接近 pixel 的主题色

``` java
mmcq.map(arrayOfPixels[0]);
// [188,196,188]
```



License
-------

Licensed under the MIT License.
