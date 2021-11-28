<!DOCTYPE html>
<htm>

    <head>
        <meta charset="UTF-8">
        <title>ZIPPY</title>
        <link rel="shortcut icon" href="">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.2/css/all.min.css" />
        <script crossorigin="anonymous" src="https://kit.fontawesome.com/70a642cd7c.js"></script>
    </head>

    <style>
        @charset "UTF-8";
        body {
            margin: 0;
            padding: 0px;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        * {
            box-sizing: border-box;
        }
        
        a {
            text-decoration: none;
        }
        
        ul {
            list-style: none;
        }
        
        .main {
            width: 100%;
            height: 100vh;
            background-image: url();
            background-size: 600px;
            background-position: center;
        }
        
        .logo {
            position: absolute;
            width: 250px;
            height: 250px;
            left: 90px;
            top: 50px;
        }
        
        .logo a {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: darkblue;
            font-weight: 700px;
            font-size: 2rem;
            text-shadow: 2px 2px 30px rgba(0, 0, 00.2);
            letter-spacing: 1px;
        }
        
        .box {
            float: right;
            max-width: 400px;
            width: 100%;
            z-index: 1;
        }
        
        .box .search-box {
            top: 60px;
            position: relative;
            height: 50px;
            max-width: 50px;
            margin: auto;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.25);
            border-radius: 25px;
            transition: all 0.3s ease;
        }
        
        #check:checked~.search-box {
            max-width: 300px;
        }
        
        .search-box input {
            position: absolute;
            height: 100%;
            width: 100%;
            border-radius: 25px;
            background: #fff;
            outline: none;
            border: none;
            padding-left: 20px;
            font-size: 18px;
        }
        
        .search-box .icon {
            position: absolute;
            right: -2px;
            top: 0;
            width: 50px;
            background: #FFF;
            height: 100%;
            text-align: center;
            line-height: 50px;
            color: #0c87f2;
            font-size: 20px;
            border-radius: 25px;
        }
        
        #check:checked~.search-box .icon {
            background: #0c87f2;
            color: #FFF;
            width: 60px;
            border-radius: 0 25px 25px 0;
        }
        
        #check {
            display: none;
        }
        
        .main-img {
            position: absolute;
            left: 10%;
            top: 20%;
            transform: translate(-15%, 50%);
        }
        
        .main-img img {
            height: 400px;
        }
        
        .main-text {
            position: absolute;
            top: 80%;
            left: 90%;
            transform: translate(-90%, -50%);
        }
        
        .main-text h1,
        h2 {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            font-weight: 700;
            margin: 0px;
            line-height: 60px;
            font-size: 4rem;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.08);
            letter-spacing: 3px;
            color: #3d3d4a;
            text-transform: uppercase;
        }
        
        .main-text h1 {
            letter-spacing: 28px;
        }
        
        .main-text span {
            color: #0c87f2;
        }
        
        .main-btn {
            width: 150px;
            height: 50px;
            background-color: #0c87f2;
            box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.2);
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 25px;
            margin-top: 25px;
            color: #ffffff;
            font-weight: 500;
            letter-spacing: 0.5px;
            font-size: 1rem;
        }
        
        .main-btn:hover {
            color: #fff;
            background-color: #ff0000;
        }
        
        .sosmed a {
            padding: 20px 15px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #6e64ff;
        }
        
        .sosmed {
            position: fixed;
            right: 30px;
            top: 50%;
            transform: translateY(-50%);
            border-radius: 20px;
            background-color: #ffffff;
            box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.2);
            padding: 5px 0px;
            z-index: 1;
        }
        
        .sosmed a:hover {
            color: #ff0000;
        }
        
        .produk {
            width: 85%;
            background-color: #FFFFFF;
            box-shadow: 2px 2px 30px rgba(167, 158, 245, 0.2);
            display: flex;
            margin: 30px auto;
            flex-direction: column;
            align-items: center;
            padding: 40px 20px;
            margin-top: 5%;
            position: relative;
            background-image: url("../images/poduct bg.png");
            background-size: 1000px;
            background-position: center;
            border-radius: 10px;
        }
        
        .p-heading {
            margin: 20px;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.05);
        }
        
        .p-heading h3 {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            font-weight: 700;
            letter-spacing: 2px;
            text-align: center;
            font-size: 2rem;
            color: #323543;
        }
        
        .p-heading h3 span {
            color: #6e64ff;
        }
        
        .produk-container {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            margin: 10px 0px;
            width: 100%;
        }
        
        .p-box {
            width: 250px;
            height: 330px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            border-radius: 4px;
            position: relative;
            margin: 10px 30px;
        }
        
        .p-box img {
            height: 180px;
        }
        
        .p-box p {
            color: #4d4d4d70;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            font-size: 0.9rem;
            letter-spacing: 0.5;
        }
        
        .price {
            color: #2c2c2c;
            font-family: poppins;
            font-size: 1rem;
            ;
        }
        
        .buy-btn {
            position: absolute;
            width: 140px;
            height: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: calibri;
            left: 50%;
            bottom: -20px;
            transform: translateX(-50%);
            border-radius: 15% 15% 15% 15% / 50% 50% 50% 50%;
            background: linear-gradient(120deg, #6b60ec 20%, #a166f4);
            color: #FFFFFF;
            display: none;
            animation: fade 0.2s;
        }
        
        .p-box:hover .buy-btn {
            display: flex;
        }
        
        .p-box:hover {
            box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.1);
            background-color: #FFFFFF;
        }
        
        .p-box:hover .price {
            color: #6b60ec;
            transition: all ease 0.2s;
        }
        
        navbar {
            margin-top: 10%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 40px;
            background-image: url("../images/poduct bg.png");
            background-size: 400px;
            background-position: center;
            border-radius: 10px;
        }
        
        navbar h3 {
            font-size: 2.5rem;
            color: #202020;
            margin: 0px;
        }
        
        .nav-menu {
            display: flex;
            box-shadow: 2px 5px 30px rgba(0, 0, 0, 0.1);
            background-color: #fff;
            border-radius: 7% 7% 7% 7% / 50% 50% 50% 50%;
            justify-content: center;
            align-items: center;
            padding: 5px 40px;
        }
        
        .nav-menu li a {
            padding: 5px 20px;
            margin: 10px;
            display: flex;
            color: #202020;
        }
        
        .nav-menu li a:hover {
            color: #6b60ec;
        }
        
        .subcribe-container {
            width: 100%;
            height: 250px;
            margin-bottom: 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-bottom: 2px solid rgba(0, 0, 0, 0.03);
        }
        
        .subcribe-container h3 {
            font-size: 2rem;
            color: rgb(130, 40, 247);
        }
        
        .subcribe-input {
            width: 500px;
            background-color: #fff;
            border-radius: 7% 7% 7% 7% / 50% 50% 50% 50%;
            height: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            box-shadow: 2px 5px 30px rgba(0, 0, 0, 0.1);
        }
        
        .subcribe-input input {
            width: 100%;
            height: 40px;
            border: none;
            outline: none;
            background-color: transparent;
        }
        
        .subcribe-btn {
            width: 120px;
            height: 40px;
            background-color: #202020;
            border-radius: 20px;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            text-transform: uppercase;
            font-weight: bold;
            box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.1);
            font-size: 1rem;
        }
        
        .subcribe-btn:hover {
            background-color: #6b60ec;
            transition: all ease 0.5s;
        }
        
        .copyright {
            color: #e7e7e7;
            background-color: #141414;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 15px;
        }
        
        @media(max-width:1230px) {
            .main-img img {
                height: 350px;
            }
            .main-text h1,
            h2 {
                font-size: 3.5rem;
            }
        }
        
        @media(max-width:1045px) {
            .main {
                background-size: 600px;
            }
            .main-img {
                display: none;
            }
            .main-text {
                left: 50%;
                top: 50%;
                transform: translate(-50%, -50%);
            }
        }
        
        @media(max-width:600px) {
            .sosmed {
                display: none;
            }
            .search-box {
                right: 30px;
                top: 30px;
            }
            .logo {
                left: 30px;
                top: 30px;
            }
            .logo a {
                font-size: 1.4rem;
                ;
            }
            .box .search-box {
                left: 30%;
                top: 50px;
            }
            .main-text {
                top: 60%;
                overflow-wrap: break-word;
                display: flex;
                flex-direction: column;
                margin: auto;
            }
            .main-text h1,
            h2 {
                font-size: 3rem;
                line-height: 40px;
                margin: 0px 20px;
                letter-spacing: 10px;
            }
            .main-text h2 {
                font-size: 1.2rem;
            }
            .main-btn {
                margin: 0px 20px;
            }
            .produk {
                width: 88%;
            }
            .p-box {
                margin: 20px 10px;
                padding: 10px 20px;
                width: 100%;
                text-align: center;
            }
            .subcribe-input {
                width: 95%;
            }
            .subcribe-container h3 {
                font-size: 1.4rem;
                text-align: center;
            }
            .nav-menu {
                top: 20%;
                width: 100%;
                margin: 20px;
                flex-wrap: wrap;
                background-color: none;
                box-shadow: none;
            }
            .nav-menu li h3 {
                top: 10px;
                margin: auto;
            }
            .nav-menu li a {
                background-color: #fff;
                border-radius: 20px;
                box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.1);
                padding: 10px 30px !important;
            }
            .copyright {
                text-align: center;
            }
        }
    </style>

    <body>
        <section class="main">
            <div class="logo">
                <img src="https://lh3.googleusercontent.com/Vf4vOAo5cQIFqdlWUNXJU5V-SFnMly5zjOLfnp092AhHaYGEQ4gkhuW4bEW9yB9yhFR8VmpnRzGXDq7xrNeeR0ToE2mDqZTicDdCQv954qNCeKto_4zE55o8GwBQQxogYJMJsxQj4c49-1CEfimEFvjA7lH2AG0jB---IZWfSp7PUppieq4S8GgyMnoJLdfj-Yfb6bJrU9ZnrzUYUJMppDOjITGuP_YG9jV2CZgZJGoogBFMZKSoDyu_2PgBKX94kxmcz267Aj0ZY6pmupHUmqkOI-Fxx4SK5j6aqKxZ-FHqDXRihm7X7pO6i87aYCb7vy5r1qP_S67dL3ePVKucf3JZL2fv_BBoYY8zjPnOkmBvZTNj30dOv6Sv8F_1vyB8WRzIWf9lIGau9Wj3jgMUEuw9Qi-RsviRyRZfwfoDoCSnCY3lhi8p1eiwggOiVKBuhLILADdgIkTWc9J3qlNtv4KMmY6Rn5nbpNMYzw9mVwYZTg4B0YKDQWrXUC9MjnuCd2daoeU-uUbJRNKQPzS_x6rTRgVYtgu6JXIDRGJtQVBW1En7ZcUdkHPOpWaZ9VDekYSk6dSKAogJqhjj741oFOaTHQ4AtAXDJJ1MroMD3TiWnQdwBRJkTvzMVIelXNLh93Ze6SKvvCFVO8lJRzaC3Kb31xWG4HD8wsVczA92LD3hOEaeTgueZQXNcNFDhGznPE_XAiA00E_vjqZM8LuVNXM=w161-h113-no?authuser=0"
                    style="max-width: 100%;">
            </div>
            <container class="box">
                <input type="checkbox" id="check">
                <div class="search-box">
                    <input type="text" placeholder="Search...">
                    <label for="check" class="icon"><a href="#"></a>
                    <i class="fas fa-search"></i>
                </label>
                </div>
            </container>

            <!-- main-img -->
            <div class="main-img">
                <img src="https://lh3.googleusercontent.com/-6xmH7yBUt4mJmggICeYC_5a7MfXrSTk2iPHSdZj2AJPKHGQmvA3oH6bnr4z2vZvXDnb8XpnaQzPmIiHyLevonatiyydjd6U2OypNKjya6RiXxiEDV6uMWSl41wPC1nqY8qudknmDvuzO2VyESll481CaYf8UwWscn270UOs-tWT9q5gGKj7CjHaHhKr_96cvimMzi2cpjWMLdzmKsKHBQUxX-O8wUaq8ydJGDxoHTMgGYQHqD1rT7AqgUuvkVxcsoaAHO8W3EKPdzQOykmRyAks8flOmjFs2yOev8V02O-z0RIJc6ha4i50NogJZZ8SXfPF32D2WC9s3L46ofgunoSBUcd9dHylghJlQKlheGcrvnP9hwsbqRy5R22eAhsX9HuQSgcRFJYjhEXhcgTR4sa44sP77qbotpzUoDQk6xHqmf-m3rA840N9AK_7m2mxepl1Fpn93-Q27RsYbh-IkaZXan4qdRBmBN5OIIrCLMa10lH9bBZw7h5i8FZRGaLy4EBA9zh7x1JA0-aTgJeIValiWuSbnS82o6HgCgApnD629DqaAFyDHdumEVMIaZiNmbJ3Lr8sMePFBb4gB1mHxYGXnXKCi7jreicdiiluc5i7EMmehuel2a4tOc82A-0uWs4mAYehTFBteJeFJSKx9Osdc4oNmbTN6J_wk-FXFManxgDUhaJe2EUx9p9REEsFSl77YIsHEznMkiEz1zicFGg=w370-h318-no?authuser=0">
            </div>
            <!-- main-text -->
            <div class="main-text">
                <h1>Su<span>mm</span>er</h1>
                <h2>Collec<span>tion</span></h2>
                <a href="#" class="main-btn">Details</a>
            </div>
            <!-- sosial media -->
            <div class="sosmed">
                <a href="#"><i class="fa fa-facebook"></i></a>
                <a href="#"><i class="fa fa-twitter"></i></a>
                <a href="#"><i class="fa fa-instagram"></i></a>
                <a href="#"><i class="fa fa-youtube"></i></a>
            </div>
        </section>
        <navbar>
            <!--footer-menu---------------->
            <h3>Kategori</h3>
            <ul class="nav-menu">
                <li><a href="#">Pria</a></li>
                <li><a href="#">Wanita</a></li>
                <li><a href="#">Anak-anak</a></li>
                <li><a href="#">Tas</a></li>
                <li><a href="#">Jam Tangan</a></li>
            </ul>
        </navbar>
        <section class="produk">
            <!--heading------------>
            <div class="p-heading">
                <h3>Produk
                    <span>Terkini</span></h3>
            </div>
            <!--product-container----------------->
            <div class="produk-container">
                <!--box-1------------>
                <div class="p-box">
                    <img alt="1" src="https://lh3.googleusercontent.com/qgOaX4X3z4ZsbLAjRIZOp63QXXvR7N18jSrY4wcB9Vc5CuzY1U5h1anJyfF_ZCLcUGMOlnergcPaFm9wNydSfFhJkFfTpZWhuaIQI-Y8GSYkeqXklKaTnttiexW9sN9lNYZrO2muZHBDpfe3HLlbGFVZQsAkfOq2uSfEmv5lyVGkjs0BjtI87QOgmEw5oXFFZZvNlARNWO66LLfuSkB8lYQ2gMyMPDqNXn1Upp--GUwoX-93ylRdXSga8ZK_1zZezRAy8r-FL_36Qggdz0_R8l8O0FmCA744PNdSzY-mYbk8H1kSjO-T0kAW1nZAPbX-DNXl73V5_PLpivAyGix7fvCS2bD8-kUKz07RTaZi_lIi87-lxrnu-e7WiYn35YQo8PUDYl3oU-4kuEp9gICRevkdvc46PR0QocXgUXQbqZbJa4kujG_e9aySS7zoygRILOGRnKG8sAOcABgmLCX2aLu3RLRZ_LEdGkpk8T2bXT-0mjPLWMxHu9WWoUPQk08GiFnwSc9M4v1fM9flWqzzQ83KYZGtPYW-0pNnr8qjHIS0elKenIa8S7nZ0eV1GEb_Dul5xEXr9kwNPN-ocXUQR-qBGqxLUvL_YTcINcd1oi-Pt0ttktSuST88Z7R6SurfEt1hzL8pc-l1ChZn0t9vt6dfot_vBTUFiVahG8pa6UkbvH5dZl-Kw5NyJRgA57ecb9z6lW-V9z9dzI6T6Eggr2k=w185-h246-no?authuser=0"
                    />
                    <!--details--------->
                    <p> Tas Black Genuine Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 33.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-2------------>
                <div class="p-box">
                    <img alt="2" src="https://lh3.googleusercontent.com/8pUnEKwQyswxTfcmrXtaW8wOmXLdtYNClMwwwJ47eAVWr4d4AL_yk8x1It6inu6wNzM0OlfB2oVuhSgn1xs_v13H9FHpT8cGPOV3oEb5DvdpTtc3pY-diOs6zY8fGn8Qqtn2Rfq9XMWyJkl4IYNbJIgFiyqbElMAC7DI5l6Al-tSMXtWs01BAZtOjw_fHPxm-a8pVqK4xfmev4U-KewnKl9r5WVqHhtFrCdYEBBPdmkuHtMYk5UjmprBnRWyf5AmLijs1DPBEZrseIBSzxEa0qWWRqt5zGrXmhAkUPOCjUk-WnMS418SksoXOE8b2oSv4bzuQqNcXxrfEOBkyD-03_-AKrdtG7SMrK8XljvOL1KVuQQDyHM8jUEwxlEIlzI5Ml_ds0F221zHeJI-haFe37Y_YapQnvA_WWTPa3z8ElLt8rvF2wRGokbvUbjzZcKtNuUdsLZRtDaFviSJQi4tnttFiDBtRzXOarlDo1ghvJuzwR-idVo90f_MlFheQTolhZt8-StfSuAe_fY0cGfdQlFDs54Yo9vV0Bn9MRP8Zc0teuSeyl8aA3LodxZ3X97tk2gPJhBKVwjA4HhwNFHzLh8v5i7BzqH3I-XkWvET9zrkiXlVlf4XCCkAJqVJjtxykLKY2GEUMOr4yKWqgkpF8aBiTtZhx088vH4m11F_5hquB_HaqNxqhmeVXi5NpbqaKtsZjqB0p2K-yIeAEdAVy4o=w219-h221-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Fashion Genuine Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 36.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-3------------>
                <div class="p-box">
                    <img alt="3" src="https://lh3.googleusercontent.com/822tLFXD6LFLEAqzbASvw89QHHsLBlrc3tcTbRook1v55XmRHoQtt9pAif9WgZKdxyhfZw0bSycoUHYewHm59O1PzgJJTGhpuJnlCHZx6PTCi3HRmcYAB5P4WB3Q1Ot0BpfZln3NUUthgGTjizfor5XqEk1ICcXF80i-1E21lTNTFZoM8MPGPfKHhsLnhpqUuFqqYm1TjX6FrdyuHdlvGiRbyAIdYBKauv03taNNygX6EnwW9iFnZubOZ5ydSTpcXJr6ty1XdvRr2a6wAo1t5ZdaibmJgBc9ASrBOOVkt-hX-nQxXYe6SzVxAIilr9p_zw5Xqt55ZZNjOUhyJlmKje3v6dSr_eJryus0eRa2N8qfO7H1yyWww6TK3LmOBXyXVSaKpyF1gae6XS8GmgiQ6aLqr0MGpySY35Hvfq3mc_dhWgDVls7OUnb4iaRhTG4otMjqeljwBuG97-DKzcHVxe_45oKqp8QC0HowoT0PrvMbhVnKEXDFsjnWfLuyraVoFUo5jplb_yHAAz1SgBegJcfMNJvwYqLujS99KwRzu51jm6RKY1PL7z9HvC8FDOqJ1XPurszug2TCu-NsCpezWtQM-uU8wBUVpPCCBhTSq_sxVps39zEoCRVR_1TFrEsvExbzZ_8ozfIVSuzRkRGAxIRW6RFlfRRvCeqIAd90zrNKlOSUUGmE5tEBzhvjlXZ9XvNDHQxdw3khHsKpRqssrME=w197-h254-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Genuine Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 30.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-4------------>
                <div class="p-box">
                    <img alt="4" src="https://lh3.googleusercontent.com/OHsiSTXP5FuzS56hbWe2h8U1plH_J56StOFzCb2BMZ-cfpnBL-xkbQ0SgIT_x3yY1wVSUmZRZvQ0iFaxfjDpYrfsGc_7J2S2Ktv3zSIkMvc8MnF2hrpbxWSG32pOSoeH4oUtVmfmZpHW0JxBX-Sc-mQSAeEZoq-ZHLWpK8LyEc2LfvBF9V-pJy2opJ7qVV4Rnpe-q7R7EMVRW7i024IURMsb2-y-sJ80gRAPJnYRq3PlHF85SsqzEj4okeHwf--yRZ4TkSwQjQHIzCfFUTbQR4UNTHY7pfIQHF7Y9Ioc95Fu_C-xnnxpqiN0SVQzn_iRYLJ8NZsw4o6Am73_9fJIVAQwzB9KWLctriUxMozztkPxalMpS9wt0wRqpZBlglMKt_9w-i-cqkk_F7vehY6Oo0D5VMvinxqF2dNVfAttUj0GwrmkbdjZ1cPOSpFUkjy552wEWMEkO91dvtz9-Ra3qzUcQ0YDYUSZNfmVNnJan-bf2WaThkSIEw1kIDhQv_FgF2M-wc_8gjodNmPJvACTCvcbYuIod4O_VOneRDCRI2WhrnhEb_gfF59HII8dw1HyVue5Vp5Rg3yNz4Q7-mjeizzBI3P9B0RkbVfNFj6u8ifwwDooR6oCLjyajAWcRcj2p2ONfktHWaxG3ei7BwVm95CLuunYZD7jGm98OqSs7rCxPu5S0V7up3QC-GJ-BtJ-7_kHHamRm6DVhlTImZ5VWAE=w152-h223-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Black Chain</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 47.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-5------------>
                <div class="p-box">
                    <img alt="5" src="https://lh3.googleusercontent.com/8Kz4l9xLqTkEAJyHF4ZlM99YfKL57QpX-5_9CHQ_wQ7y55QTVu-e9zIRm_yA4wXmjYHyxNAyG00lZq9IitgzXd-Y6920oO7FjlKPARoSoRugjF0yA2uqxigX2XnNYE1iK5HVT0dBCnwh-S4_U6b4YNPC9oWN4cP-eQTzkec4ye78uZHjCeTr-GM1ebPFglPOwAU3frhX1xFkx058b_K8fYelErgnt8Ietw1-2svCGeDIOmI5lGpAp4smDNjv3-hy4AUSKxgMjVQFyn0sxPKDW9Bb4V2FG-N6parzxq--Xl7Mr-0x6FkvT03l_oTd8ofeoUyXNhP2-THJ7enPBF2JxWJp3UrDGpofd-gp5VyltCYhhgaROi8rGrq-AWdCJSDpTL5F9F4vnALtVNpFTD6c9DGN_uOYZKRJVJPMBk0rnufNo98queGrSWADg6xdEtcMDuSyciIKdsCSdEyGbTC2DRgtoWH5fQzotLqiASafBPACOt5BYvfNJ_VGwxKT5u4zrUxhqmt_VgaSq3iEHvEs-avkmdz2l6wEW0uowWweCS9Yl0HM9VQ2QlsROnTZcT9q6qgN_w1ieYTzKJUV39w4r4dctbGf12hCDBs6WQkaPxLSpNlbz343qOJmvpXxH-6EHbosrPmU7EqNDLRcW7lDM3L_4X9nQiNPAMCbHC2zPnU2f_5h5Qbr3PX3C0KnZQRgNKKqh1oUvGUrWg6DxDiUBL0=w152-h223-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Lether</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 45.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-6------------>
                <div class="p-box">
                    <img alt="6" src="https://lh3.googleusercontent.com/YSFKZZTcll25JIaP2seNA0YqFRFvQdO2vmBF3I65N840w6J6kr-zYEZuif8OdrUN1U-uLvCgH-3QHJXiV_m79x83TISlzBJrBYAW6BStuSJX-YnETve-H399p24xpKvzI2FbhXh5kAeztvYknUtwCLQS8mj03YKoXf8W6f7o2goKO_jSY-PJVge_PbJ5sPwnjYrbRHn3kCTqd44j6X5NJ0FuWWXi758nhdrfaUc7ndritTDCxstYzNSkRObQfqXfP2SRZaBj5eRDpVZWEiQseGhhW2AOGqQNS-mf5Wbwxdz1VEBpYgrk_NzukHprY7_tmJSJYtFf5keurlLbG4gkuGZE16QHiK07SmmUyS7_G6oBg1a8k-0QtO5OmvdOtb-3ifECyCPb6ZAGOuResiXz_wmF10BuTMx9O-LjNsJe4yMJu4eLquIburhWir5Vhm9CXJdLuDeJAX4V-vhFrnndyizVKhCOOJsGJ1h2IGgrh2ulXMa3WBrKbTNkvhLofsEvAaFPnu6Vz9jTeGAzwtrj87Sq6sOpH1mMGp2XodU2tFAX1KUltlJYmu630PfzK2OyndxYMnaL16wjfxshup0lAZH8CXwV0EyblpVX0_0KB4Xb8p239sO0lnOFxgBgV3RXMSI0ucsxRSmygiF2FtaXoEfpV8yUsqda_dVCdlKiAjJuh64oXe5plE9X3wnsqdyqX8DgwZaUsv-UclLjKvDmi6s=w114-h211-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Forign</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 49.999</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
            </div>
        </section>

        <!--Tas Terpopuler------------------->
        <section class="produk">
            <!--heading------------>
            <div class="p-heading">
                <h3>Tas
                    <span>Terpopuler</span></h3>
            </div>
            <!--product-container----------------->
            <div class="produk-container">
                <!--box-1------------>
                <div class="p-box">
                    <img alt="1" src="https://lh3.googleusercontent.com/oXouTkDO544yaU8ENEJm-vZY5ZAtriufAkbjhURmMtkrI9XXcN2gA2Tm6xx7mBkV5UIWccfbmpvIXRP8h6AQ0ILI4zn1XqKsvic6SVbe6xDPFIC_POfpCesAKBqqBCMQUbmGM96vM7ufmshUrLg53HaVVa9nV7uR1j7qkAV-hBPWTYvu_ygWtio_ldXzQlyVGSmefEnjkKgY1jLz8zpFmy9ldPC0eREHxTXpQ4_rKKdTpnPUUeeKJSGRMaKsz64JNJAsMbhTYd33wGbIGIp7HrBre9Qe1nu59HarJC_GTI52jzDJRsJM37JFHmjoVhrKOD6PM_ximaA82BKkhRraT5GdsPnncWdCHuPzQY3OuXHP9rDuIke91tRK2yq9V1WNEAZ9wES8GV0ZuxW4UKJ-FXCZqClgfCaQLegB43m6A4ycYK4O5PVo3xiysWTmdzugz3y7nEX5XeTUm9s9ZE32zqM6axTd79pVyMELPPZT-6ob9v2V4iR0VKAjQgSjQg8Boc-YFI68QM1UtMjOFvje6YMVtwlrvdcWNBN35Wy0uq7vxd24KExcLg00MxnwJamJ1XHsaBR1gAPGyQN1LVXa79KyNbAYljNcvoybYdYtTGVy3_FcVbBZgQdNcTXFZ5glLe233GaW1EBaggWFzc8E7cRYHsfBim9_q8sZN4pU-j_7rgd2stfehZIM49E05pF4pUL8d1hSSKmlvH4iGU0fiUQ=w219-h221-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Dark Blue Genuine Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 30.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-2------------>
                <div class="p-box">
                    <img alt="2" src="https://lh3.googleusercontent.com/L2eSV9J9tpz3k-Sc5VN3zRweda4ZxenMWfAt6-z7Irbaq1GhCrfvM2LbrDbePWH0yY3731_pGRS33-XrV-qQZjWUctAj3UpGkvkBVdYTnNB9VRegghGd4eGK3oIKpQvOFQB-nfVpvq_VoJFf33mxPG2rA8-4cE0FdH4ocANbdX--dIEY4DoztaeLKGvD8DuEwOkMXfoSYN1sfnWUMSPV_jUihc0nt4iR0AfWUSrew9ceoEHeVuuBVAxdDlmYqnbTX5PzzfFYV4-QSsUgKaA8FSESbjDkW4i3-mC89G0J4475tC0qWxKmQKw--1Cjnq8lrS5MolmJsc7bnKwO9IPtxzn17ADflHr2m1eWt6rhwIslKKCnzMLTt1i8YzUWCGa3M_umP0vUUEWaZKyepUpPeElBaJmEFdgFUejeCgpeyt8Jjzt9MRwLnDHQl5KqQQwPvmtioshAftolCh6rt8RGya7kVWO_OrVT-HRrmLzWVfQqOmbpF_I9i4vvAbQKKRTn55SozvovITJuykYsAL8vmH9vxSDnmh756z9AYOAUIF_KDm4XlHuQ9yVHFx2dm6Z5N_W6MhBtsRJrfT0LeVOeeVr6rOAQWt3YlMiBVc0scJR-QpMY8yTk9JZXBd4bkXLxuMni20k9Q_26FFQ5Wle59BUW_NcW7cvKs9KEqT-69aPGU-irTCoXW-cljt_IxgYFSEN-B9rbVbFI9-FiSfgas_g=w225-h227-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Dark Blue Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 34.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-3------------>
                <div class="p-box">
                    <img alt="3" src="https://lh3.googleusercontent.com/GMAXdUHR04VTbywB-v_rqNUlRV_auS3r8bQkw9iUnNfFKLR88l1aYJh2VgiI3jEL_iOQQbP1ec-kAH9D3RpXjuiRZOrQFXWxuuK6re0wOKUVo0GFkVHvKoIyOLwRkaGDzlMfMJ12omOmVV_eyTWzoRdq4uYZZHclWkIwSW8-rNRqAQIFwyMov9lQs5rOQo2h0XuB1iHI0AEQ_sw4lxlXZFbLfdeP63cJApftL1IJXdVvFjceKWENf6ARBm3YZzzJI5I4P4oM8zpYlR7YjVCL7MuJIRisinZhH6tPMoA7VWfn5X14o8Am4B6I7OG8wNYT0KvBGeMIQqUnME89qxg50KWOigANo-W--3_pFzw_cW6hpVp1rN09vpAMA8BNhvbJtkFvyt5HieHF4o9fKWYRaGX_2Z9Et2F7Hw0Wx2x_vczOU8GTd6_unlKO19z2-SU3AW7kbVT0taREV3FOU-H-mTIanF6ccC-jZJnCvONoc4UHx7TO6tsA-Q5KP5lja-6ndSzZv3HjpQJavrmp7IQi0SVQlfy2ySUBy8B9Uku7yyGtDuSXqzDBo_LLLsMs0SdaCS6-1fYo0Eb2zJXvjW6Sju_U20YclTW-8ORIPxDO7s_KWlDJ6SV6dWDhhv5cwYbCO7DYxmBt3Jh36Qpkl7b7eHEo6U4OwnIKha9ioSl8fRgoAEU7QcT8Pbkk31ajmUkD05RLP4dOcT997Rv9GDNivtE=w178-h231-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Fashion Genuine</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 37.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-4------------>
                <div class="p-box">
                    <img alt="4" src="https://lh3.googleusercontent.com/u8rur7taTtvHjbIBLZukf70DvdWcr-W-YUTLYljrDyfluZTMEcyclH783KiLi4qCVVK5-3HsMb0pSACo2Z4Cog9oopT5cDP6AQnCiflE2pzJO-kPknErHkjR7zFw7KcsfnemwOncMke8iab0IosmlLmKKVUoBTpHK6zE40XoXF8HMde6Lbuc1SunYcaSEpd8XkqcJ2nTV-1TTMNL9XqsJdXJ_ppVlblzI58vUKWI_H3dxIiDo64DmYowhV1X0D78_-MVE9Eorbyl2Z-ixNeXTUz0quLnUc2N2h1l78eNnYONbgCy3p_gbzZOdZ7J_1KYCBNOQ0oaRgGhnXo6HSwGd0j4dIuSPIf2QiH-Lqw60xCW5HgZ2Ldkw7KZY8u6rsj5qXczo2Mn9BQaJtOrxMRMQRDmGMbQ0sHhgaQCYDAne9zjx1lJyFY2O3a9r_LpCyWDYjk_usFVECpZQrPFWsCIPgyPUjkp33itIfy2Th4zuhEVhd2EdwOAtQhA75NI36n-N6g_W7gWUB2LHzYcMopoH75mszP8-Bz69r6rZ9WPseTnHTMT7306IgKT3aeisMdQfjLuhgjl-p0FEZrfJCwWNL_zhiaMMtjz-i4l4h3OkUp4SzZmC9DowNz7NtlW_E4xUy5cnCIcWYYXIad4CHUezBxTntTgDQ9saO_4Briw2J6jrw7CHrzGtlKMujnKkwEqncRBmPqMG1cbwEac8Nk8Tu8=w185-h246-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Black Genuine Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 33.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-5------------>
                <div class="p-box">
                    <img alt="5" src="https://lh3.googleusercontent.com/pk6ANrlKoSE-oe5NOdlCI0apJJDYS3SqEA-2mKF1V8DO94UjT7NkA_wf4cnLM4oXmqhTrix0DTAFlah-a-5VnDWvziEjB3i-aaGwYsCUlV75-x25VsrHUrtfN0Cr8AhAk2CnOUPN_grA7INoLdjq3ww7JBAELZtaE-gOE-OANr3VFL3TjTgBnKOtkme6N1RTYZMN8wx2EY0AHiB17moMA9pbEX9LLFwa_6UJvYEwr4iSu9pnVaRLv6TumA5ieKw_NBWRmef94uqQr_ij22CV_vAsVO9RZGFUVvM9QoGdi1O0sK700shP5mLGrNMMBGSki1rPR_hwP1j3YeotQwRm3lGDPmo5L62DMkIDk4aWJRoB1HC2gGMmq45UfK48p1W5qdjJdkAyM1NKxcb4l98doyj1Ntd8wuQTd_2NCDVZ_HWhaG0f7bCFvAVJG9kQBf-1OxWg3E1c9WnaURBuHGPW2EVrYcHdQLx8kJWG-o590jwCFHF9UgDZYGRPOJ96CaT61CSJ4kTgmI08oGOBY8fKbPcP0CmVa-v-EPShA4IGOh7SWBo_9rniGxE_ZMN_6OMJxuFp8ug5LeBkKUp94yz6WDlNq_QrA-kZWBI5OxCwxdm1jHFlU6KcLR1kFzU4Hn64aL0-9E1Mzs4lXvAOcV1Ckw-W4X620pjA-QkEshvl9RK0AaIyt-zTDulrm7DyYLPWa--4KiWhLRN18vJkvE7D2Gk=w219-h221-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Fashion Genuine Lether</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 36.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-6------------>
                <div class="p-box">
                    <img alt="6" src="https://lh3.googleusercontent.com/OaKkptwHPluLKIQAlJE7zWJf77_ivG4o5o6Pr8tvgX_wo5eXa6HEqGSeQ-mGoKob3U7BsmevJyFekGi_WetVAL-bN0f1KiWyLd_JIR77Qwt7JMImAgqmIS5wKqgf8Lz5g4SQvoloWX1bQ5L9NHn3SWbmPGEinOXMG8T7tPXoVoVoYQ2D7Aycz3yll46G84vlMgsx7IgagpWzvU-aygq-R1Qo4qvEA_g7cdZdEI4gzIQCS5OIqUCQqaKjQNSr8IEgI4wcHV6Rx1yqZ7tgPiSwCSBQGx2EoiIjbWSFOK3CLXEgy9m_KKtzb6Hdls5-TMnrnbZTji10Iz-g0IByK2Lk3Vr9IV_MGXbHp1KaHqajvG7mN6HHTjX-lnAm36nro_EYsqJsA2jklJgcUwUKHeOvRbBKfkhujyPDUNK86DO6N2Lb5EAC-cuKvgKugiDlh-LXX-PdeFOILI54M4xiNDa8KNckkuQjdTtXrshz7v8vRB6J4GaPJEKOLqsMGXts9FabVoNbOnJjiXxx2ADZdffCG6Wt7UpkujNvqjkF2cCW1bdf_aK3L9cAPz87ctCdyNctNd9Snts98XNLVnvUkwJzhI4QE_Hc0rc3KrXrIJegsj9kHM2ou6wKIHFUNVWr1oPYBW_a-YuHtxDiGsuRqQtCrL7VArOReem3ZPwjmqQDPk10mF2PnLeS-mvsWS7AppdcZuFQb7FJBOENIsOjmUPitXw=w197-h254-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Tas Genuine Leather</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 30.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
            </div>
        </section>

        <!--watches------------------->
        <section class="produk">
            <!--heading------------>
            <div class="p-heading">
                <h3>Jam Tangan
                    <span>Terpopuler</span></h3>
            </div>
            <!--product-container----------------->
            <div class="produk-container">
                <!--box-1------------>
                <div class="p-box">
                    <img alt="1" src="https://lh3.googleusercontent.com/j5ARyazQ4SOGdKG_6GPh2pFBpOpmdn3_SycyHPdBorFDbWvUYm3b7Z50HTJdCNK6aaVlr00_mfCKLlXdmKn1L021dR84MgqiHeWbUKja6RaZtp-n01HQRKC-y01NelKuo1eohXc75NuxVZm3ZjXSotT2TXldJldfe3mWC7fKXwGgEDWyHLQCt4UxSpBsaIem_uqJNC8TOmgcDTIA3GwCTVZiUnU1gkzW2c4tpnryrsK8Ql1O5HtYTvlpu4Khsm2c2sX3QkKQ4hwQmnwqhYscfawCBBBoq6YleaPnUN1PQlYPBtZ-AQ5ZpIlBbhE9wHhy2xbyCzNQ8VEQ5NifKNXezAyoWoGBtGHseYYPYFN-uwmdx1VPEq8TPhUeokSmSBwb4yCDCXwIpXHzyd1vOmDC0EU5V5TudI_OZoFgwKcEn0SCNRSUetgdA2Doh6HZYsK9zprJ1DnJP_QAjlX5OFbJU1fm-cUjTlH9EFUzh8xWu6lbmCmbtcW5Q_gI4XwFyQyO6xA4gFtL18ZRxv46A_nS6EFh_63p5khICioVDz1C33r42HNKoMafndFTRzu4IGrRxN4EBFAnmPi9LQv4Ye8M7QUPxvPp1R0gX8O4d73_y-vJFr1hWQZ-f4O6YGGFdJ3cM0cVlh2rUurzQG-PdC9iWwricMKMG_vJnfqhtwjPylXgVOcybMa3uFkrIxZeD1ZldCGMy1j9BCsu69XKM4W1AEg=w141-h249-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Silver Chain</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 40.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-2------------>
                <div class="p-box">
                    <img alt="2" src="https://lh3.googleusercontent.com/Qa4EQBCASp5OxJdt_at0Gi-Gi0d9Bb08WsKryfmje-rDuEBdSjMFebGKXpPHK0L5NQcnA8rsQtCiDP1VQfZel3WgTGsMeXhJMqxdyfxXc3MjGCYrbLqXO6UCGHCho7-O6LD1sut_Rz6NibicMacDnN2jgQOMhcwiTOuO8fUGCoG6C8pZONwvH1Gl_kSpVZHfoplLOdE6Jwr_KTUKDmJm0vRuVJZ1W7gq12cu4ZCe2VguCZNyri27ZHVNo1k3ibZOv3r_TmYawraBLddRrnripwkH-aNYQcVUIbMLfRrmQBc7qNE-syS_-pEns4ov9jP1X8NJamPEstcfRouSW2q5ay2O7-zCK5HoXDHH0_Y1AdXZ-QuIEF1bFDAS2PmXA0u5Br7Z5otuJ1C7tD8Pgs9RXJfGp4WaZ96BFp7h-GhzjlQU6HiIj_rLpiVcN_weivekZufU3EE6Knpq-2N-57yJh0D02BapOknPRPZl8LQUJHe98CpldAeewq0EEMzuXzGA7D9q9OiCxt3vBBZNvuiYYLejAxmW4A-cU7xIafSef_hAXJLjhm-10lo57OvQh8fRTyJO6dwsmT15x0Xj-0vqZb3Z6ipicCnOEb6GvzM_Wg27fPyaYFffwick4UT19y7cK8FVNuqoFlPOGtHIiD_NeKJNNj9wsJ8A-V6X6tbKtDuCvLY9UymTtxTLe86h7_wvQtkaJfjKXrQHY17OWISON1E=w141-h249-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Genuine Chain</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 42.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-3------------>
                <div class="p-box">
                    <img alt="3" src="https://lh3.googleusercontent.com/jeB0gBSxw45O3_lhr68UeJmpmpfIY1dPDU8V_FficHib66-BerQrOZCFWjaeladSs3aKo_P5wdvoMOc7lA2ugUBQWg-9evPXu2-NXRNAj1clmGrhJ0pge9bI02-zODOFS9t1h5fHLFQSOEwQEi7WjKy-bpLYnmQBHDXq0V5eZJJXitzxyaSrIfBlmKRaz_tsBsWodqhAjopHmEoPMT39dnzRUW5ZuBEGN5gmWT7I6qmXY1nHcVNf-eNd6pobRlXOP8fXcjH7VOCsJEAOU1QYrQjvBYLfYaJgxyNUzY6xmL6M_l8SQoG8dtBmV4VF1MhhvJyVn-IGHvraPCkhOAiP0ds6Qd7AQONrWNjkf8N0CaZOmMw3S3TK5K4YFal4w-HQQdggBweb9UL6ViE3ezHO_U0Sfv5AvonHWz39dK-mw0IEpM0Re_MYo3N4yGR1x_-N3rci0fgI37ezilXaO7TFKM92rwpxJRYfsUt2UjCMKQJ99V1jZgRahPkodNucE0kclH2X2QtsWLAsDexGme9lVbLME2TEv1KIviYO-d_iD_Oc7QXGxeh10ez0Lm46OxSu0NtWscX6zbX2obznGrzIkBb3gO3czGoKN1f-JJMQiEi4WM1t3WShlGuvANZQ5fjxzcTtula5xzXBCxZHXf5g-jvwWVPCd01vu44Jq9ORey-LABQn5PX6Wgm9Ebn8uVYPgGw9gGyOYoUZ_x1xxzYG5ho=w141-h249-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Chain</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 48.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-4------------>
                <div class="p-box">
                    <img alt="4" src="https://lh3.googleusercontent.com/OHsiSTXP5FuzS56hbWe2h8U1plH_J56StOFzCb2BMZ-cfpnBL-xkbQ0SgIT_x3yY1wVSUmZRZvQ0iFaxfjDpYrfsGc_7J2S2Ktv3zSIkMvc8MnF2hrpbxWSG32pOSoeH4oUtVmfmZpHW0JxBX-Sc-mQSAeEZoq-ZHLWpK8LyEc2LfvBF9V-pJy2opJ7qVV4Rnpe-q7R7EMVRW7i024IURMsb2-y-sJ80gRAPJnYRq3PlHF85SsqzEj4okeHwf--yRZ4TkSwQjQHIzCfFUTbQR4UNTHY7pfIQHF7Y9Ioc95Fu_C-xnnxpqiN0SVQzn_iRYLJ8NZsw4o6Am73_9fJIVAQwzB9KWLctriUxMozztkPxalMpS9wt0wRqpZBlglMKt_9w-i-cqkk_F7vehY6Oo0D5VMvinxqF2dNVfAttUj0GwrmkbdjZ1cPOSpFUkjy552wEWMEkO91dvtz9-Ra3qzUcQ0YDYUSZNfmVNnJan-bf2WaThkSIEw1kIDhQv_FgF2M-wc_8gjodNmPJvACTCvcbYuIod4O_VOneRDCRI2WhrnhEb_gfF59HII8dw1HyVue5Vp5Rg3yNz4Q7-mjeizzBI3P9B0RkbVfNFj6u8ifwwDooR6oCLjyajAWcRcj2p2ONfktHWaxG3ei7BwVm95CLuunYZD7jGm98OqSs7rCxPu5S0V7up3QC-GJ-BtJ-7_kHHamRm6DVhlTImZ5VWAE=w152-h223-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Black Chain</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 47.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-5------------>
                <div class="p-box">
                    <img alt="5" src="https://lh3.googleusercontent.com/vuipkUph9kFJCGQzM1TSgp6_t7GzBdYruDl7kgNlPXuQdaC9tHttAD12Uk0wDvHpv1zdjs9lcs2Wuph2SKdEJ9Sgp8rYAK3EIIvWeFjwD7TsfQgBW7Mp6lmGAKcCYktS-LIRZ_IDTqMbiqGk0hgXkhkFC9N-T57CUJX1DNY1R_3kuscjaD0PsnoieJDbi4cRJJfvOF4PDVfhh7l92Ixy1Dbq3fFWsHOk0Laoz2pmr9CMB4kr3FbWq-M-Inx6YbkDqFfsAQsiVrEE-rU4srxC2vIKf5T_SKMaU-M3ozpyAgWlzytEU5yZo_VW7x-5YXROtLskyuuADk4SHzWZKCv5D7Wxa0xT9joUt1KWQnODgLj4HgtRrmgj5L2VStXUSWMwyTjpxkk-41Ufsr_WYRTJPxfSxb6uqR6RtWc7MYjy9U-sLTRDDUXDly0I5_pqhhrPy_BrNQ40xa3hjVVIITtcBo2oA4yX9n895SlBXtnMKF-CMmlQ9MEMh83bh7tUpmUYr_YcV6SEi5-PJsx5WA48pGJbVtRSwMgvWQHmtO8JN5pl7Wp25BeMgX23JAfOqw36uMkC0MWR-se3vIEQpdqDy620R1ChE7ylUdxLvEfYLQTEJ2Y5KTz0dqPwdwn1d8jgMOt33_oEDkLy2i2_bi9GQ16gKIwtrl2T1qH2z5wOvPZt8klOFq6qwtA_BfvQTIfOV6rWH7VyxBS96TjgX-k4KYA=w152-h223-no?authuser=0"
                    />
                    <!--details--------->
                    <p>Jam Tangan Fashion Lether</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 45.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
                <!--box-6------------>
                <div class="p-box">
                    <img alt="6" src="https://lh3.googleusercontent.com/8VE_1f6MKDbBU0tXrlqkPmXNFjkUtIcgewiMwIrx4kDt-6awlk8ZR_4hvfVVll01GuUVje7KtVe4J4JEEnzvtUjIcgb1P8HVo3jImBjLpe16ffv5G8RK26T-3_ugEka-C4GXFDaW8g41u5D5zIDa5viPfdRpLekIJnDvamvFBiT4cIaC0_URNxUAWykfaLCysiww7-6HBUUEFyzvj2C4sx34QwOtQATuBy-umu0HjCFD8c0R2Jjnx1a5fCJuoVrX8R2sUnX5l7v8UlRliYLu6EvBezAglrI1ZzXHlhXdCO-G-ubTZJ_U9fcuaxT50b4Zky4ibt-UTXzmGIsOdfyxbyJTejo4DP-QB51Ifue5VWIf69cgzUJAwT5zXQ4rWLncfc1vstxQDTRRL6Q15zyLJ8Pq3KeQX66PYze-pMwYeYOKCPEweARshq3deejfXz3z6G-nVU3FGpxZGW7dEBy0EW2j9FvJtyssPr_5u0AAhWxRYxZDZay-dq7osygzGuxPyE0i07L6tRm8D8WmZF3npNHv5BVyXyz_GekHqwpnqF0frMZgIvmrO1uV62050f69hDPCuWPR833ngKTGT1IxTqL1NX9RFDkWIAgU-lhILlO6Hm7ibVwQWguBlJg07kVYyJPd5mUHZMZPWQDD__FFPDhWskAkD_LV9yA75y-qTuP8u_xP_NP0o1SLhGDN3G_ZdsXpn7-Zuc7XiQhS9Qc8xNk=w114-h211-no?authuser=0"
                    />
                    <!--details--------->
                    <p> Jam Tangan Fashion Forign</p>
                    <!--price--->
                    <a class="price" href="#">Rp. 49.000</a>
                    <!--buy-btn-->
                    <a class="buy-btn" href="#">Beli</a>
                </div>
            </div>
        </section>

        <!--subscribe------------------------->
        <section class="subcribe-container">
            <!--heading-->
            <h3>Subcribe For New Product Notification</h3>
            <!--Input-------->
            <div class="subcribe-input">
                <input placeholder="Example@gmail.com" type="email" />
                <a class="subcribe-btn" href="#">Send</a>
            </div>
        </section>

        <a class="copyright" href="#">&#169; Copyright 2021. ZIPPY By Nopandi Ariyanto</a>

    </body>

    </html>
