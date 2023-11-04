# Tugas-Java membuat perulangan hingga 100, membuat program bebas dengan menerapkan if else dalam perulangan while, membuat program zodiak, membuat sebuah variabel dengan tipe data array dan menampilkan semua nilai menggunakan perulangan for
# 1. perulangan nama hingga 100 dengan output 1-9 dan setelah angka 10 maka otomatis akan membuat perulangan nama sampai 91 kali
    public class ayu{

kode program Java  harus berada di suatu kelas, yang namanya sesuai dengan nama file Java tempat kode tersebut disimpan.

    public static void main(String[] args) {

Ini adalah deklarasi metode utama, yang merupakan titik masuk utama program Java. Metode ini menerima argumen dalam bentuk array argumen string

    String name = "Ayu Dewanti Suci";
        
    String NPM = "G1A023057";
Baris ini mendefinisikan variabel string name dan string NPM menginisiasinya dengan nama dan NPM kita.

    System.out.println("Nama : " + name);

    System.out.println("NPM :" + NPM);

Dengan kode ini program akan mencetak nama dan NPM kita ke layar dengan bantuan 

    System.out.println("=================");

Kode Ini akan mencetak garis pemisah berupa garis miring di sisi kanan untuk memisahkan informasi sebelumnya dengan hasil cetakan selanjutnya.

    for (int i = 0 ; i<=100 ; i++){

            if (i>= 10 ){
                
                System.out.println(name);
            
            }
            
            else {
               
                System.out.println(i);
           
            }
       
        }
    
    }
    
}

Selanjutnya, ada sebuah loop for yang akan berjalan dari i = 0 hingga i = 100, dengan i bertambah 1 pada setiap iterasi.

Di dalam loop, terdapat pernyataan if yang digunakan untuk menentukan apakah harus mencetak nama atau nilai i.

Jika i lebih besar atau sama dengan 10, maka pernyataan System.out.println(name); akan mencetak nama, yaitu "Ayu Dewanti Suci".

Jika i kurang dari 10, maka pernyataan System.out.println(i); akan mencetak nilai i.

Hasilnya, program  akan mencetak nama, NPM, dan rangkaian angka dari 0 hingga 100, dan nama akan dicetak  dari 10 hingga 100.

# 2. membuat program dengan menerapkan if else dalam perulangan while
    public class no2 {

 Ini adalah deklarasi kelas dengan nama 

    public static void main(String[] args) {

Ini adalah deklarasi metode utama, yang merupakan titik masuk utama program Java. menerima satu parameter, yaitu array string args

    String nama = "Ayu Dewanti Suci";
    String npm = "G1A023057";

Kode Ini adalah deklarasi variabel string nama dan string npm

    int counter = 0;

Ini adalah deklarasi variabel bilangan bulat counter yang diinisialisasi ke nilai 0. Variabel counter digunakan untuk mengontrol loop.

    while (counter < 2) {

kode Ini adalah pernyataan while yang akan menjalankan blok kode yang ada selama nilai counter kurang dari 2. Dalam hal ini, ini akan dijalankan dua kali.

    if (counter == 0) {
                System.out.println("Nama: " + nama);
            } else {
                System.out.println("NPM: " + npm);
            }
            counter++;
        }
    }
}

Di dalam loop while, terdapat pernyataan if yang digunakan untuk memeriksa nilai counter. Jika counter sama dengan 0, maka akan mencetak nama Anda: System.out.println("Nama: " + nama);.

Jika counter tidak sama dengan 0 (yaitu 1), maka akan mencetak NPM Anda: System.out.println("NPM: " + npm);.

counter++;: Pernyataan ini digunakan untuk meningkatkan nilai counter setiap kali iterasi loop selesai. Ini bertujuan untuk mengontrol berapa kali pernyataan if dijalankan.

Hasilnya, program ini  mencetak nama dan NPM dua kali. Pertama nama, lalu NPM. Ini karena variabel counter awalnya 0 dan kemudian 1.

    Nama: Ayu Dewanti Suci
    NPM: G1A023057


# 3. program zodiak
    public class ayu3 {

Ini adalah deklarasi kelas dengan nama ayu3

    public static void main(String[] args) {

 Ini adalah deklarasi metode main, yang merupakan titik masuk program Java. Metode ini mengambil argumen dalam bentuk array string args.

    Scanner input = new Scanner(System.in);

Dalam metode main, sebuah objek Scanner dengan nama input dibuat untuk membaca input dari pengguna.

    int tanggal, bulan;

Dua variabel bertipe integer tanggal dan bulan dideklarasikan untuk menyimpan tanggal dan bulan yang dimasukkan

    System.out.print("Masukkan tanggal lahir (1-31): ");
    tanggal = input.nextInt();

    System.out.print("Masukkan bulan lahir (1-12): ");
    bulan = input.nextInt();

    String zodiak = tentukanZodiak(tanggal, bulan);
    System.out.println("Zodiak Anda adalah: " + zodiak);

Dengan kode ini Program mencetak pesan "Masukkan tanggal lahir (1-31): " dan  "Masukkan bulan lahir (1-12): " dan kemudian mengambil input bulan dari pengguna dengan input.nextInt(). Selanjutnya, program memanggil metode tentukanZodiak(tanggal, bulan) dengan tanggal dan bulan yang dimasukkan oleh pengguna. Hasil dari metode ini (nama zodiak) disimpan dalam variabel zodiak.

Program mencetak hasil dengan menggabungkan nama zodiak ke dalam pesan "Zodiak Anda adalah: ".

    input.close();
    }

Terakhir, objek Scanner ditutup dengan menggunakan input.close() untuk menghindari kebocoran sumber daya.

    public static String tentukanZodiak(int tanggal, int bulan) {

Di luar metode main, ada metode tentukanZodiak(int tanggal, int bulan) yang menerima tanggal dan bulan sebagai argumen. Metode ini digunakan untuk menentukan zodiak berdasarkan tanggal lahir yang dimasukkan.

    if ((bulan == 3 && tanggal >= 21) || (bulan == 4 && tanggal <= 19)) {
            return "Aries";
        } else if ((bulan == 4 && tanggal >= 20) || (bulan == 5 && tanggal <= 20)) {
            return "Taurus";
        } else if ((bulan == 5 && tanggal >= 21) || (bulan == 6 && tanggal <= 20)) {
            return "Gemini";
        } else if ((bulan == 6 && tanggal >= 21) || (bulan == 7 && tanggal <= 22)) {
            return "Cancer";
        } else if ((bulan == 7 && tanggal >= 23) || (bulan == 8 && tanggal <= 22)) {
            return "Leo";
        } else if ((bulan == 8 && tanggal >= 23) || (bulan == 9 && tanggal <= 22)) {
            return "Virgo";
        } else if ((bulan == 9 && tanggal >= 23) || (bulan == 10 && tanggal <= 22)) {
            return "Libra";
        } else if ((bulan == 10 && tanggal >= 23) || (bulan == 11 && tanggal <= 21)) {
            return "Scorpio";
        } else if ((bulan == 11 && tanggal >= 22) || (bulan == 12 && tanggal <= 21)) {
            return "Sagittarius";
        } else if ((bulan == 12 && tanggal >= 22) || (bulan == 1 && tanggal <= 19)) {
            return "Capricorn";
        } else if ((bulan == 1 && tanggal >= 20) || (bulan == 2 && tanggal <= 18)) {
            return "Aquarius";
        } else {
            return "Pisces";
        }
    }
}

kode tersebut adalah tanggal dan bulan lahir yang dimasukkan untuk menentukan zodiak. Metode ini menggunakan sejumlah pernyataan if dan else if untuk memeriksa tanggal dan bulan yang dimasukkan dan menentukan zodiak yang sesuai.

Setiap if dan else if memeriksa tanggal dan bulan untuk rentang tertentu yang sesuai dengan satu zodiak. Metode ini mengembalikan nama zodiak yang sesuai sebagai string.

Hasilnya adalah program yang memungkinkan pengguna memasukkan tanggal dan bulan lahir, dan kemudian mencetak nama zodiak yang sesuai dengan data tersebut.

# 4. variabel dengan tipe data array dan menampilkan semua nilai menggunakan perulangan for
    public class no4 {

  Ini adalah deklarasi kelas dengan nama no4.

    public static void main(String[] args) {

  Ini adalah deklarasi metode main, yang merupakan titik masuk program Java. Metode ini mengambil argumen dalam bentuk array string args

    // Membuat sebuah array dengan tipe data integer
        int[] numbers = {14, 5, 20, 5};

  Dalam metode main, sebuah array integer numbers dibuat. Array ini mengandung empat nilai integer: 14, 5, 20, dan 5.

    // Menggunakan perulangan for untuk menampilkan nilai dalam array
        for (int i = 0; i < numbers.length; i++) {
            System.out.println("Nilai indeks ke-" + i + ": " + numbers[i]);
        }
    }
}

Selanjutnya, program menggunakan perulangan for untuk mengakses setiap elemen dalam array numbers dan mencetaknya ke layar. int i = 0; adalah inisialisasi variabel i yang digunakan sebagai indeks array. Dimulai dari 0, dan akan meningkat setiap kali iterasi berikutnya.

i < numbers.length adalah kondisi untuk perulangan for. Perulangan akan terus berjalan selama indeks i kurang dari panjang array numbers.

System.out.println("Nilai indeks ke-" + i + ": " + numbers[i]); mencetak nilai yang berada di indeks i beserta indeksnya ke layar. Misalnya, pada iterasi pertama, ini akan mencetak "Nilai indeks ke-0: 14".

Perulangan for akan berjalan empat kali (sesuai dengan panjang array numbers), dan setiap nilai dalam array akan dicetak dengan pesan yang mencakup indeksnya. Hasilnya adalah program ini akan mencetak setiap nilai dalam array numbers beserta indeksnya ke layar, sehingga akan terlihat output seperti ini:

    Nilai indeks ke-0: 14
    Nilai indeks ke-1: 5
    Nilai indeks ke-2: 20
    Nilai indeks ke-3: 5
