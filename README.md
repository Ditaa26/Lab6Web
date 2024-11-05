# Lab6Web
# Dita Tiara Putri   
# TI 23 A1   

# Diktat Praktikum Perancangan Web 
# 1 jQuery Framework
```sh
<!DOCTYPE html>
<html>
<head>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js">
    </script>
    <script>
    $(document).ready(function(){
        $("#flip").click(function(){
            $("#panel").slideToggle("slow");
        });
    });
    </script>

    <style type="text/css">
    #panel, #flip {
        padding: 5px;
        text-align: center;
        background-color: #e5eecc;
        border: solid 1px #c3c3c3;
    }
    #panel {
        padding: 50px;
        display: none;
    }

    </style>
</head>
<body>
    <div id = "flip">Click to slide the panel down or up</div>
    <div id = "panel">Hello world!</div>
</body>
</html>
```
Kode ini membuat panel tersembunyi yang muncul dengan efek slide saat teks "Click to slide the panel down or up" diklik.   
jQuery: Menggunakan ``slideToggle("slow")`` untuk menampilkan atau menyembunyikan panel dengan efek meluncur.   
CSS: Mengatur tampilan dasar untuk tombol #flip dan panel #panel. Panel tersembunyi secara default.   

![image](https://github.com/user-attachments/assets/169285b8-5d77-4210-94de-803f8330b3e5)   
![image](https://github.com/user-attachments/assets/cbd6b58f-1b0a-43d4-8113-da09d0daf4c5)   

# 2 jQuery Effects - Animation
```sh
<!DOCTYPE html>
<html>
<head>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js">
    </script>
    <script>
    $(document).ready(function(){
        $("button").click(function(){
            var div=$("div");
            div.animate({height:'300px',opacity:'0.4'}, "slow");
            div.animate({height:'300px',opacity:'0.8'}, "slow");
            div.animate({height:'100px',opacity:'0.4'}, "slow");
            div.animate({height:'100px',opacity:'0.8'}, "slow");
        });
    });
    </script>
</head>
<body>
    <button>Start Animation</button>
    <div style="background:#98bf21;height:100px;width:100px;position:absolute;"></div>
</body>
</html>
```
Kode HTML ini menggunakan jQuery untuk membuat animasi pada elemen ``<div>`` saat tombol ditekan. Animasi mengubah tinggi dan opasitas ``<div>`` secara bertahap dalam empat tahap, menciptakan efek naik-turun pada ukuran dan transparansinya.   
![image](https://github.com/user-attachments/assets/e7e2d4ae-18d9-4d2d-af24-37195476b6c1)   
![image](https://github.com/user-attachments/assets/2d5f9af7-c46c-4ebd-9a24-877b9e25e9e6)   

# 3 jQuery UI Draggable
```sh
<!DOCTYPE html>
<html>
<head>
    <title>Elemen yang Dapat Ditarik</title>
    <link rel="stylesheet" href="http://code.jquery.com/ui/1.10.3/themes/base/jquery-ui.css" />
    <script src="http://code.jquery.com/jquery-1.9.1.js"></script>
    <script src="http://code.jquery.com/ui/1.10.3/jquery-ui.js"></script>
    <style>
        #draggable {
            width: 125px;
            height: 125px;
            background-color: #FFF;
            text-align: center;
            padding: 1px 5px;
            border: 1px solid #AAA;
            margin: auto;
            float: left;
        }

        #containment-wrapper {
            width: 95%;
            height: 200px;
            border: 1px solid #4E4E4E;
            padding: 10px;
        }
    </style>
    <script>
        $(function() {
            $("#draggable").draggable({
                containment: "#containment-wrapper",
                scroll: false
            });
        });
    </script>
</head>
<body>
    <div id="containment-wrapper">
        <div id="draggable">
            <p>I'm contained within the box</p>
        </div>
    </div>
</body>
</html>
```

Kode HTML ini menggunakan jQuery UI untuk membuat elemen ``#draggable`` yang bisa ditarik (drag) dalam area terbatas ``#containment-wrapper``. Elemen ini hanya bisa bergerak di dalam batas wadah tanpa menggulir halaman.   
![image](https://github.com/user-attachments/assets/78745be5-6709-40aa-8d59-29fcf9063668)   
![image](https://github.com/user-attachments/assets/8afe5127-8a55-42c6-ac1d-8e1e6c6902ca)   









