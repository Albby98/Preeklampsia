# Program Tensimeter (IDE)

#include <SoftwareSerial.h>
#include <LiquidCrystal_I2C.h>
int pinSensor = 1;
int pinFilter = 0;
int maks = 86;
int baca = 82;
int Ts = 7;
int powerOn = 5;
int nBT1 = 0;
int SW = 0;
float SBP = 0.7;
float DBP = 0.5;
int nBT = 0;
int wt = 10;
int wp = 1000;
int nSen = 0;
int tamp = 0;
const int n = 1550;
int A[n];
int B[n];
int MAP = 0;
int wb = 1000;
float sistolik = 0.0;
float diastolik = 0.0;
float x, y, nf, ng, MAP1;
LiquidCrystal_I2C lcd = LiquidCrystal_I2C(0x27, 16, 2);
void setup () {
lcd.init();
lcd.backlight();
Serial.begin(9600);
pinMode(powerOn, INPUT_PULLUP);
}
void Button() {
nBT1 = digitalRead(powerOn);
if (nBT1 == 0) nBT1 = 1;
else nBT1 = 0;
if (nBT1 == 1 && SW == 0) {
nBT1 = 1;
SW = 1;
}
else if (nBT1 == 1 && SW == 1) nBT1 = 3;
else {
nBT1 = 0;
SW = 0;
}
}
void loop() {
Button();
Serial.println("Pasang Manset!");
lcd.setCursor(1, 0);
lcd.println("Pasang Manset!      ");
lcd.setCursor(0, 1);
lcd.println("                                ");
bacaBT();
if (nBT1 == 1) {
Serial.println("Mulai Pompa");
lcd.setCursor(0, 0);
lcd.println("  Mulai Pompa!    ");
pompa();
}
else {
delay(50);
}
hasil_akhir();
int i = 0;
while (i == 0) {
Button();
if (nBT1 == 3) {
i = 1;
}
else {
delay(50);
}
}
tutup:
delay(50);
}
void bacaBT() {
int i = 0;
while (i == 0) {
Button();
if (nBT1 == 1) {
nBT = 1;
i = 1;
}
else if (nBT1 == 3) {
nBT = 3;
i = 1;
}
else {
delay(50);
}
}
}
void pompa() {          // inti program
int i = 0;
while (i == 0) {
if (nBT == 2) {
goto selesai;
}
else if (nBT == 1) {
nSen = (analogRead(pinSensor));
tamp = tekanan(nSen);
if (nSen >= maks) {
Serial.println("Buka Katup Tensi");
lcd.setCursor(0, 0);
lcd.println("Buka Katup Tensi           ");
lcd.setCursor(0, 1);
lcd.println("Secara Perlahan!           ");
i = 1;
}
delay(wp);
}
}
selesai:
delay(wt);
}
void baca_sensor () {
int i = 0;
while (i == 0) {
nSen = (analogRead(pinSensor));
if (nSen <= baca) {
Serial.println("Hitung");
lcd.setCursor(0, 0);
lcd.println("   Mendeteksi              ");
lcd.setCursor(0, 1);
lcd.println("                           ");
for (int j = 0; j < n; j++) {
A[j] = (analogRead(pinSensor));
B[j] = analogRead(pinFilter);
Serial.println(B[j]);
delay(Ts);
}
Serial.println("  selesai");
lcd.setCursor(3, 0);
lcd.println("  Harap                  ");
lcd.setCursor(3, 1);
lcd.println(" Tunggu!                 ");
i = 1;
}
else {
delay(Ts);
}
}
}
void hasil_akhir() {
MAP = B[0];
for (int i = 1; i < n; i++) {
if (B[i] > MAP) {
MAP = B[i];
delay(10);
}
else {}
}
delay(10);
MAP1 = MAP;
for (int j = 0; j < n; j++) {
nf = B[j];
x = nf / MAP;
if (x >= SBP) {
sistolik = tekanan(A[j]);
goto sis;
}
else {
delay(10);
}
}
sis:
delay(10);
for (int k = n - 1; k >= 0; k--) {
ng = B[k];
y = ng / MAP1;
if (y >= DBP) {
diastolik = tekanan(A[k]);
goto akhir;
}
else {
delay(10);
}
}
akhir:
delay(10);
Serial.print("Sistolik :");
Serial.println(sistolik);
Serial.print(" mmHg ");
lcd.setCursor(0, 0);
lcd.print("Sis :");
lcd.println(sistolik);
lcd.setCursor(10, 0);
lcd.print(" mmHg ");
Serial.print("Daistolik : ");
Serial.println(diastolik);
Serial.print(" mmHg ");
lcd.setCursor(0, 1);
lcd.print("Dis :");
lcd.println(diastolik);
lcd.setCursor(10, 1);
lcd.print(" mmHg ");
}
float tekanan(float bvolt) {
float volt = 0;
float v_kPa = 0;
float tekanan_kPa = 0;
float tekanan_mmHg = 0;
volt = bvolt * 5 / 1024;
v_kPa = volt / 5;
tekanan_kPa = (v_kPa - 0.04) / 0.0018;
tekanan_mmHg = (tekanan_kPa * 7.500617)-20;
return tekanan_mmHg;
