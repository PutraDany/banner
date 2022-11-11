<!--# Terakhir tahun ini Banner Peningkatan baru, selamat tahun baru kepada semua-->
<!--<img src="images/mouse_year.png" width="1080"/>-->

## Banner 2.0 Peningkatan baru
> Hanya buat bekas karusel yang boleh disesuaikan, tidak mengganggu UI ———— Banner 2.0

<a href="https://github.com/youth5201314/banner/tree/release-1.4.10" target="_blank">Banner 1.4.10(Jika anda ingin melihat versi lama, klik di sini)</a>

### Setelah sekian lama tidak hadir, kembali lagi

* Mula-mula saya mengisytiharkan beberapa perkara:
    * Ini hanyalah perpustakaan sumber terbuka. Jika anda berpuas hati, anda boleh menggunakannya, anda boleh belajar daripadanya dan mengubah suainya, saya harap ia akan membantu anda.
    * Jika anda tidak berpuas hati, sila kemukakan, nyatakan butiran yang salah atau ubah suai cadangan, idea yang baik dan perkara yang disesuaikan juga boleh diserahkan secara langsung, dan semua orang boleh datang dan menambah baik bersama-sama.
    * Jika anda rasa ia benar-benar sia-sia, sila jadi orang yang bercucuk tanam diri.
   
### Penambahbaikan besar diperkenalkan
Pada mulanya, saya ingin memuat naik viewpager Versi dikemas kini, tetapi melihat viewpager2 Versi rasmi telah keluar, mari letakkan yang baru padanya.viewpager2 memang daripada viewpager Prestasi yang jauh lebih baik.

- [x] Digunakan ViewPager2 kawalan asas  <a href="https://developer.android.google.cn/jetpack/androidx/releases/viewpager2" target="_blank">ViewPager2 memperkenalkan</a>
- [x] Disokong androidx Pek Keserasian
- [x] Mudah UI、Indicator menyesuaikan
- [x] Kesan galeri sokongan, kesan Meizu
- [x] Serasi dengan putaran mendatar dan menegak, dan juga boleh mencapai kesan yang serupa dengan tajuk utama Taobao
- [x] Ketergantungan pada masa ini hanya perlu diimport ViewPager2



### rendering
Lebih banyak kesan dijalankan demo Semak

![lalai](images/banner_example.gif)

![galeri](images/banner_example2.gif)

![Meizu](images/banner_example1.gif)

![tajuk utama](images/banner_example3.gif)

##### Pelbagai terbina dalam PageTransformer Kesan

![DepthPageTransformer](images/DepthPageTransformer.gif)
![ZoomOutPageTransformer](images/ZoomOutPageTransformer.gif)

|terbina dalam PageTransformer|
|---|
|AlphaPageTransformer|
|DepthPageTransformer|
|RotateDownPageTransformer|
|RotateUpPageTransformer|
|RotateYTransformer|
|ScaleInTransformer|
|ZoomOutPageTransformer|
 Ia juga boleh digunakan dalam kombinasi untuk kesan yang lebih baik

## kaedah
Lebih banyak kaedah tertakluk kepada penggunaan sebenar, tidak semuanya disenaraikan di bawah

|nama kaedah|jenis pemulangan|keterangan|
|---|---|---|
|getAdapter()|extends BannerAdapter|dapatkan tetapan anda BannerAdapter
|getViewPager2()|ViewPager2|Dapatkan ViewPager2
|getIndicator()|Indicator|Dapatkan penunjuk yang anda tetapkan (jika anda tidak menetapkannya secara langsung, ia akan mengeluarkan pengecualian)
|getIndicatorConfig()|IndicatorConfig|Dapatkan maklumat konfigurasi penunjuk yang anda tetapkan (jika anda tidak menetapkannya secara langsung, ia akan mengeluarkan pengecualian.）
|getRealCount()|int|kembali banner jumlah benar
|setUserInputEnabled(boolean)|this|Lumpuhkan leret manual Banner;true membenarkan,false  
|setDatas(List<T>)|this|set semula banner data
|isAutoLoop(boolean)|this|Sama ada untuk membenarkan putaran automatik
|setLoopTime(long)|this|Tetapkan selang putaran (lalai 3000ms)
|setScrollTime(long)|this|Tetapkan masa gelongsor karusel (800ms lalai)
|start()|this|Mulakan putaran (terutamanya digunakan dengan kitaran hayat), atau anda menjeda secara manual dan mula semula
|stop()|this|Hentikan karusel (terutamanya digunakan dengan kitaran hayat), atau anda perlu menjeda secara manual
|setAdapter(T extends BannerAdapter)|this|sediakan banner penyesuai
|setAdapter(T extends BannerAdapter,boolean)|this|sediakan banner Penyesuai, sama ada menyokong gelung tak terhingga
|setOrientation(@Orientation)|this|sediakan banner Arah karusel (menegak or Tahap)
|setOnBannerListener(this)|this|Tetapkan acara klik, subskrip bermula dari 0
|addOnPageChangeListener(this)|this|Tambah ke viewpager2 leret monitor
|setPageTransformer(PageTransformer)|this|设置viewpager的切换效果
|addPageTransformer(PageTransformer)|this|添加viewpager的切换效果（可以设置多个）
|setIndicator(Indicator)|this|设置banner轮播指示器(提供有base和接口，可以自定义)
|setIndicator(Indicator,boolean)|this|设置指示器（传false代表不将指示器添加到banner上，配合布局文件，可以自我发挥）
|setIndicatorSelectedColor(@ColorInt)|this|设置指示器选中颜色
|setIndicatorSelectedColorRes(@ColorRes)|this|设置指示器选中颜色
|setIndicatorNormalColor(@ColorInt)|this|设置指示器默认颜色
|setIndicatorNormalColorRes(@ColorRes)|this|设置指示器默认颜色
|setIndicatorGravity(@IndicatorConfig.Direction)|this|设置指示器位置（左，中，右）
|setIndicatorSpace(int)|this|设置指示器之间的间距
|setIndicatorMargins(IndicatorConfig.Margins)|this|设置指示器的Margins
|setIndicatorWidth(int,int)|this|设置指示器选中和未选中的宽度，直接影响绘制指示器的大小
|setIndicatorNormalWidth(int)|this|设置指示器未选中的宽度
|setIndicatorSelectedWidth(int)|this|设置指示器选中的宽度
|setIndicatorRadius(int)|this|设置指示器圆角，不要圆角可以设置为0
|setIndicatorHeight(int)|this|设置指示器高度
|setBannerRound(float)|this|设置banner圆角（还有一种setBannerRound2方法，需要5.0以上）
|setBannerGalleryEffect(int,int,float)|this|画廊效果
|setBannerGalleryMZ(int,float)|this|魅族效果
|setStartPosition(int)|this|设置开始的位置 (需要在setAdapter或者setDatas之前调用才有效哦)
|setIndicatorPageChange()|this|设置指示器改变监听 (一般是为了配合数据操作使用，看情况自己发挥)
|setCurrentItem()|this|设置当前位置，和原生使用效果一样
|addBannerLifecycleObserver()|this|给banner添加生命周期观察者，内部自动管理banner的生命周期


## Attributes属性
>在banner布局文件中调用,如果你自定义了indicator请做好兼容处理。
下面的属性并不是每个指示器都用得到，所以使用时要注意！

|Attributes|format|describe
|---|---|---|
|banner_loop_time|integer|轮播间隔时间，默认3000
|banner_auto_loop|boolean|是否自动轮播，默认true
|banner_infinite_loop|boolean|是否支持无限循环（即首尾直接过渡），默认true
|banner_orientation|enum|轮播方向：horizontal（默认） or vertical
|banner_radius|dimension|banner圆角半径，默认0（不绘制圆角）
|banner_indicator_normal_width|dimension|指示器默认的宽度，默认5dp （对RoundLinesIndicator无效）
|banner_indicator_selected_width|dimension|指示器选中的宽度，默认7dp 
|banner_indicator_normal_color|color|指示器默认颜色，默认0x88ffffff
|banner_indicator_selected_color|color|指示器选中颜色，默认0x88000000
|banner_indicator_space|dimension|指示器之间的间距，默认5dp （对RoundLinesIndicator无效）
|banner_indicator_gravity|dimension|指示器位置，默认center
|banner_indicator_margin|dimension|指示器的margin,默认5dp，不能和下面的同时使用
|banner_indicator_marginLeft|dimension|指示器左边的margin
|banner_indicator_marginTop|dimension|指示器上边的margin
|banner_indicator_marginRight|dimension|指示器右边的margin
|banner_indicator_marginBottom|dimension|指示器下边的margin
|banner_indicator_height|dimension|指示器高度（对CircleIndicator无效）
|banner_indicator_radius|dimension|指示器圆角（对CircleIndicator无效）
|banner_round_top_left|boolean|设置要绘制的banner圆角方向（如果都不设置默认全部）
|banner_round_top_right|boolean|设置要绘制的banner圆角方向（如果都不设置默认全部）
|banner_round_bottom_left|boolean|设置要绘制的banner圆角方向（如果都不设置默认全部）
|banner_round_bottom_right|boolean|设置要绘制的banner圆角方向（如果都不设置默认全部）



## 使用步骤
>以下提供的是最简单的步骤，需要复杂的样式自己可以自定义

#### Step 1.依赖banner
Gradle 
```groovy

repositories {
    maven { url "https://s01.oss.sonatype.org/content/groups/public" }
}

dependencies{
    //2.1.0以前jcenter的依赖
    //implementation 'com.youth.banner:banner:2.1.0'
    //现在Maven Central
    implementation 'io.github.youth5201314:banner:2.2.2'

}
```

#### Step 2.添加权限到你的 AndroidManifest.xml
```xml
<!-- if you want to load images from the internet -->
<uses-permission android:name="android.permission.INTERNET" /> 

```

#### Step 3.在布局文件中添加Banner，可以设置自定义属性
！！！此步骤可以省略，可以直接在Activity或者Fragment中new Banner();
```xml
<com.youth.banner.Banner
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/banner"
    android:layout_width="match_parent"
    android:layout_height="高度自己设置" />
```

#### Step 4.继承BannerAdapter，和RecyclerView的Adapter一样（如果你只是图片轮播也可以使用默认的）
！！！此步骤可以省略，图片轮播提供有默认适配器，其他的没有提供是因为大家的可变性要求不确定，所以直接自定义的比较好。
```java

/**
 * 自定义布局，下面是常见的图片样式，更多实现可以看demo，可以自己随意发挥
 */
public class ImageAdapter extends BannerAdapter<DataBean, ImageAdapter.BannerViewHolder> {

    public ImageAdapter(List<DataBean> mDatas) {
        //设置数据，也可以调用banner提供的方法,或者自己在adapter中实现
        super(mDatas);
    }

    //创建ViewHolder，可以用viewType这个字段来区分不同的ViewHolder
    @Override
    public BannerViewHolder onCreateHolder(ViewGroup parent, int viewType) {
        ImageView imageView = new ImageView(parent.getContext());
        //注意，必须设置为match_parent，这个是viewpager2强制要求的
        imageView.setLayoutParams(new ViewGroup.LayoutParams(
                ViewGroup.LayoutParams.MATCH_PARENT,
                ViewGroup.LayoutParams.MATCH_PARENT));
        imageView.setScaleType(ImageView.ScaleType.CENTER_CROP);
        return new BannerViewHolder(imageView);
    }

    @Override
    public void onBindView(BannerViewHolder holder, DataBean data, int position, int size) {
        holder.imageView.setImageResource(data.imageRes);
    }

    class BannerViewHolder extends RecyclerView.ViewHolder {
        ImageView imageView;

        public BannerViewHolder(@NonNull ImageView view) {
            super(view);
            this.imageView = view;
        }
    }
}

```

#### Step 5.Banner具体方法调用 

```java
public class BannerActivity extends AppCompatActivity {
    public void useBanner() {
        //--------------------------简单使用-------------------------------
        banner.addBannerLifecycleObserver(this)//添加生命周期观察者
                .setAdapter(new BannerExampleAdapter(DataBean.getTestData()))
                .setIndicator(new CircleIndicator(this));
        
        //—————————————————————————如果你想偷懒，而又只是图片轮播————————————————————————
         banner.setAdapter(new BannerImageAdapter<DataBean>(DataBean.getTestData3()) {
                    @Override
                    public void onBindView(BannerImageHolder holder, DataBean data, int position, int size) {
                        //图片加载自己实现
                        Glide.with(holder.itemView)
                             .load(data.imageUrl)
                             .apply(RequestOptions.bitmapTransform(new RoundedCorners(30)))
                             .into(holder.imageView);
                    }
                })
                .addBannerLifecycleObserver(this)//添加生命周期观察者
                .setIndicator(new CircleIndicator(this));
        //更多使用方法仔细阅读文档，或者查看demo
    }
}
```

## Banner使用中优化体验
**如果你需要考虑更好的体验，可以看看下面的代码**
#### Step 1.（可选）生命周期改变时
```java
public class BannerActivity {
  
    //方法一：自己控制banner的生命周期
    
    @Override
    protected void onStart() {
        super.onStart();
        //开始轮播
        banner.start();
    }
    
    @Override
    protected void onStop() {
        super.onStop();
        //停止轮播
        banner.stop();
    }
    
    @Override
    protected void onDestroy() {
        super.onDestroy();
        //销毁
        banner.destroy();
    }
    
    //方法二：调用banner的addBannerLifecycleObserver()方法，让banner自己控制
   
    protected void onCreate(Bundle savedInstanceState) {
         //添加生命周期观察者
        banner.addBannerLifecycleObserver(this);
    }
}
```


## 常见问题（收录被反复询问的问题）

* 网络图片加载不出来？

  `banner本身不提供图片加载功能，首先确认banner本身使用是否正确，具体参考demo，
  然后请检查你的图片加载框架或者网络请求框架，服务端也可能加了https安全认证，是看下是否报有证书相关错误`
  
* 怎么实现视频轮播？

  `demo中有实现类似淘宝商品详情的效果，第一个放视频，后面的放的是图片，并且可以设置首尾不能滑动。
  因为大家使用的播放器不一样业务环境也不同，具体情况自己把握，demo就是给一个思路哈！可以参考和修改`

* 我想指定轮播开始的位置？

  `现在提供了setStartPosition()方法，在sheAdapter和setDatas直接调用一次就行了，当然setAdapter后通过setCurrentItem设置也行`

* 父控件滑动时，banner切换会获取焦点，然后自动全部显示。不想让banner获取焦点可以给父控件加上：

    ```
        //banner也一定要用最新版哦！
        android:focusable="true"
        android:focusableInTouchMode="true"
    ```
* 怎么设置圆角？
  1、调用提供的方法或者自定义属性进行设置，这里设置的是banner本身的圆角，不是轮播内view的圆角
  2、在adapter中对自定义的view进行自己实现，就拿图片举例：可以自己定义一个圆角的ImageView控件，或者使用glide渲染都行。请举一反三，view都自定义了还有什么不能改的？
  
    
## Thanks

- [MZBannerView](https://github.com/pinguo-zhouwei/MZBannerView)
- [MagicViewPager](https://github.com/hongyangAndroid/MagicViewPager)
- [zguop的viewpager2的滑动时间解决方案](https://github.com/zguop/banner/blob/master/pager2banner/src/main/java/com/to/aboomy/pager2banner/Banner.java)


### 联系方式  <a target="_blank" href="http://mail.qq.com/cgi-bin/qm_share?t=qm_mailme&email=KBkYGhAfGhEYEB5oWVkGS0dF" style="text-decoration:none;"><img src="images/mailme.png"/></a>
* 我的个人微博：https://weibo.com/u/3013494003 有兴趣的也可以关注，大家一起交流
* 有问题可以加群大家一起交流，如果你觉得对你有帮助可以扫描下面支付宝二维码随意打赏下哦！

<img src="images/qq.png" width="220"/> <img src="images/pay.jpg" width="220"/>


## 更新说明
[更新说明](update_message.md)

