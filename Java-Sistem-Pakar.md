# Preeklampsia
package com.example.d_preeklampsia;
import android.app.Activity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.TextView;
public class SistemPakar extends Activity {
Button btnProses, btnReset;
TextView tvOutput;
CheckBox chkGejala1, chkGejala2, chkGejala3, chkGejala4, 
chkGejala5, chkGejala6,
chkGejala7, chkGejala8, chkGejala9, chkGejala10, 
chkGejala11, chkGejala12,
chkGejala13, chkGejala14, chkGejala15, chkGejala16, 
chkGejala17, chkGejala18,
chkGejala19, chkGejala20, chkGejala21, chkGejala22, 
chkGejala23, chkGejala24,
chkGejala25, chkGejala26, chkGejala27, chkGejala28;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_sistem_pakar);
btnProses = (Button) findViewById(R.id.button1);
btnReset = (Button) findViewById(R.id.button2);
tvOutput = (TextView) findViewById(R.id.textView);
chkGejala1 = (CheckBox) findViewById(R.id.cb1);
chkGejala2 = (CheckBox) findViewById(R.id.cb2);
chkGejala3 = (CheckBox) findViewById(R.id.cb3);
chkGejala4 = (CheckBox) findViewById(R.id.cb4);
chkGejala5 = (CheckBox) findViewById(R.id.cb5);
chkGejala6 = (CheckBox) findViewById(R.id.cb6);
chkGejala7 = (CheckBox) findViewById(R.id.cb7);
chkGejala8 = (CheckBox) findViewById(R.id.cb8);
chkGejala9 = (CheckBox) findViewById(R.id.cb9);
chkGejala10 = (CheckBox) findViewById(R.id.cb10);
chkGejala11 = (CheckBox) findViewById(R.id.cb11);
chkGejala12 = (CheckBox) findViewById(R.id.cb12);
chkGejala13 = (CheckBox) findViewById(R.id.cb13);
chkGejala14 = (CheckBox) findViewById(R.id.cb14);
chkGejala15 = (CheckBox) findViewById(R.id.cb15);
chkGejala16 = (CheckBox) findViewById(R.id.cb16);
chkGejala17 = (CheckBox) findViewById(R.id.cb17);
chkGejala18 = (CheckBox) findViewById(R.id.cb18);
chkGejala19 = (CheckBox) findViewById(R.id.cb19);
chkGejala20 = (CheckBox) findViewById(R.id.cb20);
chkGejala21 = (CheckBox) findViewById(R.id.cb21);
chkGejala22 = (CheckBox) findViewById(R.id.cb22);
chkGejala23 = (CheckBox) findViewById(R.id.cb23);
chkGejala24 = (CheckBox) findViewById(R.id.cb24);
chkGejala25 = (CheckBox) findViewById(R.id.cb25);
chkGejala26 = (CheckBox) findViewById(R.id.cb26);
chkGejala27 = (CheckBox) findViewById(R.id.cb27);
chkGejala28 = (CheckBox) findViewById(R.id.cb28);
btnProses.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
Certainty_factor();
}
});}
private void Certainty_factor() {
float CFe[] = {0.6f, 0.0f, 0.7f, 0.6f, 0.4f, 0.0f, -0.2f, -
0.2f, 0.6f, 0.7f, 0.7f, 0.5f, 0.6f, -0.1f, 0.6f, 0.2f, -0.7f,
0.4f, 0.7f, -0.8f, 0.6f, 0.9f, 0.8f, 0.7f, 0.8f, 0.6f, 0.6f, 
0.5f };
float CFh[] = {0.7f, 0.6f, 0.0f, 0.6f, 0.7f, 0.6f, 0.9f, 
0.8f};
float CFc[] = {0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 
0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f
, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 
0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f, 0.0f};
float CFc1, CFc2, CFc3, CFc4, CFc5, CFc6, CFc7, CFc8, CFc9, 
CFc10,
CFc11, CFc12, CFc13, CFc14, CFc15, CFc16, CFc17, CFc18, 
CFc19, CFc20,
CFc21, CFc22, CFc23, CFc24, CFc25, CFc26, CFc27;
if (chkGejala1.isChecked()) {
CFc[0] = CFh[0] * CFe[0];
}
if (chkGejala2.isChecked()) {
CFc[1] = CFh[0] * CFe[1];
}
if (chkGejala3.isChecked()) {
CFc[2] = CFh[0] * CFe[2];
}
if (chkGejala4.isChecked()) {
CFc[3] = CFh[1] * CFe[3];
}
if (chkGejala5.isChecked()) {
CFc[4] = CFh[1] * CFe[4];
}
if (chkGejala6.isChecked()) {
CFc[5] = CFh[2] * CFe[5];
}
if (chkGejala7.isChecked()) {
CFc[6] = CFh[2] * CFe[6];
}
if (chkGejala8.isChecked()) {
CFc[7] = CFh[3] * CFe[7];
}
if (chkGejala9.isChecked()) {
CFc[8] = CFh[3] * CFe[8];
}
if (chkGejala10.isChecked()) {
CFc[9] = CFh[4] * CFe[9];
}
if (chkGejala11.isChecked()) {
CFc[10] = CFh[4] * CFe[10];
}
if (chkGejala12.isChecked()) {
CFc[11] = CFh[4] * CFe[11];
}
if (chkGejala13.isChecked()) {
CFc[12] = CFh[4] * CFe[12];
}
if (chkGejala14.isChecked()) {
CFc[13] = CFh[4] * CFe[13];
}
if (chkGejala15.isChecked()) {
CFc[14] = CFh[5] * CFe[14];
}
if (chkGejala16.isChecked()) {
CFc[15] = CFh[5] * CFe[15];
}
if (chkGejala17.isChecked()) {
CFc[16] = CFh[6] * CFe[16];
}
if (chkGejala18.isChecked()) {
CFc[17] = CFh[6] * CFe[17];
}
if (chkGejala19.isChecked()) {
CFc[18] = CFh[6] * CFe[18];
}
if (chkGejala20.isChecked()) {
CFc[19] = CFh[6] * CFe[19];
}
if (chkGejala21.isChecked()) {
CFc[20] = CFh[6] * CFe[20];
}
if (chkGejala22.isChecked()) {
CFc[21] = CFh[6] * CFe[21];
}
if (chkGejala23.isChecked()) {
CFc[22] = CFh[7] * CFe[22];
}
if (chkGejala24.isChecked()) {
CFc[23] = CFh[7] * CFe[23];
}
if (chkGejala25.isChecked()) {
CFc[24] = CFh[7] * CFe[24];
}
if (chkGejala26.isChecked()) {
CFc[25] = CFh[7] * CFe[25];
}
if (chkGejala27.isChecked()) {
CFc[26] = CFh[7] * CFe[26];
}
if (chkGejala28.isChecked()) {
CFc[27] = CFh[7] * CFe[27];
}
CFc1 = 0;
if (CFc[0] >= 0 && CFc[1] >= 0) {
CFc1 = CFc[0] + CFc[1] - CFc[0] * CFc[1];
} else if (CFc[0] < 0 && CFc[1] < 0) {
CFc1 = CFc[0] + CFc[1] + CFc[0] * CFc[1];
;
} else if (CFc[0] <= 0 || CFc[1] <= 0) {
CFc1 = (CFc[0] + CFc[1]) / (1 - Math.min(Math.abs(CFc[0]), 
Math.abs(CFc[1])));
}
CFc2 = 0;
if (CFc1 >= 0 && CFc[2] >= 0) {
CFc2 = CFc1 + CFc[2] - CFc1 * CFc[2];
} else if (CFc1 < 0 && CFc[2] < 0) {
CFc2 = CFc1 + CFc[2] + CFc1 * CFc[2];
} else if (CFc1 <= 0 || CFc[2] <= 0) {
CFc2 = (CFc1 + CFc[2]) / (1 - Math.min(Math.abs(CFc1), 
Math.abs(CFc[2])));
}
CFc3 = 0;
if (CFc2 >= 0 && CFc[3] >= 0) {
CFc3 = CFc2 + CFc[3] - CFc2 * CFc[3];
} else if (CFc2 < 0 && CFc[3] < 0) {
CFc3 = CFc2 + CFc[3] + CFc2 * CFc[3];
} else if (CFc2 <= 0 || CFc[3] <= 0) {
CFc3 = (CFc2 + CFc[3]) / (1 - Math.min(Math.abs(CFc2), 
Math.abs(CFc[3])));
}
CFc4 = 0;
if (CFc3 >= 0 && CFc[4] >= 0) {
CFc4 = CFc3 + CFc[4] - CFc3 * CFc[4];
} else if (CFc3 < 0 && CFc[4] < 0) {
CFc4 = CFc3 + CFc[4] + CFc3 * CFc[4];
} else if (CFc3 <= 0 || CFc[4] <= 0) {
CFc4 = (CFc3 + CFc[4]) / (1 - Math.min(Math.abs(CFc3), 
Math.abs(CFc[4])));
}
CFc5 = 0;
if (CFc4 >= 0 && CFc[5] >= 0) {
CFc5 = CFc4 + CFc[5] - CFc4 * CFc[5];
} else if (CFc4 < 0 && CFc[5] < 0) {
CFc5 = CFc4 + CFc[5] + CFc4 * CFc[5];
} else if (CFc4 <= 0 || CFc[5] <= 0) {
CFc5 = (CFc4 + CFc[5]) / (1 - Math.min(Math.abs(CFc4), 
Math.abs(CFc[5])));
}
CFc6 = 0;
if (CFc5 >= 0 && CFc[6] >= 0) {
CFc6 = CFc5 + CFc[6] - CFc5 * CFc[6];
} else if (CFc5 < 0 && CFc[6] < 0) {
CFc6 = CFc5 + CFc[6] + CFc5 * CFc[6];
} else if (CFc5 <= 0 || CFc[6] <= 0) {
CFc6 = (CFc5 + CFc[6]) / (1 - Math.min(Math.abs(CFc5), 
Math.abs(CFc[6])));
}
CFc7 = 0;
if (CFc6 >= 0 && CFc[7] >= 0) {
CFc7 = CFc6 + CFc[7] - CFc6 * CFc[7];
} else if (CFc6 < 0 && CFc[7] < 0) {
CFc7 = CFc6 + CFc[7] + CFc6 * CFc[7];
} else if (CFc6 <= 0 || CFc[7] <= 0) {
CFc7 = (CFc6 + CFc[7]) / (1 - Math.min(Math.abs(CFc6), 
Math.abs(CFc[7])));
}
CFc8 = 0;
if (CFc7 >= 0 && CFc[8] >= 0) {
CFc8 = CFc7 + CFc[8] - CFc7 * CFc[8];
} else if (CFc7 < 0 && CFc[8] < 0) {
CFc8 = CFc7 + CFc[8] + CFc7 * CFc[8];
} else if (CFc7 <= 0 || CFc[8] <= 0) {
CFc8 = (CFc7 + CFc[8]) / (1 - Math.min(Math.abs(CFc7), 
Math.abs(CFc[8])));
}
CFc9 = 0;
if (CFc8 >= 0 && CFc[9] >= 0) {
CFc9 = CFc8 + CFc[9] - CFc8 * CFc[9];
} else if (CFc8 < 0 && CFc[9] < 0) {
CFc9 = CFc8 + CFc[9] + CFc8 * CFc[9];
} else if (CFc8 <= 0 || CFc[9] <= 0) {
CFc9 = (CFc8 + CFc[9]) / (1 - Math.min(Math.abs(CFc8), 
Math.abs(CFc[9])));
}
CFc10 = 0;
if (CFc9 >= 0 && CFc[10] >= 0) {
CFc10 = CFc9 + CFc[10] - CFc9 * CFc[10];
} else if (CFc9 < 0 && CFc[10] < 0) {
CFc10 = CFc9 + CFc[10] + CFc9 * CFc[10];
} else if (CFc9 <= 0 || CFc[10] <= 0) {
CFc10 = (CFc9 + CFc[10]) / (1 - Math.min(Math.abs(CFc9), 
Math.abs(CFc[10])));
}
CFc11 = 0;
if (CFc10 >= 0 && CFc[11] >= 0) {
CFc11 = CFc10 + CFc[11] - CFc10 * CFc[11];
} else if (CFc10 < 0 && CFc[11] < 0) {
CFc11 = CFc10 + CFc[11] + CFc10 * CFc[11];
} else if (CFc10 <= 0 || CFc[11] <= 0) {
CFc11 = (CFc10 + CFc[11]) / (1 - Math.min(Math.abs(CFc10), 
Math.abs(CFc[11])));
}
CFc12 = 0;
if (CFc11 >= 0 && CFc[12] >= 0) {
CFc12 = CFc11 + CFc[12] - CFc11 * CFc[12];
} else if (CFc11 < 0 && CFc[12] < 0) {
CFc12 = CFc11 + CFc[12] + CFc11 * CFc[12];
} else if (CFc11 <= 0 || CFc[12] <= 0) {
CFc12 = (CFc11 + CFc[12]) / (1 - Math.min(Math.abs(CFc11), 
Math.abs(CFc[12])));
}
CFc13 = 0;
if (CFc12 >= 0 && CFc[13] >= 0) {
CFc13 = CFc12 + CFc[13] - CFc12 * CFc[13];
} else if (CFc12 < 0 && CFc[13] < 0) {
CFc13 = CFc12 + CFc[13] + CFc12 * CFc[13];
} else if (CFc12 <= 0 || CFc[13] <= 0) {
CFc13 = (CFc12 + CFc[13]) / (1 - Math.min(Math.abs(CFc12), 
Math.abs(CFc[13])));
}
CFc14 = 0;
if (CFc13 >= 0 && CFc[14] >= 0) {
CFc14 = CFc13 + CFc[14] - CFc13 * CFc[14];
} else if (CFc13 < 0 && CFc[14] < 0) {
CFc14 = CFc13 + CFc[14] + CFc13 * CFc[14];
} else if (CFc13 <= 0 || CFc[14] <= 0) {
CFc14 = (CFc13 + CFc[14]) / (1 - Math.min(Math.abs(CFc13), 
Math.abs(CFc[14])));
}
CFc15 = 0;
if (CFc14 >= 0 && CFc[15] >= 0) {
CFc15 = CFc14 + CFc[15] - CFc14 * CFc[15];
} else if (CFc14 < 0 && CFc[15] < 0) {
CFc15 = CFc14 + CFc[15] + CFc14 * CFc[15];
} else if (CFc14 <= 0 || CFc[15] <= 0) {
CFc15 = (CFc14 + CFc[15]) / (1 - Math.min(Math.abs(CFc14), 
Math.abs(CFc[15])));
}
CFc16 = 0;
if (CFc15 >= 0 && CFc[16] >= 0) {
CFc16 = CFc15 + CFc[16] - CFc15 * CFc[16];
} else if (CFc15 < 0 && CFc[16] < 0) {
CFc16 = CFc15 + CFc[16] + CFc15 * CFc[16];
} else if (CFc15 <= 0 || CFc[16] <= 0) {
CFc16 = (CFc15 + CFc[16]) / (1 - Math.min(Math.abs(CFc15), 
Math.abs(CFc[16])));
}
CFc17 = 0;
if (CFc16 >= 0 && CFc[17] >= 0) {
CFc17 = CFc16 + CFc[17] - CFc16 * CFc[17];
} else if (CFc16 < 0 && CFc[17] < 0) {
CFc17 = CFc16 + CFc[17] + CFc16 * CFc[17];
} else if (CFc16 <= 0 || CFc[17] <= 0) {
CFc17 = (CFc16 + CFc[17]) / (1 - Math.min(Math.abs(CFc16), 
Math.abs(CFc[17])));
}
CFc18 = 0;
if (CFc17 >= 0 && CFc[18] >= 0) {
CFc18 = CFc17 + CFc[18] - CFc17 * CFc[18];
} else if (CFc17 < 0 && CFc[18] < 0) {
CFc18 = CFc17 + CFc[18] + CFc17 * CFc[18];
} else if (CFc17 <= 0 || CFc[18] <= 0) {
CFc18 = (CFc17 + CFc[18]) / (1 - Math.min(Math.abs(CFc17), 
Math.abs(CFc[18])));
}
CFc19 = 0;
if (CFc18 >= 0 && CFc[19] >= 0) {
CFc19 = CFc18 + CFc[19] - CFc18 * CFc[19];
} else if (CFc18 < 0 && CFc[19] < 0) {
CFc19 = CFc18 + CFc[19] + CFc18 * CFc[19];
} else if (CFc18 <= 0 || CFc[19] <= 0) {
CFc19 = (CFc18 + CFc[19]) / (1 - Math.min(Math.abs(CFc18), 
Math.abs(CFc[19])));
}
CFc20 = 0;
if (CFc19 >= 0 && CFc[20] >= 0) {
CFc20 = CFc19 + CFc[20] - CFc19 * CFc[20];
} else if (CFc19 < 0 && CFc[20] < 0) {
CFc20 = CFc19 + CFc[20] + CFc19 * CFc[20];
} else if (CFc19 <= 0 || CFc[20] <= 0) {
CFc20 = (CFc19 + CFc[20]) / (1 - Math.min(Math.abs(CFc19), 
Math.abs(CFc[20])));
}
CFc21 = 0;
if (CFc20 >= 0 && CFc[21] >= 0) {
CFc21 = CFc20 + CFc[21] - CFc20 * CFc[21];
} else if (CFc20 < 0 && CFc[21] < 0) {
CFc21 = CFc20 + CFc[21] + CFc20 * CFc[21];
} else if (CFc20 <= 0 || CFc[21] <= 0) {
CFc21 = (CFc20 + CFc[21]) / (1 - Math.min(Math.abs(CFc20), 
Math.abs(CFc[21])));
}
CFc22 = 0;
if (CFc21 >= 0 && CFc[22] >= 0) {
CFc22 = CFc21 + CFc[22] - CFc21 * CFc[22];
} else if (CFc21 < 0 && CFc[22] < 0) {
CFc22 = CFc21 + CFc[22] + CFc21 * CFc[22];
} else if (CFc21 <= 0 || CFc[22] <= 0) {
CFc22 = (CFc21 + CFc[22]) / (1 - Math.min(Math.abs(CFc21), 
Math.abs(CFc[22])));
}
CFc23 = 0;
if (CFc22 >= 0 && CFc[23] >= 0) {
CFc23 = CFc22 + CFc[23] - CFc22 * CFc[23];
} else if (CFc22 < 0 && CFc[23] < 0) {
CFc23 = CFc22 + CFc[23] + CFc22 * CFc[23];
} else if (CFc22 <= 0 || CFc[23] <= 0) {
CFc23 = (CFc22 + CFc[23]) / (1 - Math.min(Math.abs(CFc22), 
Math.abs(CFc[23])));
}
CFc24 = 0;
if (CFc23 >= 0 && CFc[24] >= 0) {
CFc24 = CFc23 + CFc[24] - CFc23 * CFc[24];
} else if (CFc23 < 0 && CFc[24] < 0) {
CFc24 = CFc23 + CFc[24] + CFc23 * CFc[24];
} else if (CFc23 <= 0 || CFc[24] <= 0) {
CFc24 = (CFc23 + CFc[24]) / (1 - Math.min(Math.abs(CFc23), 
Math.abs(CFc[24])));
}
CFc25 = 0;
if (CFc24 >= 0 && CFc[25] >= 0) {
CFc25 = CFc24 + CFc[25] - CFc24 * CFc[25];
} else if (CFc24 < 0 && CFc[25] < 0) {
CFc25 = CFc24 + CFc[25] + CFc24 * CFc[25];
} else if (CFc24 <= 0 || CFc[25] <= 0) {
CFc25 = (CFc24 + CFc[25]) / (1 - Math.min(Math.abs(CFc24), 
Math.abs(CFc[25])));
}
CFc26 = 0;
if (CFc25 >= 0 && CFc[26] >= 0) {
CFc26 = CFc25 + CFc[26] - CFc25 * CFc[26];
} else if (CFc25 < 0 && CFc[26] < 0) {
CFc26 = CFc25 + CFc[26] + CFc25 * CFc[26];
} else if (CFc25 <= 0 || CFc[26] <= 0) {
CFc26 = (CFc25 + CFc[26]) / (1 - Math.min(Math.abs(CFc25), 
Math.abs(CFc[26])));
}
CFc27 = 0;
if (CFc26 >= 0 && CFc[27] >= 0) {
CFc27 = CFc26 + CFc[27] - CFc26 * CFc[27];
} else if (CFc26 < 0 && CFc[27] < 0) {
CFc27 = CFc26 + CFc[27] + CFc26 * CFc[27];
} else if (CFc26 <= 0 || CFc[27] <= 0) {
CFc27 = (CFc26 + CFc[27]) / (1 - Math.min(Math.abs(CFc26), 
Math.abs(CFc[27])));
}


String A = Float.toString(CFc27 * 100);
String diagnosis = "";
String Saran = "";
if (CFc27 <= 0.9562239f) {
diagnosis = "HIPERTENSI TANPA RESIKO PREEKLAMPSIA";
Saran = "Tekanan darah cukup tinggi sehingga perlu 
diturunkan dan segera melakukan pemeriksaan kandungan secara berkala";
} else if (CFc27 > 0.9562239f) {
diagnosis = "PREEKLAMPSIA";
Saran = "Berdasarkan diagnosis yang didapat maka sebaiknya 
dilakukan pemeriksaan Urine di rumah sakit terdekat";
}
tvOutput.setText("Kemungkinan : " + A + "%" + "\nDiagnosis : 
" + diagnosis + "\n\nSaran : " + Saran);
btnReset.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
if (v.getId() == R.id.button2) {
chkGejala1.setChecked(false);chkGejala2.setChecked(false);ch
kGejala3.setChecked(false);chkGejala4.setChecked(false);
chkGejala5.setChecked(false);chkGejala6.setChecked(false);ch
kGejala7.setChecked(false);chkGejala8.setChecked(false);
chkGejala9.setChecked(false);chkGejala10.setChecked(false);c
hkGejala11.setChecked(false);chkGejala12.setChecked(false);
chkGejala13.setChecked(false);chkGejala14.setChecked(false);
chkGejala15.setChecked(false);chkGejala16.setChecked(false);
chkGejala17.setChecked(false);chkGejala18.setChecked(false);
chkGejala19.setChecked(false);chkGejala20.setChecked(false);
chkGejala21.setChecked(false);chkGejala22.setChecked(false);
chkGejala23.setChecked(false);chkGejala24.setChecked(false);
chkGejala25.setChecked(false);chkGejala26.setChecked(false);
chkGejala27.setChecked(false);chkGejala28.setChecked(false);
tvOutput.setText("");
}
}
});}}
