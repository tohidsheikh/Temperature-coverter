# Temperature-coverter
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temprature convertor</title>
    <script src="https://kit.fontawesome.com/b94ee17cb1.js" crossorigin="anonymous"></script>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        ::-webkit-scrollbar {
            width: 10px;

        }


        ::-webkit-scrollbar-thumb {
            background-repeat: no-repeat;
            background-color: rgb(43, 43, 117);
            border-radius: 6px;
        }

        html {
            scroll-behavior: smooth;

        }

        ::-webkit-scrollbar-thumb:hover {
            background-color: rgb(14, 2, 55);
        }

        :root {

            --primary-text-color: rgb(217, 219, 182);
            --seconary-text-color: rgb(215, 202, 196);
            --head-accent-color: rgb(14, 2, 55);
            --hover-head-accent-color: rgb(21, 21, 81);
            --back-color: rgb(243, 140, 4);
        }


        body {
            font-family: tahoma;

        }

        #img {
            width: 50px;


        }

        .div {
            width: 100%;
            display: flex;
            flex-direction: column;

        }

        .calci {
            width: 100%;
            display: flex;
            justify-content: end;
            padding: 20px 0px 0px 20px;

        }


        h1 #heading {
            text-align: center;
            margin-top: 40px;


        }

        .cont {
            align-self: center;
            display: flex;
            flex-direction: column;
            width: 90%;

        }


        .heading {
            width: 100%;
            user-select: none;
            margin: 10px 0px 0 0;
            padding: 20px;
            display: flex;
            border-radius: 10px;
            justify-content: space-between;
            background-color: var(--head-accent-color);
            color: var(--primary-text-color);

        }

        .boxw {

            width: 90%;
            align-self: center;
            background-color: var(--back-color);
            margin: 10px;
            border-radius: 20px;
            display: none;
        }

        .co {
            background-color: black;
        }

        .active {
            display: block;
        }

        .icon {
            position: relative;
            top: 10px;
            height: fit-content;

        }

        .color {
            background-color: var(--hover-head-accent-color);
            color: var(--seconary-text-color);
        }


        .input-div {
            padding: 20px;
            font-size: 30px;
            font-weight: bold;
            width: 70%;
            text-align: center;
            border-radius: 10px;
            margin: 10px 15% 0px 15%;

        }


        .inpt {
            border: 2px solid black;
            width: 100%;
            border-radius: 10px;
            text-align: center;
        }



        /* calculator */

        .img1 {
            user-select: none;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

        }


        .bound {
            display: flex;
            width: 100%;
            justify-content: flex-end;



        }

        .containe {
            display: none;
            width: 50%;
            position: relative;
            height: 100%;
            background-color: rgb(21, 21, 81);
            box-shadow: 15px 15px 20px rgba(0, 0, 0, 0.1),
                -15px -15px 20px #fffb;
            padding: 20px;
            border-radius: 10px;
        }


        .containe #result {
            height: 60px;
            position: relative;
            width: 95%;
            background-color: #fff;
            font-weight: 500;
            margin: 10px;
            user-select: text;
            text-align: end;
            border-radius: 10px;

            font-size: 2rem;
            border: 5px solid rgb(243, 140, 4);
            overflow-y: auto;
        }



        .containe #result::-webkit-scrollbar {
            width: 2px;
            height: 2px;
        }

        .inner {
            position: relative;
            width: 100%;
            height: 70%;
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-evenly;
        }


        .left {


            border-radius: 20px;
            box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.1),
                inset -5px -5px 20px #fff;
            position: relative;
            display: grid;
            padding: 10px;
            background-color: #fff;
            flex-wrap: wrap;

        }

        .left #left {
            position: relative;
            grid-column: span 5;

        }

        .right span {
            padding: 20px;
        }

        .right {


            border-radius: 20px;
            flex-wrap: wrap;

            display: grid;
            position: relative;
            padding: 10px;
            background-color: #fff;
        }

        .right #right {
            position: relative;
            grid-column: span 4;

        }

        #back {
            grid-column: span 2;
            background-color: rgb(148, 245, 3);
            border: 2px solid #87fc02;
            box-shadow: 5px 5px 10px rgba(91, 245, 2, 0.1),
                inset -5px -5px 20px #68e217;
        }


        #clear {
            background-color: red;
            border: 2px solid #fc0202;
            box-shadow: 5px 5px 10px rgba(243, 241, 241, 0.1),
                inset -5px -5px 20px #e21717;
            grid-column: span 2;
        }

        .inner span {
            position: relative;

            box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.1),
                inset -5px -5px 20px #fff;
            padding: 5px;
            margin: 5px;
            cursor: pointer;
            user-select: none;

            display: flex;
            justify-content: center;
            align-items: center;
            /* font-size: 1.2em; */
            border: 2px solid #fff;
            color: rgb(21, 21, 81);
            border-radius: 10px;

        }

        .inner span:hover {
            box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.1),
                inset -5px -5px 20px #ebe2e2;
            border: 2px solid #f37609;


        }

        @media screen and (max-width: 650px) {
            .right #right {
                grid-column: span 3;
            }

            .left #left {
                grid-column: span 3;
            }
        }

        @media screen and (max-width: 1320px) {
            .containe {
                width: 60%;
            }
        }

        @media screen and (max-width: 1130px) {
            .containe {
                width: 70%;
            }
        }

        @media screen and (max-width: 1150px) {
            .containe {
                width: 80%;
            }
        }

        @media screen and (max-width: 890px) {
            .containe {
                width: 90%;
            }
        }

        @media screen and (max-width: 725px) {
            .containe {
                width: 100%;
            }
        }


        footer {


            height: 50px;
        }
    </style>

</head>

<body style="display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100vh; background-color: black;">


    <!-- temprature -->
    <div class="heading  " id="heading2">
        <h1 id="heading">Temperature Convertor</h1>
        <div class="icon " id="icon2"><i class="fa-solid fa-sun  fa-2xl" style="color: #fa9200;"></i></div>
    </div>
    <div id="container2" class="boxw">
        <div class="input-div">
            <label>Celsius</label> <br>
            <input type="number" value="1" id="cl" class="inpt">

        </div>

        <div class="input-div">
            <label>Kelvin</label> <br>
            <input type="number" value="1000" id="kl" class="inpt">

        </div>

        <div class="input-div">
            <label>Fahrenheit</label> <br>
            <input type="number" value="1000000" id="ft" class="inpt">

        </div>

    </div>

    <script>

        // temperature

        const tog2 = document.getElementById('heading2');
        const cont2 = document.getElementById('container2');
        const ic2 = document.getElementById('icon2');

        tog2.addEventListener('click', function () {
            cont2.classList.toggle('active');
            tog2.classList.toggle('color');
            ic2.classList.toggle('fa-spin');
        });

        var cl = document.getElementById('cl');
        var kl = document.getElementById('kl');
        var ft = document.getElementById('ft');


        cl.addEventListener('input', function () {
            let cli = this.value;
            let kli = cli * 274.15;
            kl.value = kli;
            let fti = cli * 33.8;
            ft.value = fti;

        });
        kl.addEventListener('input', function () {
            let kli = this.value;

            let cli = kli * -272.15;
            cl.value = cli;
            let fti = kli * -457.87;
            ft.value = fti;

        });

        ft.addEventListener('input', function () {
            let fti = this.value;
            let kli = fti * 255.92777778;
            kl.value = kli;
            let cli = fti * -17.222222222;
            cl.value = cli;

        });


    </script>

</body>

</html>
