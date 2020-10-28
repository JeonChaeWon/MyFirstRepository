# 19173054 전채원

## 1주차 과제

## 2주차 과제
<img width="300" height="500" src="./png/19173054전채원_2주차과제.PNG"></img>

## 3주차 과제
<img width="300" height="500" src="./png/19173054전채원_3주차과제.PNG"></img>
<img width="300" height="500" src="./png/19173054전채원_3주차과제-2.PNG"></img>

## 4주차 과제

  - 앱 아이디어 이름 : 추억여행
  - 앱 아이디어 설명 : 대륙, 국가, 도시 등등 각각의 카테고리에 맞춰 여행 후기를 작성하여 해당 여행지를 추천하는 앱이다. 여행 후기 또한 관광지, 맛집, 숙소 등 다양한 카테고리에 맞춰 후기 작성 및 해당 장소 추천을 할 수 있도록 한다. 사진/동영상 업로드 기능을 활성화시켜 사용자들이 시각적인 컨텐츠를 다양하게 접할 수 있게 만든다. 또한 북마크 기능을 강조하여 다시 보고 싶은 포스트를 쉽게 찾을 수 있게 한다. 코로나로 인해 여행을 떠나지 못하는 사용자의 상황을 고려하여 후기 글을 작성함으로써 과거에 다녀왔던 여행을 추억할 수 있으며, 코로나가 종식된 이후에 어떤 장소로 무슨 여행을 떠날 지 계획을 세울 수 있는 정보를 제공할 수 있을 것이다.

## 5주차 과제

## 6주차 과제

## 7주차 과제
<img width="300" height="500" src="./png/19173054전채원_7주차과제.PNG"></img>
<img width="300" height="500" src="./png/19173054전채원_7주차과제-2.PNG"></img>

## 9주차 과제
<h6>[메인화면]</h6>
<img width="300" height="500" src="./png/19173054전채원_9주차과제.PNG"></img>
<h6>[넓이]</h6>
<img width="300" height="500" src="./png/19173054전채원_9주차과제-2.PNG"></img>
<h6>[높이]</h6>
<img width="300" height="500" src="./png/19173054전채원_9주차과제-3.PNG"></img>
<h6>[이미지 바꾸기]</h6>
<img width="300" height="500" src="./png/19173054전채원_9주차과제-4.PNG"></img>

<h3>- Java 소스코드</h3>

    package com.example.a9week_hw_application;

    import androidx.appcompat.app.AppCompatActivity;

    import android.content.res.Resources;
    import android.graphics.drawable.BitmapDrawable;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.ImageView;
    import android.widget.ScrollView;
    import android.widget.Toast;

    public class MainActivity extends AppCompatActivity {

        ScrollView scrollView;
        ImageView imageView;
        BitmapDrawable bitmap;
        String Width;
        String Height;

        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);

            scrollView = findViewById(R.id.verScrollView);
            imageView = findViewById(R.id.imageView);
            scrollView.setHorizontalScrollBarEnabled(true);

            Resources res = getResources();
            bitmap = (BitmapDrawable) res.getDrawable(R.drawable.image01);
            int bitmapWidth = bitmap.getIntrinsicWidth();
            int bitmapHeight = bitmap.getIntrinsicHeight();
            Width = Integer.toString(bitmapWidth);
            Height = Integer.toString(bitmapHeight);

            imageView.setImageDrawable(bitmap);
            imageView.getLayoutParams().width = bitmapWidth;
            imageView.getLayoutParams().height = bitmapHeight;
        }
        public void btnClicked(View v)
        {
            changeImage();
        }
        private void changeImage()
        {
            Resources res = getResources();
            bitmap = (BitmapDrawable) res.getDrawable(R.drawable.image02);
            int bitmapWidth = bitmap.getIntrinsicWidth();
            int bitmapHeight = bitmap.getIntrinsicHeight();

            imageView.setImageDrawable(bitmap);
            imageView.getLayoutParams().width = bitmapWidth;
            imageView.getLayoutParams().height = bitmapHeight;
        }
        public void btnWClicked(View v)
        {
            Toast.makeText(this, Width, Toast.LENGTH_LONG).show();
        }
        public void btnHClicked(View v)
        {
            Toast.makeText(this, Height, Toast.LENGTH_LONG).show();
        }
    }
