# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrograman
<br> Nama	      	: Angga Gustian
<br>NIM		        :	1227050022
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
No.1 Adalah tugas dasprog buat bagaimana kita untuk mencari nilai menggunakan array 2 dimensi dngan dibalikannya yg semulanya nilai baris dibalik menjadi dikolom dan nilai kolom mejadi dibaris.

No.2 Adalah tugas dasprog untuk mencari nilai deret bilangan yang tidak habis di bagi 3,5,7 menggunakan array 2 dimensi.
## Source Code

No.1
#include <iostream>
#include <conio.h>
using namespace std;

int main()
{
	int b,k;
    cout << "masukkan banyak baris : ";cin >> b;
    cout << "masukkan banyak kolom : ";cin >> k;
    const int baris_R = b;
    const int kolom_R = k;
    int array[baris_R][kolom_R];
    int tuker[kolom_R][baris_R];
    cout << "masukkan nilai : " << endl;
    for(int i = 0; i < baris_R; i++){
        for(int j = 0; j < kolom_R; j++){
            cout << "baris ke-" << i+1 << " kolom ke-" << j+1 << " : ";
            cin >> array[i][j]; 
        }
    }
    cout << "bentuk awal : " << endl;
    for(int i = 0; i < baris_R; i++){
        for(int j = 0; j < kolom_R; j++){
            cout << array[i][j] << " ";
        }
        cout << endl;
    }
    for(int i = 0; i < baris_R; i++){
        for(int j = 0; j < kolom_R; j++){
            tuker[j][i] = array[i][j];
        }
    }
    cout << "bentuk akhir : " << endl;
    for(int i = 0; i < kolom_R; i++){
        for(int j = 0; j < baris_R; j++){
            cout << tuker[i][j] << " ";
        }
        cout << endl;
    }
  
  No.2
#include <iostream>
#include <conio.h>
using namespace std;

int main()
{

    int array[3][3], baris, kolom;
    cout << "masukkan jumlah baris : ";cin >> baris;
    cout << "masukkan jumlah kolom : ";cin >> kolom;
    cout << "masukkan nilai : " << endl;
    for(int i = 0; i < baris ;i++){
        for(int j = 0; j < kolom ;j++){
            cout << "masukkan nilai baris ke-" << i+1 << " kolom ke-" << j+1 << " : ";
            cin >> array[i][j];
        }
    }
    cout << "nilai awal :" << endl;
    for(int i = 0; i < baris ;i++){
        for(int j = 0; j < kolom ;j++){
            cout << array[i][j] << " ";
        }
        cout << endl;
    }
    cout << "nilai akhir :" << endl;
    for(int i = 0; i < baris ;i++){
            for(int j = 0; j < kolom ;j++){
                if(array[i][j]%3 != 0 && array[i][j]%5 != 0 && array[i][j]%7 != 0){
                    cout << array[i][j] << " ";
                }
                else{
                }
            }
    }
    getch();
    return 0;
}
     
    getch();         
    return 0;
}

## Output

No.1
masukkan banyak baris : 3
masukkan banyak kolom : 2
masukkan nilai :
baris ke-1 kolom ke-1 : 1
baris ke-1 kolom ke-2 : 2
baris ke-2 kolom ke-1 : 3
baris ke-2 kolom ke-2 : 4
baris ke-3 kolom ke-1 : 5
baris ke-3 kolom ke-2 : 6
bentuk awal :
1 2
3 4
5 6
bentuk akhir :
1 3 5
2 4 6
  
  
  
No.2  
masukkan jumlah baris : 3
masukkan jumlah kolom : 2
masukkan nilai :
masukkan nilai baris ke-1 kolom ke-1 : 2
masukkan nilai baris ke-1 kolom ke-2 : 4
masukkan nilai baris ke-2 kolom ke-1 : 7
masukkan nilai baris ke-2 kolom ke-2 : 8
masukkan nilai baris ke-3 kolom ke-1 : 9
masukkan nilai baris ke-3 kolom ke-2 : 12
nilai awal :
2 4
7 8
9 12
nilai akhir :
2 4 8
