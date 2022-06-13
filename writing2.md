Writing Assignment Minggu kedua :
===

- Scope
- Function
- Git & Github lanjutan
- Javascript DOM & Object
- Array


1.Scope
===

*GLOBAL SCOPE*

Variabel harus dideklarasikan diluar blocks code

*LOCAL SCOPE*

Variabel hanya bisa diakses didalam blocks code 

* Contoh Global Scope 

```javascript
let x = 10;
function test() {
    console.log('nilai x : ' , x)
    x = 9
    console.log('nilai perubahan x : ',x)
}
test()
console.log('nilai global x: ' ,x)
```
* Contoh Local Scope 

```javascript
let y = '10'
function test() {
    let y =100
    console.log('nilai local y : ',y)
}
test()
console.log('nilai global y: ' ,y)
```

2.Function
===
*Function* adalah blok kode yang dirancang untuk menyelesaikan tugas tertentu dan ketika function dibutuhkan lagi , kita bisa kembali menggunakannya dengan menggunakan perintah return.

* Cara memanggil function
```javascript
greeting()
console.log(greeting());
```

* Contoh :
```javascript
function getGoodbye(){
    console.log("Never");
}
getGoodbye();
```

3.JavaScript DOM
===

Didalam JavaScript DOM kita bisa Memanipulasi element HTML dan Menangkap interaksi user.

**_Memanipulasi ELement HTML_**

a. Mencari Element HTML
dengan memperhatikan elemen HTML , misal;
* elemen id maka diubah ke DOM menjadi `document.getElementById("")`
* elemen class maka diubah ke DOM menjadi `document.getElementByClassName("")`
* elemen kombinasi query selector maka diubah ke DOM menjadi `document.querySelector("# header p span")`


b. Mengubah Konten Element
>`Element.textContent_`: digunakan hanya untuk mengubah teks didalam sebuah element
>`Element.innerHTML` : digunakan untuk menambah/mengubah konten dari HTML tersebut didalam sebuah element

c. Membuat Element HTML

- pertama misal ingin membuat heading  , langkah pertama yang harus dilakukan adalah membuat elemen yang baru dengan 
`.createElement()`
- kemudian gunakan .textContent untuk mengubah konten teks 
- jangan lupa jika setiap membuat elemen baru maka harus diikuti `.appendChild` untuk menambahkan ke DOM.


**_Menangkap Interaksi User_**

dengan menambahkan `Element.addEvenListener("event")` dan `Element.onevent`

`Element.addEvenListener("event")` : digunakan untuk EventListener

- EvenListener-Click : akan digunakan jika kita ingin menampilkan alert/popup yang berisi teks inputan dan element yang digunakan berupa id inputan dan button. 
- contoh : 
```javascript 
button.addEventListener("click",function(){
    alert(input.value)
})
```
----
**atau**
```javascript 
button.oncClick=function(){alert(input.value)}
```
----

OBJECT
===

_Cara Membuat Object_
```javascript
let namaObject = {key : 'value'}
```

_Cara Mengakses properti_
---
1.Dot Notation
```javascript
let person ={
    nama : ' Nanda "
    umur : 17,
    hobby : ' singing ' 
}

console.log(person.umur + ' ' + 'dot notation');
console.log(person.hobby);
//output 
17 dot notation
```
2.Bracket Notation
```javascript
let person ={
    nama : ' Nanda "
    umur : 17,
    hobby : ' singing ' 
}

console.log(person['umur'] + ' ' + 'bracket notation');
console.log(person.hobby);
//output 
//17 bracket notation//
//
```
_Cara Update Object_
---
mengupdate object dapat dilakukan dengan 2 cara yaitu dengan menggunakan __dot notation__ dan __bracket notation__

_Const in Object_
>Nilainya dapat diupdate tetapi tidak boleh reassign dengan nilai baru

_Nested Object_
>Objek didalam sebuah objek
_Looping Object_
mengunakan const key atau let key dengan syntax :

```javascript
for(let key in object){
};
```

_Array of Object_

    * Membuat sebuah Object

contoh 

_without properti_
```javascript
let person = {};
```
_with properti_
```javascript
let person ={
    name:'nanda',
    age:'17',
    isVerified:'true'
}
```

>Object dapat diassign kedalam sebuah variabel.
>Objek dapat menyimpan properti dengan tipe data apapun.


4.Git & Github Lanjutan
===
- Cara Git Clone atau supaya projek bisa dikerjakan bersama sama dengan menggunakan github
    * Clone Repository file yang sudah dipost di github 
    * Buka Git bash kemudian ketik git clone https:// 
    * Buka Visual Studio Code
    * Buka Terminal dengan New Terminal
    * Arahkan kedalam file dengan cd/.../...
    * Jangan lupa buat branch dengan cara git checkout - b namabranch
    * Kemudian git add . 
    * Lalu git commit -m "adding"
    * Kemudian compare and pull request
    * Klik create pull request
    * Jangan mengklik merge pull request karena yang mempunyai wewenang hanyalah yang mengupload/membuat folder

5.Array
===
- Array 

Array adalah tipe data yang dapat menyimpat tipe data apapun seperti String ,Number ,Boolean ,dsb.

contoh :

```javascript
letBuah = ["Semangka","Jambu","Manggis"];
console.log(Buah);
```
>Yang perlu diingat dalam Array adalah bahwa array dihitung dari index data ke-0.
>Ketika menggunakan const kita tidak bisa mengupdate array baru,tetapi kita dapat melakukan update konten nilai didalam array 
>Ketika menggunakan const pada array kita tidak bisa mengubah array dengan array yang baru

- Array Properties

terdapat constructor , length , index,input dan prototype.
    *length* digunakan untuk mengembalikan nilai dari jumlah panjang suatu array.

- Array Method

memudahkan penggunaan function yang bisa kita gunakan dalam javascript.

contoh :

    `.push()` : menambahkan item array pada urutan paling akhir.
```javascript
let activity = [
    'Belajar',
    'Mendesain',
    'Mendengarkan lagu'
];
activity.push('Menonton drakor');
console.log(activity);

//output//
// Belajar
// Mendesain
// Mendengarkan lagu
// Menonton drakor
```
- Looping in Array

Ketika melakukan looping pada Array ada dua cara yang dapat dilakukan yaitu menggunakan :
`.map`
`.forEach()`

- `.map ` adalah melakukan looping dengan membuat array baru sebelum perubahan ,sehingga array asli masih sama.
---
- `.forEach()` adalah method untuk melakukan looping pada setiap elemen array dengan kata lain merubah array yang asli.

>Melakukan looping lebih aman menggunakan `.map`
>Melakukan looping dengan menggunakan `.forEach()` jika hanya memerlukan looping untuk menampilkan / menyimpan ke database 
>Melakukan looping dengan menggunakan `map` jika melakukan operasi pada array .
>Membaca looping pada array :

```javascript
for (let i = 0; i <buah.length ; i++){
    console.log(buah[1])
}
```
    let i = 0 dianggap sebagai START
    i < buah.length dianggap sebagai STOP
    i ++ dianggap sebagai STEP

- Array of Object
>Menampilkan array of object menggunakan forEarch