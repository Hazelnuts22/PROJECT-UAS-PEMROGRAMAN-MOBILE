# PROJECT-UAS-PEMROGRAMAN-MOBILE

Nama : Cahyo Hidayatullah

Kelas : TI.22.A1

Nim : 312210079

Matkul  : Pemrograman Mobile

Dosen   : Donny Maulana, S.Kom., M.M.S.I.

## TUGAS
<p align="justify"> Di tugas kali ini saya akan menyatukan semua project dari pertemuan satu sampai pertemuan akhir yang di gabungkan dalam satu aplikasi. Berikut adalah code dan hasil run yang saya buat.</p>

## Source Code
Di bawah ini adalah source code project saya

**colors.xml**
      
      <?xml version="1.0" encoding="utf-8"?>
      <resources>
          <color name="black">#FF000000</color>
          <color name="white">#FFFFFFFF</color>
          <color name="blue">#3700B3</color>
          <color name="pink">#FFC0CB</color>
          <color name="colorPrimary">#3F5185</color>
          <color name="colorPrimaryDark">#303F9F</color>
          <color name="colorAccent">#FF4081</color>
          <color name="birumuda">#ABCBFA</color>
          <color name="salem">#F8C6E6</color>
          <color name ="purple">#E3A2ED</color>
          <color name="hijau">#92A676</color>
          <color name="biru">#8FC2EA</color>
          <color name="hijaumuda">#C2E69C</color>
          <color name="kuning">#FFEB3B</color>
          <color name="orange">#FF9800</color>
          <color name="cream">#E6C18A</color>
          <color name="hijautua">#3F4A2F</color>
          <color name="hijausoft">#9FC17C</color>
          <color name="coklat">#574545</color>
          <color name="choco">#A69E9E</color>
      </resources>

 **dimens.xml**

            <?xml version="1.0" encoding="utf-8"?>
      <resources>
          <dimen name="padding_regular">10dp</dimen>
          <dimen name="line_spacing">5sp</dimen>
      </resources>

 **strings.xml**

                      <resources>
                      <string name="app_name">CahyoAplication</string>
                      <string name="Hello_World">Hello World!!</string>
                  
                      <string name="button_main">Send</string>
                      <string name="editText_main">Enter Your Message Here</string>
                      <string name="text_header">Message Received</string>
                      <string name="buttton_second">Reply</string>
                      <string name="editText_second">Enter Your Reply Here</string>
                      <string name="text_header_reply">Reply Received</string>
                  
                      <string name="button_label_toast">Toast</string>
                      <string name="button_label_count">Count</string>
                      <string name="count_initial_value">1</string>
                      <string name="toast_massage">Hello Toast!</string>
                      <string name="button_label_restart">Restart</string>
                      <string name="enter_fibonacci_limit">Masukkan Angka Limit</string>
                  
                      <string name="article_title"> Kasus Sianida</string>
                      <string name="article_subtitle">ICE COLD!</string>
                  
                      <string name="article_text"> Film dokumenter Ice Cold: Murder, Coffee and Jessica Wongso memaparkan pertanyaan tak terjawab tentang persidangan yang dilalui Jessica Wongso. Dengan menyajikan perspektif baru, film ini hadir bertahun-tahun setelah kematian sahabat Jessica, Wayan Mirna Salihin.
                  
                  
                  Film ini menggambarkan bagaimana Jessica yang mengajak teman-temannya, termasuk Mirna, untuk bertemu setelah sekian lama tak berjumpa. Pertemuan di salah satu kafe di mal ibu kota tersebut pun berlangsung lancar, sebelum akhirnya Mirna pingsan sesaat setelah meminum kopi yang sebelumnya dipesan Jessica.Dokumenter ini turut menyajikan rekaman CCTV pada waktu kejadian, berbagai footage berita saat persidangan berlangsung, hingga wawancara eksklusif dengan beberapa sumber, termasuk Jessica Wongso.
                  
                  
                  Persidangan atas dugaan pembunuhan Mirna Salihin digelar lima bulan setelah kematiannya. Sidang tersebut melalui 32 kali persidangan dengan menghadirkan puluhan saksi di pengadilan. Hasilnya, Jessica Wongso divonis bersalah atas kematian Mirna dan dijatuhi hukuman 20 tahun penjara.
                  Kasus yang berjalan cukup lama tersebut menyita banyak perhatian dari masyarakat Indonesia. Musababnya, banyak misteri tak terjawab selama rangkaian persidangan yang panjang tersebut. Salah satunya adalah mengenai akses untuk mendapatkan bubuk sianida yang tidak bisa didapatkan oleh orang sembarangan. Selain itu, motif Jessica di balik pembunuhan tersebut pun belum menemukan jawabannya.
                  
                  
                  Film dokumenter buatan Netflix ini menyoroti rangkaian persidangan yang saat itu menjadi sidang pertama yang disiarkan secara langsung di berbagai stasiun televisi Indonesia. Selain itu, kasus ini juga diliput secara intens oleh media massa, baik nasional maupun internasional.Tak hanya itu, pihak rumah produksi Beach House Pictures juga berhasil mendapatkan akses untuk mewawancarai Jessica Wongso secara langsung dari balik tahanan. Dalam video trailer yang diluncurkannya, ditampilkan juga sejumlah wawancara eksklusif yang dilakukan dengan beberapa narasumber. Mulai dari ayah dan saudara kembar  Mirna Salihin, pengacara Jessica Wongso, jurnalis yang mendalami kasus tersebut, hingga bagaimana saat itu kasus ini begitu ramai diberitakan oleh media massa Indonesia dan internasional.</string>
                          <!-- TODO: Remove or change this placeholder text -->
                          <string name="hello_blank_fragment">Hello blank fragment</string>
                  
                  
                  </resources>

**Source Code SplashScreen**

  -***SplashScreen.java***

          package com.example.intentapp;
          
          import android.content.Intent;
          import android.os.Bundle;
          import android.os.Handler;
          
          import androidx.appcompat.app.AppCompatActivity;
          
          public class SplashScreen extends AppCompatActivity {
              @Override
              protected void onCreate(Bundle savedInstanceState) {
                  super.onCreate(savedInstanceState);
          
                  new Handler().postDelayed(new Runnable() {
                      @Override
                      public void run() {
                          startActivity(new Intent(SplashScreen.this, MainActivity.class));
                          finish();
                      }
                  }, 2500);
              }
          }

  ***logo SplashScreen***

          <?xml version="1.0" encoding="utf-8"?>
          <layer-list xmlns:android="http://schemas.android.com/apk/res/android">
              <item android:drawable="@color/birumuda"/>
              <item>
                  <bitmap
                      android:src="@drawable/logo"
                      android:gravity="center" />
              </item>
          </layer-list>


**Themes**

***themes.xml***

      <resources xmlns:tools="http://schemas.android.com/tools">
          <!-- Base application theme. -->
          <style name="SplashScreen" parent="Theme.MaterialComponents.DayNight.NoActionBar">
              <item name="android:windowBackground">@drawable/splashscreenapp</item>
              <item name="android:statusBarColor">?attr/colorOnPrimary</item>
          </style>
      
          <!-- Base application theme. -->
          <style name="Base.Theme.TabExperiment" parent="Theme.MaterialComponents.DayNight.NoActionBar">
              <!-- Primary brand color. -->
              <item name="colorPrimary">@color/colorPrimary</item>
              <item name="colorPrimaryVariant">@color/cream</item>
              <item name="colorOnPrimary">@color/white</item>
              <!-- Secondary brand color. -->
              <item name="colorSecondary">@color/hijau</item>
              <item name="colorSecondaryVariant">@color/hijaumuda</item>
              <item name="colorOnSecondary">@color/black</item>
              <!-- Status bar color. -->
              <item name="android:statusBarColor">@color/choco</item>
              <item name="android:navigationBarColor">@color/choco</item>
              <!-- Customize your light theme here. -->
          </style>
      
          <style name="Theme.TabExperiment" parent="Base.Theme.TabExperiment" />
      </resources>

***themes.xml(night)***

      <resources xmlns:tools="http://schemas.android.com/tools">
          <!-- Base application theme. -->
          <style name="SplashScreen" parent="Theme.MaterialComponents.DayNight.NoActionBar">
              <item name="android:windowBackground">@drawable/splashscreenapp</item>
              <item name="android:statusBarColor">?attr/colorOnPrimary</item>
          </style>
      
          <!-- Base application theme. -->
          <style name="Base.Theme.TabExperiment" parent="Theme.MaterialComponents.DayNight.NoActionBar">
              <!-- Primary brand color. -->
              <item name="colorPrimary">@color/colorPrimary</item>
              <item name="colorPrimaryVariant">@color/cream</item>
              <item name="colorOnPrimary">@color/white</item>
              <!-- Secondary brand color. -->
              <item name="colorSecondary">@color/hijau</item>
              <item name="colorSecondaryVariant">@color/hijaumuda</item>
              <item name="colorOnSecondary">@color/black</item>
              <!-- Status bar color. -->
              <item name="android:statusBarColor">@color/choco</item>
              <item name="android:navigationBarColor">@color/choco</item>
              <!-- Customize your light theme here. -->
          </style>
      
          <style name="Theme.TabExperiment" parent="Base.Theme.TabExperiment" />
      </resources>

**Source Code Java**

  ***MainActivity.java***

      package com.example.intentapp;
      
      import android.annotation.SuppressLint;
      import android.content.Intent;
      import android.net.Uri;
      import android.os.Bundle;
      import android.view.View;
      import androidx.appcompat.app.AppCompatActivity;
      
      
      public class MainActivity extends AppCompatActivity {
      
          @SuppressLint("MissingInflatedId")
          @Override
          protected void onCreate(Bundle savedInstanceState) {
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_main);
      
              findViewById(R.id.cdMenu5).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
      
                      setAlarm();
                  }
              });
      
              findViewById(R.id.cdMenu1).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      // Ketika tombolSatu ditekan, pindah ke HelloActivity
                      Intent helloworld = new Intent(MainActivity.this, HelloActivity.class);
                      startActivity(helloworld);
                  }
              });
      
              findViewById(R.id.cdMenu2).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      // Ketika tombolDua ditekan, lakukan aksi yang diinginkan
                      // Misalnya, pindah ke aktivitas lain atau jalankan fungsi khusus
                      Intent toast = new Intent(MainActivity.this, CountActivity.class);
                      startActivity(toast);
                  }
              });
      
              findViewById(R.id.cdMenu3).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      // Ketika tombolDua ditekan, lakukan aksi yang diinginkan
                      // Misalnya, pindah ke aktivitas lain atau jalankan fungsi khusus
                      Intent sianida = new Intent(MainActivity.this, SianidaActivity.class);
                      startActivity(sianida);
                  }
              });
      
              findViewById(R.id.cdMenu4).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      // Ketika tombolDua ditekan, lakukan aksi yang diinginkan
                      // Misalnya, pindah ke aktivitas lain atau jalankan fungsi khusus
                      Intent twoactivity = new Intent(MainActivity.this, TwoactActivity.class);
                      startActivity(twoactivity);
                  }
              });
      
              findViewById(R.id.cdMenu7).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      // Ketika tombolDua ditekan, lakukan aksi yang diinginkan
                      // Misalnya, pindah ke aktivitas lain atau jalankan fungsi khusus
                      Intent fragmentactivity = new Intent(MainActivity.this, FragmentActivity.class);
                      startActivity(fragmentactivity);
                  }
              });
      
              findViewById(R.id.cdMenu6).setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      // Example location: Jakarta, Indonesia
                      Uri geoLocation = Uri.parse("geo:-6.2088,106.8456");
                      openMaps(geoLocation);
                  }
              });
          }
      
          private void setAlarm() {
              Intent alarmIntent = new Intent(android.provider.AlarmClock.ACTION_SET_ALARM);
              // Add extra details for the alarm, e.g., alarm time, label, etc.
              // alarmIntent.putExtra(...
              startActivity(alarmIntent);
          }
          private void openMaps(Uri geoLocation) {
              Intent maps = new Intent(Intent.ACTION_VIEW);
              maps.setData(geoLocation);
              if (maps.resolveActivity(getPackageManager()) != null) {
                  startActivity(maps);
              }
          }
      
      }
  
  ***ViewAdapter.java***

      package com.example.intentapp;
      
      import androidx.annotation.NonNull;
      import androidx.fragment.app.Fragment;
      import androidx.fragment.app.FragmentActivity;
      import androidx.viewpager2.adapter.FragmentStateAdapter;
      
      public class ViewAdapter extends FragmentStateAdapter {
          public ViewAdapter(@NonNull FragmentActivity fragmentActivity) {
              super(fragmentActivity);
          }
      
          @NonNull
          @Override
          public Fragment createFragment(int position) {
              switch (position){
                  case 0:
                      return new ActionFragment();
                  case 1:
                      return new ComedyFragment();
                  case 2:
                      return new RomanceFragment();
                  default:
                      return new ActionFragment();
              }
          }
      
          @Override
          public int getItemCount() {
              return 3;
          }
      }
    
  ***VideoPlayerActivity.java***

      package com.example.intentapp;
      
      
      import android.content.pm.ActivityInfo;
      import android.net.Uri;
      import android.os.Bundle;
      import android.view.Menu;
      import android.view.MenuItem;
      import android.view.View;
      import android.view.ViewGroup;
      import android.widget.MediaController;
      import android.widget.RelativeLayout;
      import android.widget.VideoView;
      
      import androidx.annotation.NonNull;
      import androidx.annotation.Nullable;
      import androidx.appcompat.app.AppCompatActivity;
      
      
      public class VideoPlayerActivity extends AppCompatActivity {
      
          private VideoView videoView; // Deklarasi VideoView sebagai variabel global
          private int originalOrientation;
      
          @Override
          protected void onCreate(@Nullable Bundle savedInstanceState) {
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_video_player);
      
              // Get the video URI from the intent
              String videoPath = getIntent().getStringExtra("VIDEO_PATH");
              Uri uri = Uri.parse(videoPath);
      
              // Set up VideoView
              videoView = findViewById(R.id.videoView); // Inisialisasi variabel videoView
              videoView.setVideoURI(uri);
      
              // Set up MediaController
              MediaController mediaController = new MediaController(this);
              mediaController.setAnchorView(videoView);
              videoView.setMediaController(mediaController);
      
              // Start playing the video
              videoView.start();
      
              // Get the original orientation
              originalOrientation = getResources().getConfiguration().orientation;
      
              // Adjust video layout based on the original orientation
              adjustVideoLayout(originalOrientation);
          }
      
          @Override
          protected void onResume() {
              super.onResume();
              // Detect orientation changes and adjust VideoView layout
              int currentOrientation = getResources().getConfiguration().orientation;
              if (currentOrientation != originalOrientation) {
                  adjustVideoLayout(currentOrientation);
                  originalOrientation = currentOrientation;
              }
          }
      
          private void adjustVideoLayout(int orientation) {
              if (orientation == ActivityInfo.SCREEN_ORIENTATION_LANDSCAPE ||
                      orientation == ActivityInfo.SCREEN_ORIENTATION_REVERSE_LANDSCAPE) {
                  // Landscape mode
                  setFullscreen(true);
              } else {
                  // Portrait or other orientations
                  setFullscreen(false);
              }
          }
      
          private void setFullscreen(boolean fullscreen) {
              if (fullscreen) {
                  // Hide action bar
                  if (getSupportActionBar() != null) {
                      getSupportActionBar().hide();
                  }
      
                  // Set VideoView layout parameters for fullscreen
                  RelativeLayout.LayoutParams params = new RelativeLayout.LayoutParams(
                          ViewGroup.LayoutParams.MATCH_PARENT,
                          ViewGroup.LayoutParams.MATCH_PARENT
                  );
                  params.addRule(RelativeLayout.CENTER_IN_PARENT);
                  videoView.setLayoutParams(params);
      
                  // Hide navigation bar and status bar
                  getWindow().getDecorView().setSystemUiVisibility(
                          View.SYSTEM_UI_FLAG_FULLSCREEN |
                                  View.SYSTEM_UI_FLAG_HIDE_NAVIGATION |
                                  View.SYSTEM_UI_FLAG_IMMERSIVE_STICKY);
              } else {
                  // Show action bar
                  if (getSupportActionBar() != null) {
                      getSupportActionBar().show();
                  }
      
                  // Set VideoView layout parameters for normal mode
                  RelativeLayout.LayoutParams params = new RelativeLayout.LayoutParams(
                          ViewGroup.LayoutParams.MATCH_PARENT,
                          ViewGroup.LayoutParams.WRAP_CONTENT
                  );
                  params.addRule(RelativeLayout.CENTER_IN_PARENT);
                  videoView.setLayoutParams(params);
      
                  // Show navigation bar and status bar
                  getWindow().getDecorView().setSystemUiVisibility(
                          View.SYSTEM_UI_FLAG_VISIBLE);
              }
          }
      
          @Override
          public boolean onCreateOptionsMenu(Menu menu) {
              getMenuInflater().inflate(R.menu.menu_video_player, menu);
              return true;
          }
      
          @Override
          public boolean onOptionsItemSelected(@NonNull MenuItem item) {
              if (item.getItemId() == R.id.action_back) {
                  // Tambahkan logika untuk kembali ke halaman sebelumnya atau finish activity
                  finish();
                  return true;
              }
              return super.onOptionsItemSelected(item);
          }
      }
  
  ***TwoactActivity.java***

      package com.example.intentapp;


      import androidx.appcompat.app.AppCompatActivity;
      
      import android.content.Intent;
      import android.os.Bundle;
      import android.util.Log;
      import android.view.View;
      import android.widget.EditText;
      import android.widget.TextView;
      
      public class TwoactActivity extends AppCompatActivity {
      
          private static final String LOG_TAG = TwoactActivity.class.getSimpleName();
      
          public static final String EXTRA_MESSAGE = "com.example.android.Two2Activity.extra.MESSAGE";
      
          public static final int TEXT_REQUEST = 1;
      
          private EditText mMessageEditText;
      
          private TextView mReplyHeadTextView;
      
          private TextView mReplyTextView;
      
          @Override
          protected void onCreate(Bundle savedInstanceState) {
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_twoact);
      
              mMessageEditText = findViewById(R.id.editText_main);
              mReplyHeadTextView = findViewById(R.id.text_header_reply);
              mReplyTextView = findViewById(R.id.text_message_reply);
          }
      
          public void LaunchSecondActivity(View view) {
              Log.d(LOG_TAG, "Button clicked!");
              Intent intent = new Intent(this, Twoact2Activity.class);
              String message = mMessageEditText.getText().toString();
              intent.putExtra(EXTRA_MESSAGE, message);
              startActivityForResult(intent, TEXT_REQUEST);
          }
      
          @Override
          public void onActivityResult(int requestCode, int resultCode, Intent data) {
              super.onActivityResult(requestCode, resultCode, data);
      
              if (requestCode == TEXT_REQUEST) {
                  if (resultCode == RESULT_OK) {
                      String reply = data.getStringExtra(Twoact2Activity.EXTRA_REPLY);
      
                      mReplyHeadTextView.setVisibility(View.VISIBLE);
                      mReplyTextView.setText(reply);
                      mReplyTextView.setVisibility(View.VISIBLE);
                  }
              }
          }
      }
  
  ***Twoact2Activity.java***

      package com.example.intentapp;
      
      import android.content.Intent;
      import android.os.Bundle;
      import android.view.View;
      import android.widget.EditText;
      import android.widget.TextView;
      
      import androidx.appcompat.app.AppCompatActivity;
      
      public class Twoact2Activity extends AppCompatActivity {
      
          public static final String EXTRA_REPLY ="com.example.android.Two2Activity.extra.REPLY";
          public static final String EXTRA_MESSAGE ="com.example.android.Two2Activity.extra.MESSAGE";
          private EditText mReply;
      
          @Override
          protected void onCreate(Bundle savedInstanceState){
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_twoact2);
      
              mReply = findViewById(R.id.editText_second);
      
              Intent intent = getIntent();
              String message = intent.getStringExtra(Twoact2Activity.EXTRA_MESSAGE);
      
              TextView textView = findViewById(R.id.text_message);
              textView.setText(message);
          }
          public void returnReply(View view){
              String reply = mReply.getText().toString();
              Intent replyIntent = new Intent();
              setResult(RESULT_OK, replyIntent);
              finish();
          }
      }
  
  ***SianidaActivity.java***

      package com.example.intentapp;
      
      import android.os.Bundle;
      
      import androidx.appcompat.app.AppCompatActivity;
      
      public class SianidaActivity extends AppCompatActivity {
          @Override
          protected void onCreate(Bundle savedInstanceState){
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_sianida);
          }
      }

***HelloActivity.java***

      package com.example.intentapp;
      
      
      import androidx.appcompat.app.AppCompatActivity;
      
      import android.os.Bundle;
      
      public class HelloActivity extends AppCompatActivity{
          @Override
          protected void onCreate(Bundle savedInstanceState) {
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_hello);
          }
      }

***CountActivity.java***

      package com.example.intentapp;
      
      import android.annotation.SuppressLint;
      import android.app.AlertDialog;
      import android.content.DialogInterface;
      import android.graphics.Color;
      import android.os.Bundle;
      import android.view.View;
      import android.widget.EditText;
      import android.widget.TextView;
      import androidx.appcompat.app.AppCompatActivity;
      
      
      public class CountActivity extends AppCompatActivity {
          private TextView show_count;
          private int count = 1;
          private long fibNMinus1 = 1;
          private long fibNMinus2 = 1;
          private int limit = -1; // Inisialisasi limit dengan nilai default
      
      
          @SuppressLint("MissingInflatedId")
          @Override
          protected void onCreate(Bundle savedInstanceState) {
              super.onCreate(savedInstanceState);
              setContentView(R.layout.activity_count);
      
              show_count = findViewById(R.id.show_count);
          }
      
          public void countUp(View view) {
              if (count == 0) {
                  show_count.setText("0");
              }
              else if (count == 1) {
                  show_count.setText("1");
              }
              else {
                  if (limit != -1 && count > limit) {
                      // Jika count melebihi limit, atur ulang perhitungan
                      count = 0;
                      fibNMinus1 = 1;
                      fibNMinus2 = 0;
                      show_count.setText(getString(R.string.count_initial_value));
                  }
                  else {
                      long fibCurrent = fibNMinus1 + fibNMinus2;
                      fibNMinus2 = fibNMinus1;
                      fibNMinus1 = fibCurrent;
      
                      //Mengatur warna teks berdasarkan angka Fibonacci
                      int colorResId = R.color.colorAccent; // Warna Default
                      switch (count % 11) {
                          case 1:
                              colorResId = R.color.colorAccent; // Warna Pink Tua
                              break;
                          case 2:
                              colorResId = R.color.hijaumuda; // Warna Hijau Muda
                              break;
                          case 3:
                              colorResId = R.color.purple; // Warna Ungu
                              break;
                          case 4:
                              colorResId = R.color.salem; // Warna Salem
                              break;
                          case 5:
                              colorResId = R.color.birumuda; // Warna Biru Muda
                              break;
                          case 6 :
                              colorResId = R.color.kuning; // Warna Kuning
                              break;
                          case 7:
                              colorResId = R.color.hijau; // Warna Hijau
                              break;
                          case 8:
                              colorResId = R.color.cream; // Warna Cream
                              break;
                          case 9:
                              colorResId = R.color.pink; // Warna Pink
                              break;
                          case 10:
                              colorResId = R.color.biru; // Warna Biru
                              break;
                          case 11:
                              colorResId = R.color.orange; // Warna Orange
                              break;
                      }
                      show_count.setTextColor(getResources().getColor(colorResId));
                      show_count.setText(String.valueOf(fibCurrent));
                  }
              }
      
              count++;
          }
      
          public void back1(View view) {
              count = 1;
              fibNMinus1 = 1;
              fibNMinus2 = 0;
              show_count.setText(getString(R.string.count_initial_value));
          }
      
          public void setLimit(View view) {
              // Create and display a dialog to set the limit
              AlertDialog.Builder builder = new AlertDialog.Builder(this);
              builder.setTitle("Set Limit");
      
              final EditText input = new EditText(this);
              input.setInputType(android.text.InputType.TYPE_CLASS_NUMBER);
              builder.setView(input);
      
              builder.setPositiveButton("OK", new DialogInterface.OnClickListener() {
                  @Override
                  public void onClick(DialogInterface dialog, int which) {
                      // Get the limit from the input and set it for calculations
                      String limitStr = input.getText().toString();
                      limit = Integer.parseInt(limitStr);
                  }
              });
      
              builder.setNegativeButton("Cancel", new DialogInterface.OnClickListener() {
                  @Override
                  public void onClick(DialogInterface dialog, int which) {
                      dialog.cancel();
                  }
              });
      
              builder.show();
          }
      }

***FragmentActivity.java***

    package com.example.intentapp;
    
    
    import androidx.annotation.NonNull;
    import androidx.appcompat.app.AppCompatActivity;
    import androidx.fragment.app.Fragment;
    import androidx.fragment.app.FragmentManager;
    import androidx.fragment.app.FragmentStatePagerAdapter;
    import androidx.viewpager2.widget.ViewPager2;
    
    import android.annotation.SuppressLint;
    import android.content.Context;
    import android.graphics.drawable.ColorDrawable;
    import android.os.Bundle;
    
    import com.google.android.material.tabs.TabLayout;
    
    import java.util.Objects;
    
    public class FragmentActivity extends AppCompatActivity {
    
        TabLayout tabLayout;
        ViewPager2 viewPager2;
        ViewAdapter adapter;
    
        @SuppressLint({"NewApi", "MissingInflatedId"})
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_movie);
    
            Objects.requireNonNull(getSupportActionBar()).setBackgroundDrawable(new ColorDrawable(getColor(R.color.cream)));
    
            tabLayout = findViewById(R.id.tab);
            viewPager2 = findViewById(R.id.view);
            adapter = new ViewAdapter(this);
            viewPager2.setAdapter(adapter);
    
            tabLayout.addOnTabSelectedListener(new TabLayout.OnTabSelectedListener() {
                @Override
                public void onTabSelected(TabLayout.Tab tab) {
                    viewPager2.setCurrentItem(tab.getPosition());
                }
    
                @Override
                public void onTabUnselected(TabLayout.Tab tab) {
    
                }
    
                @Override
                public void onTabReselected(TabLayout.Tab tab) {
    
                }
            });
    
            class Halaman extends FragmentStatePagerAdapter {
                Context context;
                int jumlah_tab;
    
                Halaman(Context context, FragmentManager fm, int jml_tab)
                {
                    super(fm);
                    this.context=context;
                    this.jumlah_tab=jml_tab;
                }
    
                @NonNull
                @Override
                public Fragment getItem(int posisition){
                    switch (posisition){
                        case 0:return new ActionFragment();
                        case 1:return new ComedyFragment();
                        case 2:return new RomanceFragment();
                    }
                    return null;
                }
    
                @Override
                public int getCount(){
                    return jumlah_tab;
                }
            }
    
            viewPager2.registerOnPageChangeCallback(new ViewPager2.OnPageChangeCallback() {
                @Override
                public void onPageSelected(int position) {
                    super.onPageSelected(position);
                    tabLayout.getTabAt(position).select();
                }
            });
    
        }
    }
        
***RomanceFragment.java***
      
      package com.example.intentapp;
      
      
      import android.content.Intent;
      import android.os.Bundle;
      import android.util.Log;
      import android.view.LayoutInflater;
      import android.view.Menu;
      import android.view.MenuInflater;
      import android.view.MenuItem;
      import android.view.View;
      import android.view.ViewGroup;
      import android.widget.Button;
      import android.widget.Toast;
      
      import androidx.fragment.app.Fragment;
      
      
      
      public class RomanceFragment extends Fragment {
      
          private static final String TAG = "RomanceFragment";
      
          @Override
          public View onCreateView(LayoutInflater inflater, ViewGroup container,
                                   Bundle savedInstanceState) {
              // Inflate the layout for this fragment
              setHasOptionsMenu(true);
              View view = inflater.inflate(R.layout.fragment_romance, container, false);
      
              // Find the button by its ID
              Button argantaraButton = view.findViewById(R.id.argantara);
              Button galaksiButton = view.findViewById(R.id.galaksi);
              Button mohondoarestuButton = view.findViewById(R.id.mohondoarestu);
      
              // Set click listener for each button
              argantaraButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Centurygirl button clicked");
                      playVideo(R.raw.argantara);
                  }
              });
      
              galaksiButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Cheerup button clicked");
                      playVideo(R.raw.galaksi);
                  }
              });
      
              mohondoarestuButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Hiddenlove button clicked");
                      playVideo(R.raw.mohondoarestu);
                  }
              });
      
              return view;
          }
      
          @Override
          public void onCreateOptionsMenu(Menu menu, MenuInflater inflater) {
              inflater.inflate(R.menu.menu_tab, menu);
          }
      
          @Override
          public boolean onOptionsItemSelected(MenuItem item) {
              if (item.getItemId() == R.id.tab_romance) {
                  Toast.makeText(getActivity(), "Clicked on " + item.getTitle(), Toast.LENGTH_SHORT)
                          .show();
              }
              return true;
          }
      
          private void playVideo(int videoResource) {
              String videoPath = "android.resource://" + getActivity().getPackageName() + "/" + videoResource;
              Intent intent = new Intent(getActivity(), VideoPlayerActivity.class);
              intent.putExtra("VIDEO_PATH", videoPath);
              startActivity(intent);
          }
      }

***ComedyFragment.java***  
  
      package com.example.intentapp;
      
      
      import android.content.Intent;
      import android.os.Bundle;
      import android.util.Log;
      import android.view.LayoutInflater;
      import android.view.Menu;
      import android.view.MenuInflater;
      import android.view.MenuItem;
      import android.view.View;
      import android.view.ViewGroup;
      import android.widget.Button;
      import android.widget.Toast;
      
      import androidx.fragment.app.Fragment;
      
      
      public class ComedyFragment extends Fragment {
      
          private static final String TAG = "ComedyFragment";
      
          @Override
          public View onCreateView(LayoutInflater inflater, ViewGroup container,
                                   Bundle savedInstanceState) {
              // Inflate the layout for this fragment
              setHasOptionsMenu(true);
              View view = inflater.inflate(R.layout.fragment_comedy, container, false);
      
              // Find the button by its ID
              Button cektokosebelahButton = view.findViewById(R.id.cektokosebelah);
              Button helloghostButton = view.findViewById(R.id.helloghost);
              Button srimulatButton = view.findViewById(R.id.srimulat);
      
              // Set click listener for each button
              cektokosebelahButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Cektokosebelah2 button clicked");
                      playVideo(R.raw.cektokosebelah);
                  }
              });
      
              helloghostButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Friendzone button clicked");
                      playVideo(R.raw.helloghost);
                  }
              });
      
              srimulatButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "HospitalPlaylist button clicked");
                      playVideo(R.raw.srimulat);
                  }
              });
      
              return view;
          }
      
          @Override
          public void onCreateOptionsMenu(Menu menu, MenuInflater inflater) {
              inflater.inflate(R.menu.menu_tab, menu);
          }
      
          @Override
          public boolean onOptionsItemSelected(MenuItem item) {
              if (item.getItemId() == R.id.tab_comedy) {
                  Toast.makeText(getActivity(), "Clicked on " + item.getTitle(), Toast.LENGTH_SHORT)
                          .show();
              }
              return true;
          }
      
          private void playVideo(int videoResource) {
              String videoPath = "android.resource://" + getActivity().getPackageName() + "/" + videoResource;
              Intent intent = new Intent(getActivity(), VideoPlayerActivity.class);
              intent.putExtra("VIDEO_PATH", videoPath);
              startActivity(intent);
          }
      }

***ActionFragment.java***

      package com.example.intentapp;
      
      
      import android.content.Intent;
      import android.os.Bundle;
      import android.util.Log;
      import android.view.LayoutInflater;
      import android.view.Menu;
      import android.view.MenuInflater;
      import android.view.MenuItem;
      import android.view.View;
      import android.view.ViewGroup;
      import android.widget.Button;
      import android.widget.Toast;
      
      import androidx.fragment.app.Fragment;
      
      
      public class ActionFragment extends Fragment {
      
          private static final String TAG = "ActionFragment";
      
          @Override
          public View onCreateView(LayoutInflater inflater, ViewGroup container,
                                   Bundle savedInstanceState) {
              // Inflate the layout for this fragment
              setHasOptionsMenu(true);
              View view = inflater.inflate(R.layout.fragment_action, container, false);
      
              // Find the button by its ID
              Button avengerButton = view.findViewById(R.id.avenger);
              Button fastandfuriousButton = view.findViewById(R.id.fastandfurious);
              Button spidermanButton = view.findViewById(R.id.spiderman);
      
              // Set click listener for each button
              avengerButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Avenger button clicked");
                      playVideo(R.raw.avenger);
                  }
              });
      
              fastandfuriousButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "MyName button clicked");
                      playVideo(R.raw.fastandfurious);
                  }
              });
      
              spidermanButton.setOnClickListener(new View.OnClickListener() {
                  @Override
                  public void onClick(View v) {
                      Log.d(TAG, "Spiderman button clicked");
                      playVideo(R.raw.spiderman);
                  }
              });
      
              return view;
          }
      
          @Override
          public void onCreateOptionsMenu(Menu menu, MenuInflater inflater) {
              inflater.inflate(R.menu.menu_tab, menu);
          }
      
          @Override
          public boolean onOptionsItemSelected(MenuItem item) {
              if (item.getItemId() == R.id.tab_action) {
                  Toast.makeText(getActivity(), "Clicked on " + item.getTitle(), Toast.LENGTH_SHORT)
                          .show();
              }
              return true;
          }
      
          private void playVideo(int videoResource) {
              String videoPath = "android.resource://" + getActivity().getPackageName() + "/" + videoResource;
              Intent intent = new Intent(getActivity(), VideoPlayerActivity.class);
              intent.putExtra("VIDEO_PATH", videoPath);
              startActivity(intent);
          }
      }

**Layout**

***activity_count.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout
          xmlns:android="http://schemas.android.com/apk/res/android"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          xmlns:tools="http://schemas.android.com/tools"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          tools:context=".CountActivity">
      
          <ImageView
              android:id="@+id/background"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:background="@drawable/bgcount"
              android:adjustViewBounds="true"
              android:scaleType="centerCrop" />
      
          <Button
              android:id="@+id/button_toast"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginEnd="8dp"
              android:layout_marginStart="8dp"
              android:layout_marginTop="8dp"
              android:background="@color/black"
              android:onClick="showToast"
              android:text="@string/button_label_toast"
              android:textColor="@android:color/white"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent"
              tools:ignore="UsingOnClickInXml"/>
      
          <Button
              android:id="@+id/button_count"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginEnd="8dp"
              android:layout_marginStart="8dp"
              android:layout_marginBottom="8dp"
              android:background="@color/black"
              android:onClick="countUp"
              android:text="@string/button_label_count"
              android:textColor="@android:color/white"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintBottom_toBottomOf="parent"
              tools:ignore="UsingOnClickInXml" />
      
          <TextView
              android:id="@+id/show_count"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginEnd="8dp"
              android:text="@string/count_initial_value"
              android:textAlignment="center"
              android:textColor="@color/black"
              android:textSize="160sp"
              android:textStyle="bold"
              app:layout_constraintBottom_toTopOf="@+id/button_count"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintHorizontal_bias="0.0"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toBottomOf="@+id/button_toast"
              tools:ignore="RtlCompat" />
      
      </androidx.constraintlayout.widget.ConstraintLayout>

***activity_hello.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout    xmlns:android="http://schemas.android.com/apk/res/android"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          xmlns:tools="http://schemas.android.com/tools"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          tools:context=".HelloActivity">
      
          <ImageView
              android:id="@+id/background"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:background="@drawable/bghello"
              android:adjustViewBounds="true"
              android:scaleType="centerCrop"/>
      
          <TextView
              android:id="@+id/txthello"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:gravity="center"
              android:text="Hello World!!"
              android:textColor="@color/white"
              android:textSize="20pt"
              android:textStyle="bold"
              app:layout_constraintBottom_toBottomOf="parent"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintHorizontal_bias="0.503"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent"
              app:layout_constraintVertical_bias="0.413"
              tools:ignore="TextSizeCheck" />
      
      </androidx.constraintlayout.widget.ConstraintLayout>

***activity_main.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <ScrollView
          xmlns:android="http://schemas.android.com/apk/res/android"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          xmlns:tools="http://schemas.android.com/tools"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          android:background="@drawable/background"
          tools:context=".MainActivity">
      
          <RelativeLayout
              android:layout_width="match_parent"
              android:layout_height="wrap_content">
      
              <TextView
                  android:id="@+id/title_view"
                  android:layout_width="wrap_content"
                  android:layout_height="wrap_content"
                  android:layout_centerHorizontal="true"
                  android:text="Menu Program"
                  android:fontFamily="serif"
                  android:textColor="@color/black"
                  android:textStyle="bold"
                  android:textSize="35sp"
                  android:layout_marginTop="35dp"/>
      
              <GridLayout
                  android:layout_width="match_parent"
                  android:layout_height="match_parent"
                  android:layout_below="@+id/title_view"
                  android:layout_marginStart="35dp"
                  android:layout_marginTop="45dp"
                  android:layout_marginEnd="40dp"
                  android:layout_marginBottom="35dp"
                  android:columnCount="10"
                  android:rowCount="10">
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu1"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="0"
                      android:layout_rowWeight="1"
                      android:layout_column="0"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/world" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="sans-serif"
                              android:text="HELLO WORLD!"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu2"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="0"
                      android:layout_rowWeight="1"
                      android:layout_column="1"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/math" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="serif"
                              android:text="FIBONACCI"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu3"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="1"
                      android:layout_rowWeight="1"
                      android:layout_column="0"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/coffe" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="serif"
                              android:text="ICE COLD!"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu4"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="1"
                      android:layout_rowWeight="1"
                      android:layout_column="1"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/message" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="serif"
                              android:text="TWO ACTIVITY"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu5"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="2"
                      android:layout_rowWeight="1"
                      android:layout_column="0"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/jam" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="serif"
                              android:text="ALARM"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu6"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="2"
                      android:layout_rowWeight="1"
                      android:layout_column="1"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/maps" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="serif"
                              android:text="G-MAPS"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
                  <androidx.cardview.widget.CardView
                      android:id="@+id/cdMenu7"
                      android:layout_width="80dp"
                      android:layout_height="100dp"
                      android:layout_row="3"
                      android:layout_rowWeight="1"
                      android:layout_column="0"
                      android:layout_columnWeight="1"
                      android:layout_gravity="fill"
                      android:layout_margin="8dp"
                      app:cardCornerRadius="8dp"
                      app:cardElevation="8dp">
      
                      <LinearLayout
                          android:layout_width="wrap_content"
                          android:layout_height="wrap_content"
                          android:layout_gravity="center_vertical|center_horizontal"
                          android:gravity="center"
                          android:orientation="vertical">
      
                          <ImageView
                              android:layout_width="50dp"
                              android:layout_height="50dp"
                              android:src="@drawable/movie" />
      
                          <TextView
                              android:layout_width="wrap_content"
                              android:layout_height="wrap_content"
                              android:layout_marginTop="10dp"
                              android:fontFamily="serif"
                              android:text="MOVIES"
                              android:textAlignment="center"
                              android:textColor="@color/black"
                              android:textStyle="bold" />
                      </LinearLayout>
                  </androidx.cardview.widget.CardView>
      
              </GridLayout>
      
              <TextView
                  android:id="@+id/bottom_text"
                  android:layout_width="wrap_content"
                  android:layout_height="wrap_content"
                  android:layout_marginBottom="35dp"
                  android:layout_alignParentBottom="true"
                  android:layout_centerHorizontal="true"
                  android:fontFamily="monospace"
                  android:text="© 2024 Cahyo Hidayatullah"
                  android:textColor="@color/black"
                  android:textSize="15sp"
                  android:textStyle="bold" />
      
          </RelativeLayout>
      
      </ScrollView>

***activity_movie.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          xmlns:tools="http://schemas.android.com/tools"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          android:background="@color/white"
          tools:context=".FragmentActivity">
      
      
          <com.google.android.material.tabs.TabLayout
              android:id="@+id/tab"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:background="@color/choco"
              app:tabSelectedTextColor="@color/white"
              app:tabIndicatorColor="@color/white"
              tools:layout_editor_absoluteX="1dp"
              tools:layout_editor_absoluteY="3dp"
              tools:ignore="MissingConstraints">
      
              <com.google.android.material.tabs.TabItem
                  android:layout_width="wrap_content"
                  android:layout_height="wrap_content"
                  android:text="action"
                  tools:layout_editor_absoluteX="0dp"
                  tools:layout_editor_absoluteY="3dp" />
      
              <com.google.android.material.tabs.TabItem
                  android:layout_width="wrap_content"
                  android:layout_height="wrap_content"
                  android:text="comedy" />
      
              <com.google.android.material.tabs.TabItem
                  android:layout_width="wrap_content"
                  android:layout_height="wrap_content"
                  android:text="romance" />
          </com.google.android.material.tabs.TabLayout>
      
          <androidx.viewpager2.widget.ViewPager2
              android:id="@+id/view"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:layout_marginTop="50dp"
              android:background="@color/white"
              tools:layout_editor_absoluteX="1dp"
              tools:layout_editor_absoluteY="52dp" />
      
      </androidx.constraintlayout.widget.ConstraintLayout>

***activity_sianida.xml***
      
      <?xml version="1.0" encoding="utf-8"?>
      <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          xmlns:tools="http://schemas.android.com/tools"
          tools:context=".SianidaActivity">
      
          <TextView
              android:id="@+id/article_heading"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:background="@color/colorPrimary"
              android:padding="@dimen/padding_regular"
              android:text="@string/article_title"
              android:textAppearance="@android:style/TextAppearance.DeviceDefault.Large"
              android:textColor="@android:color/white"
              android:textStyle="bold" />
      
          <ScrollView
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_below="@id/article_heading">
      
              <LinearLayout
                  android:layout_width="match_parent"
                  android:layout_height="wrap_content"
                  android:orientation="vertical">
      
                  <TextView
                      android:id="@+id/article_subheading"
                      android:layout_width="match_parent"
                      android:layout_height="wrap_content"
                      android:padding="@dimen/padding_regular"
                      android:text="@string/article_subtitle"
                      android:textAlignment="center"
                      android:textAppearance="@android:style/TextAppearance.DeviceDefault"
                      android:textColor="#8D6E63" />
      
                  <TextView
                      android:id="@+id/article"
                      android:layout_width="wrap_content"
                      android:layout_height="wrap_content"
                      android:autoLink="web"
                      android:lineSpacingExtra="@dimen/line_spacing"
                      android:padding="@dimen/padding_regular"
                      android:text="@string/article_text"
                      tools:ignore="VisualLintLongText" />
              </LinearLayout>
          </ScrollView>
      </RelativeLayout>

***activity_twoact.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout
          xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          xmlns:tools="http://schemas.android.com/tools"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          tools:context=".TwoactActivity">
      
          <ImageView
              android:id="@+id/background"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:adjustViewBounds="true"
              android:scaleType="centerCrop"
              android:src="@drawable/bgtwoact" />
      
          <TextView
              android:id="@+id/text_header_reply"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginLeft="8dp"
              android:layout_marginTop="16dp"
              android:text="@string/text_header_reply"
              android:textAppearance="@style/TextAppearance.AppCompat.Medium"
              android:textStyle="bold"
              android:visibility="invisible"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent"/>
      
          <TextView
              android:id="@+id/text_message_reply"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginLeft="8dp"
              android:layout_marginTop="8dp"
              android:visibility="invisible"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toBottomOf="@+id/text_header_reply" />
      
          <Button
              android:id="@+id/button_main"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginBottom="16dp"
              android:layout_marginRight="16dp"
              android:text="@string/button_main"
              android:background="@color/biru"
              android:onClick="LaunchSecondActivity"
              app:layout_constraintBottom_toBottomOf="parent"
              app:layout_constraintRight_toRightOf="parent"
              tools:ignore="UsingOnClickInXml"/>
      
          <EditText
              android:id="@+id/editText_main"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginEnd="8dp"
              android:layout_marginBottom="16dp"
              android:ems="10"
              android:hint="@string/editText_main"
              android:inputType="textLongMessage"
              android:minHeight="48dp"
              app:layout_constraintBottom_toBottomOf="parent"
              app:layout_constraintEnd_toStartOf="@+id/button_main"
              app:layout_constraintStart_toStartOf="parent" />
      </androidx.constraintlayout.widget.ConstraintLayout>

***activity_twoact2.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <androidx.constraintlayout.widget.ConstraintLayout
          xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          xmlns:tools="http://schemas.android.com/tools"
          xmlns:app="http://schemas.android.com/apk/res-auto"
          tools:context=".Twoact2Activity">
      
          <ImageView
              android:id="@+id/background"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              android:adjustViewBounds="true"
              android:scaleType="centerCrop"
              android:src="@drawable/bgtwoact2" />
      
          <TextView
              android:id="@+id/text_header"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginLeft="8dp"
              android:layout_marginTop="16dp"
              android:text="@string/text_header"
              android:textAppearance="@style/TextAppearance.AppCompat.Medium"
              android:textStyle="bold"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent" />
      
          <TextView
              android:id="@+id/text_message"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginLeft="8dp"
              android:layout_marginTop="8dp"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toBottomOf="@+id/text_header" />
      
          <Button
              android:id="@+id/button_second"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginBottom="16dp"
              android:layout_marginRight="16dp"
              android:text="@string/buttton_second"
              android:onClick="returnReply"
              android:background="@color/biru"
              app:layout_constraintBottom_toBottomOf="parent"
              app:layout_constraintRight_toRightOf="parent"
              tools:ignore="UsingOnClickInXml" />
      
          <EditText
              android:id="@+id/editText_second"
              android:layout_width="0dp"
              android:layout_height="wrap_content"
              android:layout_marginStart="8dp"
              android:layout_marginEnd="8dp"
              android:layout_marginBottom="16dp"
              android:ems="10"
              android:hint="@string/editText_second"
              android:inputType="textLongMessage"
              android:minHeight="48dp"
              app:layout_constraintBottom_toBottomOf="parent"
              app:layout_constraintEnd_toStartOf="@+id/button_second"
              app:layout_constraintStart_toStartOf="parent" />
      </androidx.constraintlayout.widget.ConstraintLayout>

***activity_video_player.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="match_parent">
      
          <VideoView
              android:id="@+id/videoView"
              android:layout_width="match_parent"
              android:layout_height="match_parent"/>
      </RelativeLayout>

***activity_action.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="wrap_content"
          xmlns:tools="http://schemas.android.com/tools"
          android:padding="15dp"
          android:background="@drawable/bg_film"
          tools:context=".ActionFragment">
      
          <ImageView
              android:id="@+id/imgMovie"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:src="@drawable/avengersendgame" />
      
          <TextView
              android:id="@+id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_marginStart="16dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="AVENGERS : END GAME"/>
      
          <TextView
              android:id="@+id/Deskription"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="10dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="The story of the Avengers efforts to restore parts of the universe that were destroyed after the events of Infinity War. Using time travel technology, they attempt to steal the Infinity Stones to overcome the destruction caused by Thanos. An epic battle takes place, culminating in a great sacrifice and victory that changes the fate of the universe."/>
      
      
          <Button
              android:id="@+id/avenger"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription"
              android:text="Watch Trailer Now"
              android:onClick="playAvengerTrailer"/>
      
      
          <ImageView
              android:id="@+id/imgMovie2"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:layout_marginTop="200dp"
              android:src="@drawable/forious"/>
      
          <TextView
              android:id="@+id/tvTitle2"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie2"
              android:layout_marginStart="16dp"
              android:layout_marginTop="200dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="FAST AND FURIOUS 9"/>
      
          <TextView
              android:id="@+id/Deskription2"
              android:layout_toRightOf="@id/imgMovie2"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="210dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Dom Toretto (Vin Diesel) menjalani kehidupan yang tenang dengan Letty dan putranya, Brian kecil, tetapi mereka tahu bahwa bahaya selalu mengintai. Kali ini, ancaman itu akan memaksa Dom untuk menghadapi kesalahan dari masa lalunya jika dia ingin menyelamatkan orang yang paling dia cintai.
              Krunya bergabung bersama untuk menghentikan sesuatu yang dapat menghancurkan dunia.
              serangan dipimpin oleh pembunuh paling terampil dan pengemudi yang sangat handal dan juga merupakan saudara laki-laki Dom yang ditinggalkan, Jakob (John Cena)"/>
      
          <Button
              android:id="@+id/fastandfurious"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie2"
              android:layout_below="@id/Deskription2"
              android:text="Watch Trailer Now"
              android:onClick="playFastandfuriousTrailer"/>
      
          <ImageView
              android:id="@+id/imgMovie3"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:layout_marginTop="400dp"
              android:src="@drawable/spiderman"/>
      
          <TextView
              android:id="@+id/tvTitle3"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie3"
              android:layout_marginStart="16dp"
              android:layout_marginTop="400dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="SPIDERMAN : NO WAY HOME"/>
      
          <TextView
              android:id="@+id/Deskription3"
              android:layout_toRightOf="@id/imgMovie3"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="420dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Peter Parker tries to fix the mess after his Spider-Man identity is revealed and his personal life is threatened. Peter enlists the help of Doctor Strange to use magic gone wrong, opening the multiverse and bringing forth a version of Spider-Man from a parallel reality. Along with the other Spider-Men, Peter confronts villains from the past and faces serious consequences in their efforts to right those wrongs."
              />
      
          <Button
              android:id="@+id/spiderman"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie3"
              android:layout_below="@id/Deskription3"
              android:text="Watch Trailer Now"
              android:onClick="playSpidermanTrailer" />
      </RelativeLayout>

***activity_comedy.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <RelativeLayout
          xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="wrap_content"
          android:background="@drawable/bg_film"
          android:padding="15dp">
      
          <ImageView
              android:id="@+id/imgMovie"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:src="@drawable/cektokosebelah"/>
      
          <TextView
              android:id="@+id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_marginStart="16dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="CEK TOKO SEBELAH"/>
      
          <TextView
              android:id="@+id/Deskription"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="10dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Cek Toko Sebelah adalah film drama komedi Indonesia tahun 2016 yang ditulis dan disutradarai oleh Ernest Prakasa. Ide cerita film ini dibuat berdasarkan pada realitas etnis Tionghoa saat anak beranjak dewasa, kuliah yang tinggi, mirisnya ujung-ujungnya bekerja di toko orang tuanya sendiri."/>
      
          <Button
              android:id="@+id/cektokosebelah"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription"
              android:text="Watch Trailer Now"
              android:onClick="playCektokosebelah2Trailer"/>
      
          <ImageView
              android:id="@+id/imgMovie2"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:layout_marginTop="200dp"
              android:src="@drawable/helloghost"/>
      
          <TextView
              android:id="@+id/tvTitle2"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_marginStart="16dp"
              android:layout_marginTop="200dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="HELLO GHOST"/>
      
          <TextView
              android:id="@+id/Deskription2"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="210dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Setelah percobaan bunuh dirinya gagal, Kresna mendapati dirinya dikuntit oleh empat hantu dengan karakter yang berbeda-beda. Kuatno, hantu tua bangka yang mata keranjang, Bima, hantu perokok yang dulunya adalah supir angkot, Lita, hantu melankolis yang mudah menangis, dan Chika, hantu kecil yang senang menggunakan sepatu roda.
              Mereka hanya akan pergi jika Kresna mau memenuhi permintaan mereka masing-masing. Kresna tidak berdaya, akhirnya menuruti keinginan mereka. Namun ternyata, dalam proses menuntaskan misi tersebut, Kresna sendiri yang menemukan makna baru bagi hidupnya dan juga cintanya pada Suster Linda."
              />
      
          <Button
              android:id="@+id/helloghost"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription2"
              android:text="Watch Trailer Now"
              android:onClick="playHelloGhostTrailer"/>
      
          <ImageView
              android:id="@+id/imgMovie3"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:layout_marginTop="400dp"
              android:src="@drawable/srimulat"/>
      
          <TextView
              android:id="@+id/tvTitle3"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_marginStart="16dp"
              android:layout_marginTop="400dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="SRIMULAT"/>
      
          <TextView
              android:id="@+id/Deskription3"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="410dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Kelompok lawak Srimulat yang tengah populer di Jawa, mendadak terganggu penampilannya karena muncul pemain kendang yang lebih lucu bernama Gepeng. Tepat pada saat itu, sebuah telegram dari Ibukota datang, mengundang Srimulat tampil di TV Nasional." />
      
          <Button
              android:id="@+id/srimulat"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription3"
              android:text="Watch Trailer Now"
              android:onClick="playSrimulatTrailer"/>
      </RelativeLayout>

***activity_romance.xml***

      <?xml version="1.0" encoding="utf-8"?>
      <RelativeLayout
          xmlns:android="http://schemas.android.com/apk/res/android"
          android:layout_width="match_parent"
          android:layout_height="wrap_content"
          android:background="@drawable/bg_film"
          android:padding="15dp">
      
          <ImageView
              android:id="@+id/imgMovie"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:src="@drawable/argantara"/>
      
          <TextView
              android:id="@+id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginLeft="16dp"
              android:layout_toRightOf="@id/imgMovie"
              android:text="ARGANTARA"
              android:textColor="@color/white"
              android:textSize="16sp" />
      
          <TextView
              android:id="@+id/Deskription"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/tvTitle"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginTop="16dp"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Kehidupan SYERA, seorang siswi SMA berusia 16 tahun mendadak berubah ketika ia menikah muda dengan ARGANTARA, seorang cowok bandel yang dibencinya di sekolah dan juga ketua geng Agberos. Sifat dan sikap keduanya yang bertolak belakang membuat rumah tangga mereka penuh pertengkaran." />
      
          <Button
              android:id="@+id/argantara"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription"
              android:text="Watch Trailer Now"
              android:onClick="playArgantaraTrailer"/>
      
          <ImageView
              android:id="@+id/imgMovie2"
              android:layout_width="150dp"
              android:layout_height="170dp"
              android:layout_marginTop="200dp"
              android:src="@drawable/galaksi"/>
      
          <TextView
              android:id="@+id/tvTitle2"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_marginStart="16dp"
              android:layout_marginTop="200dp"
              android:textSize="16sp"
              android:textColor="@color/white"
              android:text="GALAKSI"/>
      
          <TextView
              android:id="@+id/Deskription2"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_below="@id/tvTitle"
              android:layout_marginStart="16dp"
              android:layout_marginLeft="12dp"
              android:layout_marginTop="210dp"
              android:layout_toRightOf="@id/imgMovie"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="GALAKSI, ketua geng Ravispa dari SMA Ganesha, berseteru dengan musuh bebuyutannya, geng Avegar - geng milik SMA Kencana. Ravispa bagi Galaksi adalah keluarga, pelarian dari persoalan di rumah yang rumit dan berlarut. Hadir KEJORA ke dalam hidup Galaksi, seorang gadis yang bercita-cita jadi anggota Paskibra di sekolah. Pertemuan mereka terjadi ketika Kejora terancam terlambat masuk seleksi Paskibra, Satu-satunya yang bisa membawanya ke sekolah adalah Galaksi. Dari sanalah kisah mereka yang rumit mulai terjalin menjadi kisah cinta. Kejora terancam gagal masuk seleksi paskibra dan menyalahkan Galaksi.
              Keberanian Kejora ini membuat Galaksi tertarik padanya, dan berusaha untuk mendekat. Namun hal ini membuat Kejora masuk dalam lingkaran konflik Ravispa dan Avegar.
              Kejora menjadi target Avegar sehingga memicu tawuran antar geng dua Sekolah itu. Melihat Kejora terlibat cukup jauh dengan Ravispa, Abraham, senior Paskibra yang diam-diam menaruh hati pada Kejora memberi ultimatum kepada Kejora untuk menjauhi Galaksi. Kejora berada dalam posisi yang membingungkan, hingga kemudian sebuah momen membuat Kejora memahami bahwa perilaku Galaksi berawal dari kekerasan yang dialami dalam keluarganya. Kejora makin dekat dengan Galaksi dan jatuh cinta dengannya.
              Kehadiran Kejora ditentang Geng Ravispa karena membuat Galaksi menjadi lemah, sementara kedekatan Galaksi dan Kejora mengancam keberhasilan Kejora lolos seleksi Paskibraka." />
      
          <Button
              android:id="@+id/galaksi"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription2"
              android:text="Watch Trailer Now"
              android:onClick="playGalaksiTrailer"/>
      
          <ImageView
              android:id="@+id/imgMovie3"
              android:layout_width="150dp"
              android:layout_height="175dp"
              android:layout_marginTop="400dp"
              android:src="@drawable/gambar"/>
      
          <TextView
              android:id="@+id/tvTitle3"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_marginStart="16dp"
              android:layout_marginLeft="7dp"
              android:layout_marginTop="400dp"
              android:layout_toRightOf="@id/imgMovie"
              android:text="MOHON DOA RESTU"
              android:textColor="@color/white"
              android:textSize="16sp" />
      
          <TextView
              android:id="@+id/Deskription3"
              android:layout_width="match_parent"
              android:layout_height="wrap_content"
              android:layout_below="@id/tvTitle"
              android:layout_marginStart="16dp"
              android:layout_marginLeft="16dp"
              android:layout_marginTop="410dp"
              android:layout_toRightOf="@id/imgMovie"
              android:maxLines="5"
              android:textColor="@color/white"
              android:text="Mel (Syifa Hadju) adalah teman masa kanak-kanak Satya (Jefri Nichol). Banyak menghabiskan waktu bersama sebagai sahabat sejak usia dini, keduanya akrab dan saling menyayangi. Namun Mel dan Satya kecil harus berpisah karena pindah ke tempat yang berjauhan.
              Saat berjumpa kembali di usia dewasa, Mel dan Satya dijodohkan oleh kedua orang tua mereka. Mel tidak keberatan, demikian pula Satya karena mereka sama-sama saling suka. Proses perjodohan berjalan lancar dan pernikahan mulai dipersiapkan. Akan tetapi konflik mulai timbul karena pernikahan tersebut diatur dengan detail oleh kedua orang tua Mel dan Satya.
              Widi (Cut Mini) dan Ira (Sarah Sechan), ibu dari Mel serta Satya sama-sama ngotot ingin mewujudkan sebuah pernikahan yang mereka inginkan, tanpa minta persetujuan dari anak-anaknya. Mel mulai merasa tidak nyaman karena selalu diatur, apalagi Satya tidak berani menolak apapun yang diucapkan oleh ibunya. Mel kecewa karena lelaki yang dia harapkan menjadi pemimpin dalam keluarga ternyata selalu nurut ucapan ibu dan tidak mendengarkan apa yang diinginkan Mel." />
      
          <Button
              android:id="@+id/mohondoarestu"
              android:layout_width="wrap_content"
              android:layout_height="wrap_content"
              android:layout_marginStart="10dp"
              android:layout_marginTop="10dp"
              android:layout_toRightOf="@id/imgMovie"
              android:layout_below="@id/Deskription3"
              android:text="Watch Trailer Now"
              android:onClick="playMohondoarestuTrailer"/>
      </RelativeLayout>

**HASIL RUN**

https://github.com/Hazelnuts22/PROJECT-UAS-PEMROGRAMAN-MOBILE/assets/115677959/7d9bdbc9-749d-45b3-8682-ff2eb703858e

<p align="center"><b>TERIMAKASIH </b></p>
<p align="center">Cahyo Hidayatullah</p>

  

      


