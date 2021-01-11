# Preeklampsia
package com.example.d_preeklampsia;
import android.app.Activity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends Activity {
public static final String DEVICE_EXTRA = "com.example.d_preeklampsia.SOCKET";
public static final String DEVICE_UUID = "com.example.d_preeklampsia.uuid";
public static final String BUFFER_SIZE = "com.example.d_preeklampsia.buffersize";
Button buttontd,buttonsp;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
buttontd= (Button) findViewById(R.id.Tomboltd);
buttonsp= (Button) findViewById(R.id.Tombolsp);
buttontd.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
Intent intent = new Intent (MainActivity.this,BacaBluetooth.class);
startActivity(intent);
}
});
buttonsp.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
Intent intent = new Intent (MainActivity.this,Pedoman.class);
startActivity(intent);
}
});
}
}
