# HuiermAndroidFrame



[图片下载缓存库Picasso](http://square.github.io/picasso/)
===

##示例
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

  


