# Preeklampsia
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
<android.support.v7.widget.CardView
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="10dp"
android:clickable="true"
android:focusable="true"
app:cardBackgroundColor="@color/cardview_shadow_end_color"
app:cardCornerRadius="6dp"
app:cardElevation="5dp" >
<LinearLayout
android:layout_width="match_parent"
android:layout_height="110dp"
android:background="@drawable/upframe"
android:gravity="center"
android:orientation="horizontal"
android:padding="10dp" />
</android.support.v7.widget.CardView>
<android.support.v7.widget.CardView
android:layout_width="200dp"
android:layout_height="wrap_content"
android:layout_marginTop="15dp"
android:layout_marginLeft="0dp"
android:layout_marginRight="0dp"
android:layout_marginBottom="2dp"
android:orientation="horizontal"
android:layout_gravity="center"/>
<android.support.v7.widget.CardView
android:layout_width="200dp"
android:layout_height="200dp"
android:layout_margin="0dp"
android:clickable="true"
app:cardCornerRadius="15dp"
app:cardElevation="3dp"
app:cardBackgroundColor="@color/cardview_shadow_end_color"
android:focusable="true"
android:layout_gravity="center">
<Button
android:id="@+id/Tomboltd"
android:layout_width="200dp"
android:layout_height="200dp"
android:backgroundTint="@color/cardview_shadow_end_color"
android:layout_gravity="center" />
<ImageView
android:layout_width="200dp"
android:layout_height="match_parent"
android:src="@drawable/tens"
android:layout_gravity="center"
android:layout_alignParentEnd="true"
android:contentDescription="@string/periksa_tekanan_darah_ibu
"
/>
</android.support.v7.widget.CardView>

<android.support.v7.widget.CardView
android:layout_width="200dp"
android:layout_height="wrap_content"
android:layout_marginTop="15dp"
android:layout_marginLeft="0dp"
android:layout_marginRight="0dp"
android:layout_marginBottom="2dp"
android:orientation="horizontal"
android:layout_gravity="center"/>
<android.support.v7.widget.CardView
android:layout_width="200dp"
android:layout_height="200dp"
android:layout_margin="5dp"
android:clickable="true"
app:cardCornerRadius="3dp"
app:cardElevation="3dp"
app:cardBackgroundColor="@color/cardview_shadow_end_color"
android:focusable="true"
android:layout_gravity="center">
<Button
android:id="@+id/Tombolsp"
android:layout_width="200dp"
android:layout_height="200dp"
android:layout_gravity="center"
android:backgroundTint="@color/cardview_shadow_end_color"
tools:targetApi="LOLLIPOP"/>
<ImageView
android:layout_width="200dp"
android:layout_height="200dp"
android:src="@drawable/re"
android:layout_gravity="center"
android:layout_alignParentBottom="true"
android:layout_alignParentEnd="true"
android:contentDescription="@string/sistem_pakar_deteksi_
preeklampsia"
/>
</android.support.v7.widget.CardView>
<TextView
android:padding="30sp"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:text="Design by TEKNIK ELEKTRO UNIB"
android:gravity="center"
android:textStyle="bold"
android:textSize="15sp"
android:textColor="#FFF"
/>
</LinearLayout>
