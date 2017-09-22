### ELA
ELA 全称：Error Level Analysis ，汉译为“错误级别分析”或者叫“误差分析”。通过检测特定压缩比率重新绘制图像后造成的误差分布，可用于识别JPEG图像的压缩。
[维基百科](https://en.wikipedia.org/wiki/Error_level_analysis)：ELA是对JPEG有损压缩的数字数据中的压缩影像进行分析。
这个领域的专家非 [Neal Krawetz先生](http://www.hackerfactor.com/) 莫属，其在 [其07年论文](https://www.wired.com/images_blogs/threatlevel/files/bh-usa-07-krawetz.pdf) 中详细的介绍了这项技术的实现。

### 原理
正常情况下做有损压缩的图像会均匀地应用于一组数据，导致压缩伪像的均匀水平。
错误级别分析显示了整个图像的不同错误级别，强烈建议某种形式的数字操纵。
错误级别分析（ELA）通过以已知错误率（例如95％）故意重新绘制图像，然后计算图像之间的差异来工作。如果几乎没有变化，那么在该质量水平下，单元格已达到其局部最小值误差。然而，如果存在大量的变化，则像素不在其本地最小值处，并且是有效的。
### 示例
1. [http://www.errorlevelanalysis.com](http://www.errorlevelanalysis.com) 是专门做ELA分析的网站，可惜现在已经关闭了。但还是保留了一个示例作为参考(请留意嘴唇、衬衫以及眼睛，这些部分与其周围因素是有所不同的，根据推测是经过修改的，区域变亮)：
![](http://images.43px.com/576ff2a.jpg)
![](http://images.43px.com/576ff2a_enhanced.jpg)
2. [Jonas Wagner](https://29a.ch) 个人的测试(可以看到假的部分图像明显高亮于其周围区域)：
![](http://images.43px.com/fake_screenshot.jpg)
![](http://images.43px.com/original_screenshot.jpg)
### 局限性

有了这个说法，算法并不是完全可靠的，尤其是那些经过重新缩放和经常压缩的图像

-------

更新中。。。

-------

###拓展

 [Neal Krawetz先生](http://www.hackerfactor.com/) 的 [演讲文档](https://www.wired.com/images_blogs/threatlevel/files/bh-usa-07-krawetz.pdf) 
[https://29a.ch/](https://29a.ch/) 也有其他关于图像处理的技术，比如：
自动化图像裁剪主题区域(非暴力裁剪中心区域)的 smartcrop.js [介绍页](https://29a.ch/2014/04/03/smartcrop-content-aware-image-cropping) | [示例页](https://29a.ch/sandbox/2014/smartcrop/examples/testsuite.html) | [测试页]() | [GitHub](https://github.com/jwagner/smartcrop.js/)
图片滤镜 Film Emulator
[测试页](https://29a.ch/film-emulator/) | [GitHub](https://github.com/jwagner/analog-film-emulator)

-------
```
参考资料：
· http://www.hackerfactor.com/
· http://www.wired.com/images_blogs/threatlevel/files/bh-usa-07-krawetz.pdf
· http://www.errorlevelanalysis.com/
· https://29a.ch/
· http://fotoforensic.com/
· https://en.wikipedia.org/wiki/Error_level_analysis
```
-------


