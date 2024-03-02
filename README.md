# 2.-TUGAS-PBO

**1. sebutkan apa yang dimaksud dengan class dan object**
1. **Class**: Di JavaScript, class adalah sintaks baru yang di perkenalkan dalam ECMAScript 2015 (ES6) yang memungkinkan kita untuk mendefinisikan sebuah class. Class adalah cetak biru atau blueprint untuk membuat objek. Ini mendefinisikan atribut (variabel) dan metode (fungsi) yang akan dimiliki oleh objek yang dibuat dari class tersebut. Contoh sederhana class adalah sebagai berikut:

    ```javascript
    class Manusia {
        constructor(nama, umur) {
            this.nama = nama;
            this.umur = umur;
        }

        sapa() {
            console.log(`Halo, nama saya ${this.nama} dan saya berusia ${this.umur} tahun.`);
        }
    }
    ```

    Di sini, `Manusia` adalah sebuah class yang memiliki dua atribut (`nama` dan `umur`) dan satu metode (`sapa`).

2. **Objek**: Objek adalah instansi dari sebuah class. Ketika sebuah class diinstansiasi, objek baru dibuat dari class tersebut. Objek memiliki atribut dan metode yang sama dengan class yang digunakan untuk membuatnya. Contoh penggunaan class `Manusia` di atas:

    ```javascript
    let manusia1 = new Manusia("John", 30);
    manusia1.sapa();  // Output: Halo, nama saya John dan saya berusia 30 tahun.
    ```

    Di sini, `manusia1` adalah objek yang dibuat dari class `Manusia`. Objek ini memiliki atribut `nama` dengan nilai "John" dan atribut `umur` dengan nilai 30. Objek juga memiliki metode `sapa`, yang ketika dipanggil akan mencetak pesan sapaan sesuai dengan nilai atribut yang dimiliki objek.

Dengan menggunakan class dan objek, kita dapat membuat kode yang lebih terstruktur dan mudah dimengerti, serta memungkinkan untuk mengelompokkan data dan fungsi yang berhubungan bersama-sama.

**2. sebutkan dan jelaskan jenis jenis method**


1. **Constructor Method**: Constructor method adalah metode khusus yang dipanggil saat sebuah objek dari class dibuat. Ini biasanya digunakan untuk menginisialisasi objek dengan nilai awal. Constructor method memiliki nama yang khusus, yaitu `constructor`. Contoh:

    ```javascript
    class Manusia {
        constructor(nama, umur) {
            this.nama = nama;
            this.umur = umur;
        }
    }
    ```

2. **Instance Method**: Instance method adalah metode yang terikat pada objek individu yang dibuat dari class. Metode ini dapat diakses melalui objek tersebut. Contoh:

    ```javascript
    class Manusia {
        constructor(nama, umur) {
            this.nama = nama;
            this.umur = umur;
        }

        sapa() {
            console.log(`Halo, nama saya ${this.nama} dan saya berusia ${this.umur} tahun.`);
        }
    }

    let manusia1 = new Manusia("John", 30);
    manusia1.sapa();  // Output: Halo, nama saya John dan saya berusia 30 tahun.
    ```

3. **Static Method**: Static method adalah metode yang terikat pada class itu sendiri, bukan pada objek individu yang dibuat dari class. Metode ini dapat diakses langsung melalui class tanpa membuat objek. Contoh:

    ```javascript
    class Manusia {
        constructor(nama, umur) {
            this.nama = nama;
            this.umur = umur;
        }

        static jumlahManusia() {
            console.log("Ada beberapa manusia di dunia ini.");
        }
    }

    Manusia.jumlahManusia();  // Output: Ada beberapa manusia di dunia ini.
    ```

4. **Getter dan Setter Method**: Getter dan setter method adalah metode yang digunakan untuk mengakses dan mengubah nilai dari properti objek. Getter digunakan untuk mengambil nilai properti, sedangkan setter digunakan untuk mengubah nilai properti. Contoh:

    ```javascript
    class Manusia {
        constructor(nama, umur) {
            this._nama = nama;
            this._umur = umur;
        }

        get nama() {
            return this._nama;
        }

        set nama(namaBaru) {
            this._nama = namaBaru;
        }
    }

    let manusia1 = new Manusia("John", 30);
    console.log(manusia1.nama);  // Output: John

    manusia1.nama = "Jane";
    console.log(manusia1.nama);  // Output: Jane
    ```

Dengan menggunakan berbagai jenis metode ini, kita dapat membuat class yang lebih fleksibel dan dapat diakses dengan lebih mudah.

Mari kita bahas kode di atas bagian per bagian:

1. **public class Komputer {**: Ini adalah deklarasi class `Komputer`. Class ini memiliki dua atribut, yaitu `jenis_komputer` dan `merk`. `jenis_komputer` adalah atribut publik, sedangkan `merk` adalah atribut privat.

2. **String jenis_komputer;**: Ini adalah deklarasi atribut `jenis_komputer` yang bertipe data `String`. Atribut ini adalah publik, sehingga dapat diakses dari luar class.

3. **private String merk;**: Ini adalah deklarasi atribut `merk` yang bertipe data `String`. Atribut ini adalah privat, sehingga hanya dapat diakses dari dalam class.

4. **public void setDataKomputer (String jenis, String merk) { jenis_komputer = jenis; this.merk = merk; }**: Ini adalah metode `setDataKomputer` yang bertugas untuk mengatur nilai atribut `jenis_komputer` dan `merk`. Metode ini menerima dua parameter, yaitu `jenis` dan `merk`, dan mengatur nilai atribut sesuai dengan nilai yang diberikan.

5. **public String getJenis() { return jenis_komputer; }:** Ini adalah metode `getJenis` yang bertugas untuk mengembalikan nilai atribut `jenis_komputer`.

6. **public String getMerk() { return merk; }:** Ini adalah metode `getMerk` yang bertugas untuk mengembalikan nilai atribut `merk`.

7. **public static void main(String[] args) {**: Ini adalah metode `main`, yang merupakan titik masuk utama untuk program Java. Di dalam metode ini, kita membuat objek `mykom` dari class `Komputer`.

8. **Komputer mykom new Komputer();**: Ini adalah deklarasi dan inisialisasi objek `mykom` dari class `Komputer`.

9. **mykom.setDatakomputer("LAPTOP", "MACBOOK");**: Ini adalah pemanggilan metode `setDatakomputer` pada objek `mykom` untuk mengatur nilai atribut `jenis_komputer` dan `merk`.

10. **System.out.printin(mykom.getuenis());**: Ini adalah pemanggilan metode `getJenis` pada objek `mykom` untuk mendapatkan nilai atribut `jenis_komputer`. Namun, ada kesalahan penulisan, seharusnya `getJenis` bukan `getuenis`.

11. **System.out.println(mykom.getMerk());**: Ini adalah pemanggilan metode `getMerk` pada objek `mykom` untuk mendapatkan nilai atribut `merk`.

Jadi, kode di atas adalah contoh sederhana dari class `Komputer` yang memiliki dua atribut dan beberapa metode untuk mengatur dan mendapatkan nilai atribut tersebut.




**3. Berdasarkan gambar berikut ini, jelaskan masing masing bagian sesuai nomer urut yang ada**

Ada beberapa kesalahan dalam kode yang diberikan. Berikut adalah koreksi yang diperlukan:

1. **Penulisan Class**: Penulisan class harus diawali dengan huruf kapital. Jadi, `public class Komputer` harus diganti menjadi `public class Komputer`.

2. **Penulisan Objek**: Penulisan objek harus menggunakan operator `new`. Jadi, `Komputer mykom new Komputer();` harus diganti menjadi `Komputer mykom = new Komputer();`.

3. **Penulisan Method**: Penulisan method `setDataKomputer` harus menggunakan huruf kapital yang benar. Jadi, `setDatakomputer` harus diganti menjadi `setDataKomputer`.

4. **Penulisan Method**: Penulisan method `getJenis` dan `getMerk` harus menggunakan huruf kapital yang benar. Jadi, `getJenis` dan `getMerk` harus diganti menjadi `getJenis` dan `getMerk`.

5. **Penulisan Method**: Penulisan method `System.out.printin` harus diganti menjadi `System.out.println`.

Setelah koreksi, kode yang benar adalah sebagai berikut:

```java
public class Komputer {
    String jenis_komputer;
    private String merk;

    public void setDataKomputer(String jenis, String merk) {
        jenis_komputer = jenis;
        this.merk = merk;
    }

    public String getJenis() {
        return jenis_komputer;
    }

    public String getMerk() {
        return merk;
    }

    public static void main(String[] args) {
        Komputer mykom = new Komputer();
        mykom.setDataKomputer("LAPTOP", "MACBOOK");
        System.out.println(mykom.getJenis());
        System.out.println(mykom.getMerk());
    }
}
```

Dengan koreksi ini, kode akan berjalan dengan benar dan mencetak output yang diharapkan.




Berikut adalah koreksi dari kode yang berikan:

```java
public class Komputer {  

    String jenis_komputer;
    private String merk;

    public void setDataKomputer(String jenis, String merk) {
        jenis_komputer = jenis;
        this.merk = merk;
    }

    public String getJenis() {
        return jenis_komputer;
    }

    public String getMerk() {
        return merk;
    }

    public static void main(String[] args) {
        Komputer mykom = new Komputer();
        mykom.setDataKomputer("LAPTOP", "MACBOOK");
        System.out.println(mykom.getJenis());
        System.out.println(mykom.getMerk());
    }
}
```

Perubahan yang dilakukan:

1. Penambahan `=` setelah `Komputer mykom` pada baris 5.
2. Penambahan `()` setelah `setDataKomputer` pada baris 6.
3. Penambahan `()` setelah `getJenis` pada baris 10.
4. Penambahan `()` setelah `getMerk` pada baris 11.
5. Penambahan `;` setelah `System.out.println(mykom.getMerk())` pada baris 12.

Dengan perubahan tersebut, kode sekarang akan berjalan dengan benar dan mencetak output:

```
LAPTOP
MACBOOK
```

**4. tuliskan perbaikan pada kode program berikut ini, agar kode program tersebut dapat di compile sehingga program akan berjalan denga benar!**

Berikut adalah perbaikan pada kode program yang Anda berikan agar dapat dicompile dan berjalan dengan benar:

```java
public class HandPhone {

    String jenis_hp;
    int tahun_pembuatan;

    public void setDataHP(String jenis_hp, int tahun_pembuatan) {
        this.jenis_hp = jenis_hp;
        this.tahun_pembuatan = tahun_pembuatan;
    }

    public String getJenisHP() {
        return jenis_hp;
    }

    public int getTahunPembuatan() {
        return tahun_pembuatan;
    }

    public static void main(String args[]) {
        HandPhone hp = new HandPhone();
        hp.setDataHP("Smartphone", 2022);
        System.out.println(hp.getJenisHP());
        System.out.println(hp.getTahunPembuatan());
    }
}
```

Perubahan yang dilakukan:

1. Penambahan `()` setelah `HandPhone` pada baris 1.
2. Penambahan `()` setelah `setDataHP` pada baris 6.
3. Penambahan `()` setelah `getJenisHP` pada baris 11.
4. Penambahan `()` setelah `getTahunPembuatan` pada baris 15.
5. Penambahan `()` setelah `main` pada baris 17.
6. Penambahan `()` setelah `setDataHP` pada baris 19.
7. Penambahan `()` setelah `getJenisHP` pada baris 21.
8. Penambahan `()` setelah `getTahunPembuatan` pada baris 23.

Dengan perubahan tersebut, kode sekarang akan berjalan dengan benar dan mencetak output:

```
Smartphone
2022
```
