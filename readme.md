readme.md
1.最主要的就是img的filter这个属性 ，我把它理解成为投影，觉得更形象
2.这个属性能让我们减少一些http请求(不考虑base64的情况下)，尤其适用于超简单的icon颜色切换，当然也可以考虑svg，这里随便写一下
3.难点和亮点就是，这里我们只显示投影而不显示img原图，毕竟我们只是一张图片的颜色上的简单切换，当时研究了好久，因为若给图片的父元素设置overflow属性的话，原图片看不见，那么他的filter也是不可见的！为此想了好多方法都是失败了，这里不再多说，最后 咱们的 border(你一定知道)闪亮登场，很简单，就是让boder的一个边框宽度为图片宽度，这样边框在父元素中是不会被隐藏的，随后只需要边框透明，然后将投影定位到边框上，搞定# img-filter
