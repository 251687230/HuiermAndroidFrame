# HuiermAndroidFrame

目录
===
* <h2>框架</h2>
    * <h3><a href="#KJFrame">KJFrame</a></h3>

* <h2>网络</h2>
 * <h3><a href="#Volley">Volley</a></h3>
 * <h3>OkHttp</h3>

* <h2>图片下载缓存</h2>
 * <h3>Picasso</h3>
 * <h3>Fresco</h3>
 * <h3>Glide</h3>
 
* <h2>组件</h2>
 * <h3>下拉刷新ListView SwipeRefreshLayout</h3>
 * <h3>自定义形状ImageView CustomShapeImageView</h3>
 * <h3>图片轮播 ImageCycleview</h3>
 * <h3>左划菜单Navigation View</h3>
 * <h3>MaterialLoadingProgressBar</h3>
 * <h3>MaterialSearchView</h3>
 * <h3>MaterialSpinner</h3>

* <h2>存储</h2>
 * <h3>加密数据库 sqlcipher</h3>

* <h2>其他</h2>
 * <h3>注解框架ButterKnife</h3>
 * <h3>非空格式验证框架 Android Validation</h3>
 * <h3>二维码生成及扫描 QrCodeScan</h3>
 * <h3>事件分发库 EventBus</h3>
 
 

<h1 id="KJFrame">KJFrame</h1>
###APi文档地址 http://kjframe.github.io/
###github地址  https://github.com/kymjs/KJFrameForAndroid

* **1.Activity(Fragment)Frame**
   
<h1 id="Volley">Volley</h1>



[图片下载缓存库Picasso](http://square.github.io/picasso/)
===

* **1.基本用法**
```java
Picasso.with(context)    
  .load(url)                              //请求Uri,resourceId,File对象,或者文件路径
  .resize(50, 50)                         //指定图片缩放尺寸
  .placeholder(R.drawable.moren_banner)   //默认图
  .error(R.drawable.moren_banner)         //请求错误图
  .centerCrop()                           //填充方式，centerCrop or centerInsider
  .into(imageView);
  ```
* **2.Adapter中的使用**
```java
@Override public void getView(int position, View convertView, ViewGroup parent) {
    SquaredImageView view = (SquaredImageView) convertView;
    if (view == null) {
    view = new SquaredImageView(context);
   }
   String url = getItem(position);
   Picasso.with(context).load(url).into(view);
}
```

下拉刷新库SwipeRefreshLayout
===

  


