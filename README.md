# menggunakan-properti-dinamis-di-CI3

Fungsi dari #[\AllowDynamicProperties] di CI3 adalah untuk mengizinkan penggunaan properti dinamis di kelas tersebut. Properti dinamis adalah properti yang tidak dideklarasikan secara eksplisit di kelas, tetapi dapat ditetapkan secara dinamis menggunakan operator `->`.

Pada PHP versi 8.2, penggunaan properti dinamis di kelas yang tidak menggunakan atribut `#[\AllowDynamicProperties]` akan menghasilkan peringatan (warning). Peringatan ini akan diubah menjadi kesalahan (error) pada PHP versi 9.

Untuk mengatasi peringatan ini, kita dapat menambahkan atribut `#[\AllowDynamicProperties]` di kelas yang menggunakan properti dinamis. Atribut ini akan mengizinkan penggunaan properti dinamis di kelas tersebut tanpa menghasilkan peringatan.

Berikut adalah contoh penggunaan atribut `#[\AllowDynamicProperties]`:

```php
class MyClass
{
    #[AllowDynamicProperties]
    public $name;

    public function __construct()
    {
        $this->name = 'John Doe';
    }
}

$myClass = new MyClass();
$myClass->name = 'Jane Doe';

echo $myClass->name; // Jane Doe
```

Pada contoh di atas, kelas `MyClass` menggunakan atribut `#[\AllowDynamicProperties]` untuk mengizinkan penggunaan properti dinamis `name`. Properti `name` kemudian dapat ditetapkan secara dinamis menggunakan operator `->`.

Berikut adalah beberapa hal yang perlu diperhatikan saat menggunakan atribut `#[\AllowDynamicProperties]`:

* Atribut ini hanya berlaku untuk kelas yang menggunakan properti dinamis.
* Atribut ini tidak boleh digunakan di kelas yang menggunakan properti statis.
* Atribut ini tidak boleh digunakan di kelas yang menggunakan properti protected atau private.

Demikian penjelasan tentang fungsi dari #[\AllowDynamicProperties] di CI3.



Untuk lebih simpelnya silahkan ganti folder system pada CI3 anda dengan Folder yang telah saya sediakan.
