

<template>
    <div id="app">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100..900;1,100..900&family=Sigmar+One&display=swap" rel="stylesheet">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">


        <img class="Greeting" src="../img/Fon.png" alt="">
        <header>
            <nav>
                <ul>
                    <li><a href="#">Обо мне</a></li>
                    <li><a href="#">Наставничевство</a></li>
                    <li><a href="#">Мероприятия</a></li>
                    <li><a href="#">Кейсы</a></li>
                    <li><a href="#">Отзывы</a></li>
                    <li><a href="#">Контакты</a></li> 
                    <li><a class="number" href="#">8-397-234-23-76</a></li>
                </ul>
                <img class="LineFour" src="../img/Line4.png" alt="#">
                    <img class="LineThree" src="../img/Line3.png" alt="#">
                        <img class="LineTwo" src="../img/Line2.png" alt="#">
                            <img class="lineOne" src="../img/Line1.png" alt="#">
                                <img class="LogoPhone" src="../img/PhoneLogo.png" alt="#">
                <img class="LogoAlex"  src="../img/logoAlex.png" alt="#">
                <img class="Menu"  src="../img/menu.png" alt="">
            </nav>
        </header>
        <main>
            
            <section>
                <h1 class="TextOne">СОЗДАЮ УСЛОВИЯ <br> ДЛЯ ВАШЕГО УСПЕХА</h1>
                <h1 class="TextLitle">
                Когда ваше время и энергия лучше сфокусированы,стремлее к новым <br>
                возможностям становится реалбностью, ваш успех от ваших действий</h1>
                <div class="BorderOne"></div>
                <h1 class="textCripto1">техник<br>для достижений целей</h1>
                <h1 class="textCripto2">увеличение личной<br>продуктивности</h1>
                <h1 class="NumberCripto1">130+</h1>
                <h1 class="NumberCripto2">250%</h1>
            </section>

            <section>
                <div class="TwoBtn">
                    <button class="btn1" @click="toggleElement"> 
                        <span class="span1">Записаться на консультацию</span>
                    </button>
                    <div class="lineBtn1">
                        <img  class="imgLineBtn1" src="../img/Vector2.png" alt="#">
                        <img  class="VectorLitle1" src="../img/VectorLitle.png" alt="#" >
                        <div class="BorderLineBtn1">
                        </div>
                    </div>


                    <button class="btn2" >
                        <span class="span2">Бесплатная консультация</span>
                    </button>
                    <div class="lineBtn2">
                        <img class="imgLineBtn2" src="../img/Vector.png" alt="#">
                        <img class="VectorLitle2"  src="../img/VectorLitle2.png" alt="#">
                        <div class="BorderLineBtn2">
                        </div>
                    </div>
                </div>
            </section>

            <section>
                <div class="mentorAlexS">
                    <img class="logoMentor" src="../img/mentor2.png" alt="#">
                </div>        
            </section>

            <section>
            <div class="Zayavka"  v-if="isELVisible">
                <div class="element"></div>
                
                <div class="ZayavkaVibor" id="ZayavkaViborID" >
                    <img class="crest" src="../img/Crest.png" alt="#" v-on:click="toggleElement2">
                    <h1 class="h1Zayavka">Закажите <br> обратный звонок</h1>
                    <div class="Hyston">
                    <input class="inputName" 
                    type="text" 
                    placeholder="ИМЯ" 
                    v-bind:value="inputValue"
                    v-on:input="inputV">
                    <img class="LineName" src="../img/NameLIne.png" alt="">
                    </div>

                    <div class="Hyston2">
                    <input class="inputPhone" type="tel" placeholder="ТЕЛЕФОН">
                    <img class="LinePhone" src="../img/PhoneLine.png" alt="">
                    </div>

                    <input class="CheckBox" type="checkbox">
                    <h1 class="TextCheckBox">Согласен на сохранение и обработку <br> 
                    персолальных данных</h1>
                        
                    
                    <button class="btnZayavka">
                    <img class="btnLogoZayavka" src="../img/Vector.png" alt="3">
                        <span class="btnZayavkaSpan">
                            Заказать обратный звонок
                        </span>
                        <div class="lineBtnZayavka"></div>
                    </button> 
                </div>
            </div>

            </section>

        </main>
    </div>

</template>

<script>


export default {
    data() {
        return {
            isELVisible: false,
            Greenburg: true,
            inputValue: '',
        }
    },
    methods: {
        toggleElement() {
            this.isELVisible = !this.isELVisible
        },
        toggleElement2() {
            if(this.Greenburg == true) {
                this.isELVisible = !this.isELVisible
                
            }
        }
    }
}


</script>

<style>

body {
    margin: 0;
    padding: 0;
    width: 100vw;
    height: 100vh;

    background: url(../img/City.png);
    background-size: cover;
    background-repeat: no-repeat;
    overflow-x: hidden;
}

nav {
    margin: -62% 0 0 29%;
    position: absolute;
    z-index: 3;
}

ul {
    display: flex;

}


li {
    margin-right: 30px;
    list-style-type: none;
}


a {
    text-decoration: none;
    color: rgba(255, 255, 255, 0.834);
    font-size: 14px;
    transition: 0.2s;
}

a:hover {
    color: white;
}

#app {
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    position: fixed;
    
}

.number {
    position: relative;

    margin:  0 0 0 140px;
    font-size: 16px;
}


.LogoAlex {
    position: absolute;
    margin: -4.8% 0 0 -32%;
}

.LogoPhone {
    position: absolute;
    margin: -5% 0 0 79%;
}

.Menu {
    position: absolute;
    margin: 0 0 0 -1000px;
}

.lineOne {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 -32%;

}

.LineTwo {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 10.5%;

}

.LineThree {
    position: absolute;
    height: 739px;
    background-size: cover;
    margin: -9.2% 0 0 55.5%;

}

.LineFour {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -9.2% 0 0 96.7%;
}

/* Оснвоная часть Main */

.TextOne {
    position: absolute;
    margin: -51% 0 0 10.2%;

    color: white;
    font-size: 50px;
    font-weight: 500;
    font-family: "Raleway", sans-serif;

}

.TextLitle {
    position: absolute;
    margin: -40% 0 0 12%;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    font-weight:100;
    font-family: "Raleway", sans-serif;
}

.TwoBtn {
    position: absolute;
    z-index: 3;
    margin: -34% 0 0 10.2%;
}

/* Кнопка консуль - 1 */
.btn1 {
    position: absolute;
    height: 68px;
    width: 340px;
    border: none;
    z-index: 3;  
    transition: 0.1s;

}

.btn1:hover {
    background-color: rgba(255, 255, 255, 0.745);
}

.span1 {
    margin-left: -30%;
    margin-top: -20%;
    font-size: 15px;
    font-weight: 600;
    font-family: "Raleway", sans-serif;
}


.lineBtn1 {
    position: absolute;
    z-index: 4;
    border-left: 2.4px solid #07305D;
    height: 70px;
    width: 20px;
    margin: -1px 0 0 38%;
}

.imgLineBtn1 {
    margin: 37px 0 0 36px;
}

.VectorLitle1 {
    position: absolute;
    margin: 0 0 0 -600px;
}

/* Кнопка консуль - 2 */
.btn2 {
    height: 68px;
    width: 340px;
    margin-left: 371.5px;
    background: none;
    border: 1px solid white;
    -webkit-text-fill-color: white;
    z-index: 3;
    transition: 0.1s;
}

.btn2:hover {
    background-color: rgba(255, 255, 255, 0.068);
}

.span2 {
    margin-left: -35%;
    font-family: "Raleway", sans-serif;
    font-weight: 500;
    font-size: 15px;
}


.lineBtn2 {
    position: absolute;
    z-index: 4;
    border-left: 2px solid rgb(254, 254, 254);
    height: 67px;
    width: 20px;
    margin: -68px 0 0 90%;
    
}

.imgLineBtn2 {
    margin: 33px 0 0 36px;

}

.VectorLitle2 {
    position: absolute;
    margin: 0 0 0 -900px;
}

/* ==================================== */

.BorderOne {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 29px;
    margin: -39.9% 0 0 10.2%;
    z-index: 3;
}

.BorderLineBtn1 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 120px;
    margin: 80px 0 0 -273px;
}

.BorderLineBtn2 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 120px;
    margin: 80px 0 0 -270.5px;
}


/*=============================================================== Нижняя часть =============================================================== */

.textCripto1 {
    position: absolute;

    margin: -300px 0 0 11.5%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.textCripto2 {

    position: absolute;

    margin: -300px 0 0 36.9%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.NumberCripto1 {
    position: absolute;

    margin: -365px 0 0 11.5%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}

.NumberCripto2 {
    position: absolute;
    margin: -365px 0 0 36.9%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}
/*=============================================================== Ментор!Скамер? =============================================================== */
.mentorAlexS {
    position: absolute;
    z-index: 3;
    margin: -830px 0 0 63%;
    display: block;
    max-width: 100%;
    height: auto;
}

/* =========================================================== Zayavka ========================================================== */

.Zayavka {
    position: absolute;
    display: flex;
    
    z-index: 3;
    width: 400px;
    height: 100%;
    background-color: #07305D;
    margin: -953px 0 0 1px;
}



.crest {
    position: absolute;
    margin: 20px 0 0 360px;
    width: 20px;
    height: 20px;
    color: white;
}


.btnLogoZayavka {
    position: absolute;
    margin: 10px 0 0 172px;

    width: 17px;
    height: 17px;
}

.h1Zayavka {
    position: absolute;
    margin: 80px 0 0 60px;

    font-weight: 600;
    font-family: "Raleway", sans-serif;
    font-size: 35px;
    color: white;
}

.LineName {
    position: absolute;
    width: 300px;
    margin: 280px 0 0 49px;
    
    
}

.LinePhone {
    position: absolute;
    width: 300px;
    margin: 120px 0 0 16px;

}


.btnZayavka {
    position:absolute;
    margin: 560px 0 0 48px;

    border: 1px solid white;
    background-color: #07315d00;
    width: 274px;
    height: 55px;
}

.btnZayavka:hover {
    background-color: rgba(255, 255, 255, 0.084);
}


.TextCheckBox {
    position: absolute;
    font-size: 13px;
    color: white;
    font-family: "Montserrat", sans-serif;
    font-weight: 300;
    margin: 450px 0 0 72px;                         
}


.CheckBox {
    position: absolute;
    margin: 455px 0 0 37px;
    width: 20px;
    height: 20px;
}




.btnZayavkaSpan {
    margin: 0 0 0 -58px;



    color: white;
    font-size: 14px;
    font-weight: 400;
    font-family: "Raleway", sans-serif;
}

.lineBtnZayavka {
    position: absolute;

    margin: -35px 0 0 210px;

    border-left: 1px solid white;
    height: 53px;
}


.Hyston2 {
    position: absolute;
    margin: 250px 0 0 33px;
}

.inputPhone {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 99px 0 0 13px;
}

.inputPhone::-webkit-input-placeholder {
    font-size: 14px;
}


.inputName {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 258px 0 0 48px;
}



/* ==================================================== Адаптив - Media 1 ====================================================*/
@media screen and (max-width: 1448px) {
    body {
    width: 1363px;
    margin: 0;
    padding: 0;
    width: 100vw;
    height: 100vh;

    background: url(../img/City.png);
    background-size: cover;
    background-repeat: no-repeat;
    }

    nav {
    margin: -64% 0 0 29%;
    position: absolute;
    z-index: 3;
    } 

    ul {
        display: flex;

    } 
    
    li {
    margin-right: 30px;
    list-style-type: none;
    }

    a {
    text-decoration: none;
    color: rgba(255, 255, 255, 0.834);
    font-size: 14px;
    }

    #app {
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    position: fixed;
    }

    .number {
    position: relative;

    margin:  0 0 0 140px;
    font-size: 16px;
    }

    .LogoAlex {
    position: absolute;
    margin: -5% 0 0 -32%;
    }

    .LogoPhone {
    position: absolute;
    margin: -5.5% 0 0 78%;
    height: 100%;
    }
    .Menu {
    position: absolute;
    margin: 0 0 0 -1000px;
}

.lineOne {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 -32%;

}

.LineTwo {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 10.5%;

}

.LineThree {
    position: absolute;
    height: 739px;
    background-size: cover;
    margin: -9.2% 0 0 55.5%;

}

.LineFour {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -9.2% 0 0 96.7%;
}

/* Оснвоная часть Main */

.TextOne {
    position: absolute;
    margin: -53% 0 0 9.6%;

    color: white;
    font-size: 50px;
    font-weight: 500;
    font-family: "Raleway", sans-serif;

}

.TextLitle {
    position: absolute;
    margin: -41.1% 0 0 11.5%;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    font-weight:100;
    font-family: "Raleway", sans-serif;
}

.TwoBtn {
    position: absolute;
    z-index: 3;
    margin: -35% 0 0 9.6%;
}

/* Кнопка консуль - 1 */
.btn1 {
    position: absolute;
    height: 68px;
    width: 340px;
    border: none;
    z-index: 3;  
    transition: 0.1s;

}

.btn1:hover {
    background-color: rgba(255, 255, 255, 0.745);
}

.span1 {
    margin-left: -30%;
    margin-top: -20%;
    font-size: 15px;
    font-weight: 600;
    font-family: "Raleway", sans-serif;
}


.lineBtn1 {
    position: absolute;
    z-index: 4;
    border-left: 2.4px solid #07305D;
    height: 70px;
    width: 20px;
    margin: -1px 0 0 38%;
}

.imgLineBtn1 {
    margin: 37px 0 0 36px;
}

/* Кнопка консуль - 2 */
.btn2 {
    height: 68px;
    width: 340px;
    margin-left: 373px;
    background: none;
    border: 1px solid white;
    -webkit-text-fill-color: white;
    z-index: 3;
    transition: 0.1s;
}

.btn2:hover {
    background-color: rgba(255, 255, 255, 0.068);
}

.span2 {
    margin-left: -35%;
    font-family: "Raleway", sans-serif;
    font-weight: 500;
    font-size: 15px;
}

.lineBtn2 {
    position: absolute;
    z-index: 4;
    border-left: 2px solid rgb(254, 254, 254);
    height: 67px;
    width: 20px;
    margin: -68px 0 0 90%;
    
}

.imgLineBtn2 {
    margin: 33px 0 0 36px;

}
/* ==================================== */

.BorderOne {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 29px;
    margin: -41% 0 0 9.6%;
    z-index: 3;
}

.BorderLineBtn1 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 120px;
    margin: 80px 0 0 -273px;
}

.BorderLineBtn2 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 120px;
    margin: 80px 0 0 -270.5px;
}


/*=============================================================== Нижняя часть =============================================================== */

.textCripto1 {
    position: absolute;

    margin: -300px 0 0 11.5%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.textCripto2 {

    position: absolute;

    margin: -300px 0 0 36.9%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.NumberCripto1 {
    position: absolute;

    margin: -365px 0 0 11.5%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}

.NumberCripto2 {
    position: absolute;
    margin: -365px 0 0 36.9%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}
/*=============================================================== Ментор!Скамер? =============================================================== */
.mentorAlexS {
    position: absolute;
    z-index: 3;
    margin: -830px 0 0 63%;
}


/* =========================================================== Zayavka ========================================================== */

.Zayavka {
    position: absolute;
    display: block;
    z-index: 3;
    width: 380px;
    height: 100%;
    background-color: #07305D;
    margin: -953px 0 0 1px;
}



.crest {
    position: absolute;
    margin: 15px 0 0 345px;
}


.btnLogoZayavka {
    position: absolute;
    margin: 10px 0 0 172px;

    width: 17px;
    height: 17px;
}

.h1Zayavka {
    position: absolute;
    margin: 80px 0 0 60px;

    font-weight: 600;
    font-family: "Raleway", sans-serif;
    font-size: 35px;
    color: white;
}

.LineName {
    position: absolute;
    width: 300px;
    margin: 280px 0 0 49px;
    
    
}

.LinePhone {
    position: absolute;
    width: 300px;
    margin: 120px 0 0 16px;

}


.btnZayavka {
    position:absolute;
    margin: 560px 0 0 48px;

    border: 1px solid white;
    background-color: #07315d00;
    width: 274px;
    height: 55px;
}

.btnZayavka:hover {
    background-color: rgba(255, 255, 255, 0.084);
}


.TextCheckBox {
    position: absolute;
    font-size: 13px;
    color: white;
    font-family: "Montserrat", sans-serif;
    font-weight: 300;
    margin: 450px 0 0 72px;                         
}


.CheckBox {
    position: absolute;
    margin: 455px 0 0 37px;
    width: 20px;
    height: 20px;
}

.btnZayavkaSpan {
    margin: 0 0 0 -58px;



    color: white;
    font-size: 14px;
    font-weight: 400;
    font-family: "Raleway", sans-serif;
}

.lineBtnZayavka {
    position: absolute;

    margin: -35px 0 0 210px;

    border-left: 1px solid white;
    height: 53px;
}


.Hyston2 {
    position: absolute;
    margin: 250px 0 0 33px;
}

.inputPhone {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 99px 0 0 13px;
}

.inputPhone::-webkit-input-placeholder {
    font-size: 14px;
}


.inputName {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 258px 0 0 48px;
}



}



/* ==================================================== Media - 2 ===================================================================*/

@media screen and (max-width: 1363px) {
    
    body {
        width: 1200px;
        margin: 0;
        padding: 0;
        width: 100vw;
        height: 100vh;
    
        background: url(../img/City.png);
        background-size: cover;
        background-repeat: no-repeat;
        overflow-x: hidden;
    }
    
    
    
    nav {
        margin: -68% 0 0 29%;
        position: absolute;
        z-index: 3;
    }
    
    ul {
        display: flex;
    
    }
    
    
    li {
        margin-right: 30px;
        list-style-type: none;
    }
    
    
    a {
        text-decoration: none;
        color: rgba(255, 255, 255, 0.834);
        font-size: 14px;
        transition: 0.2s;
    }
    
    a:hover {
        color: white;
    }
    
    #app {
        overflow: hidden;
        width: 100vw;
        height: 100vh;
        position: fixed;
        
    }
    
    .number {
        position: relative;
    
        margin:  0 0 0 140px;
        font-size: 16px;
    }
    
    
    .LogoAlex {
        position: absolute;
        margin: -4.8% 0 0 -32%;
    }
    
    .LogoPhone {
        position: absolute;
        margin: -5.5% 0 0 78%;
    }

    .Menu {
    position: absolute;
    margin: 0 0 0 -1000px;
}
    
    .lineOne {
        position: absolute;
        height: 100vh;
        background-size: cover;
        margin: -10% 0 0 -32%;
    
    }
    
    .LineTwo {
        position: absolute;
        height: 100vh;
        background-size: cover;
        margin: -10% 0 0 10.5%;
    
    }
    
    .LineThree {
        position: absolute;
        height: 739px;
        background-size: cover;
        margin: -9.2% 0 0 55.5%;
    
    }
    
    .LineFour {
        position: absolute;
        height: 100vh;
        background-size: cover;
        margin: -9.2% 0 0 96.7%;
    }
    
    /* Оснвоная часть Main */
    
    .TextOne {
        position: absolute;
        margin: -55% 0 0 8.4%;
    
        color: white;
        font-size: 55px;
        font-weight: 500;
        font-family: "Raleway", sans-serif;
    
    }
    
    .TextLitle {
        position: absolute;
        margin: -41.3% 0 0 10%;
        font-size: 15px;
        color: rgba(255, 255, 255, 0.5);
        font-weight:100;
        font-family: "Raleway", sans-serif;
    }
    
    .TwoBtn {
        position: absolute;
        z-index: 3;
        margin: -34% 0 0 8.5%;
    }
    
    /* Кнопка консуль - 1 */
    .btn1 {
        position: absolute;
        height: 68px;
        width: 340px;
        border: none;
        z-index: 3;  
        transition: 0.1s;
    
    }
    
    .btn1:hover {
        background-color: rgba(255, 255, 255, 0.745);
    }
    
    .span1 {
        margin-left: -30%;
        margin-top: -20%;
        font-size: 15px;
        font-weight: 600;
        font-family: "Raleway", sans-serif;
    }
    
    
    .lineBtn1 {
        position: absolute;
        z-index: 4;
        border-left: 2.4px solid #07305D;
        height: 70px;
        width: 20px;
        margin: -1px 0 0 38%;
    }
    
    .imgLineBtn1 {
        margin: 37px 0 0 36px;
    }
    
    /* Кнопка консуль - 2 */
    .btn2 {
        height: 68px;
        width: 340px;
        margin-left: 371.5px;
        background: none;
        border: 1px solid white;
        -webkit-text-fill-color: white;
        z-index: 3;
        transition: 0.1s;
    }
    
    .btn2:hover {
        background-color: rgba(255, 255, 255, 0.068);
    }
    
    .span2 {
        margin-left: -35%;
        font-family: "Raleway", sans-serif;
        font-weight: 500;
        font-size: 15px;
    }
    
    .lineBtn2 {
        position: absolute;
        z-index: 4;
        border-left: 2px solid rgb(254, 254, 254);
        height: 67px;
        width: 20px;
        margin: -68px 0 0 90%;
        
    }
    
    .imgLineBtn2 {
        margin: 33px 0 0 36px;
    
    }
    /* ==================================== */
    
    .BorderOne {
        position: absolute;
        border-left: 1px solid white;
        width: 1px;
        height: 31px;
        margin: -41% 0 0 8.4%;
        z-index: 3;
    }
    
    .BorderLineBtn1 {
        position: absolute;
        border-left: 1px solid white;
        width: 1px;
        height: 120px;
        margin: 65px 0 0 -275px;
    }
    
    .BorderLineBtn2 {
        position: absolute;
        border-left: 1px solid white;
        width: 1px;
        height: 120px;
        margin: 65px 0 0 -270.5px;
    }
    
    
    /*=============================================================== Нижняя часть =============================================================== */
    
    .textCripto1 {
        position: absolute;
    
        margin: -265px 0 0 9.9%;
        font-size: 16px;
        font-weight: 100;
        font-family: "Raleway", sans-serif;
        color: rgba(255, 255, 255, 0.61);
    }
    
    .textCripto2 {
    
        position: absolute;
    
        margin: -265px 0 0 37.5%;
        font-size: 16px;
        font-weight: 100;
        font-family: "Raleway", sans-serif;
        color: rgba(255, 255, 255, 0.61);
    }
    
    .NumberCripto1 {
        position: absolute;
    
        margin: -337px 0 0 9.8%;
        font-family: "Montserrat", sans-serif;
        font-size: 35px;
        font-weight: 600;
        color: rgb(255, 255, 255);
    
    }
    
    .NumberCripto2 {
        position: absolute;
        margin: -337px 0 0 37.3%;
        font-family: "Montserrat", sans-serif;
        font-size: 35px;
        font-weight: 600;
        color: rgb(255, 255, 255);
    
    }
    /*=============================================================== Ментор!Скамер? =============================================================== */
    .mentorAlexS {
        position: absolute;
        z-index: 3;
        margin: -830px 0 0 63%;
    }
    }

/* ======================================== Media - 3 ======================================== */
@media screen and (max-width: 1200px) {
    body {
    width: 1024px;
    margin: 0;
    padding: 0;
    width: 100vw;
    height: 100vh;

    background: url(../img/City.png);
    background-size: cover;
    background-repeat: no-repeat;
    }

    nav {
    margin: -77% 0 0 29%;
    position: absolute;
    z-index: 3;
    } 

    ul {
        display: flex;
        margin-left: -32px;

    } 
    
    li {
    position: relative;
    margin-right: 30px;
    list-style-type: none;
    


    }

    a {
    text-decoration: none;
    color: rgba(255, 255, 255, 0.834);
    font-size: 14px;
    }

    #app {
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    position: fixed;
    }

    .number {
    margin: 0 0 0 98px;
    font-size: 15px;
    }

    .LogoAlex {
    position: absolute;
    margin: -5.5% 0 0 -32%;
    }

    .LogoPhone {
    position: absolute;
    margin: -50px 0 0 76%;
    height: 100%;
    width: 50px;
    height: 50px;
    }

    .Menu {
    position: absolute;
    margin: 0 0 0 -1000px;
}

.lineOne {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 -32%;

}

.LineTwo {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 7.6%;

}

.LineThree {
    position: absolute;
    height: 739px;
    background-size: cover;
    margin: -12.9% 0 0 56.5%;

}

.LineFour {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -12.9% 0 0 96.7%;
}

/* Оснвоная часть Main */

.TextOne {
    position: absolute;
    margin: -66.5% 0 0 7.8%;

    color: white;
    font-size: 50px;
    font-weight: 500;
    font-family: "Raleway", sans-serif;

}

.TextLitle {
    position: absolute;
    margin: -53% 0 0 10%;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    font-weight:100;
    font-family: "Raleway", sans-serif;
}

.TwoBtn {
    position: absolute;
    z-index: 3;
    margin: -46% 0 0 7.9%;
}

/* Кнопка консуль - 1 */
.btn1 {
    position: absolute;
    height: 68px;
    width: 280px;
    border: none;
    z-index: 3;  
    transition: 0.1s;

}

.btn1:hover {
    background-color: rgba(255, 255, 255, 0.745);
}

.span1 {
    margin-left: -27%;
    margin-top: -20%;
    font-size: 14px;
    font-weight: 600;
    font-family: "Raleway", sans-serif;
}


.lineBtn1 {
    position: absolute;
    z-index: 4;
    border-left: 2.4px solid #07305D;
    height: 70px;
    width: 20px;
    margin: -1px 0 0 35.5%;
}

.imgLineBtn1 {
    margin: 37px 0 0 36px;
}

/* Кнопка консуль - 2 */
.btn2 {
    height: 68px;
    width: 280px;
    margin-left: 315px;
    background: none;
    border: 1px solid white;
    -webkit-text-fill-color: white;
    z-index: 3;
    transition: 0.1s;
}

.btn2:hover {
    background-color: rgba(255, 255, 255, 0.068);
}

.span2 {
    margin-left: -31%;
    font-family: "Raleway", sans-serif;
    font-weight: 500;
    font-size: 15px;
}

.lineBtn2 {
    position: absolute;
    z-index: 4;
    border-left: 2px solid rgb(254, 254, 254);
    height: 67px;
    width: 20px;
    margin: -68px 0 0 88.2%;
    
}

.imgLineBtn2 {
    margin: 33px 0 0 36px;

}
/* ==================================== */

.BorderOne {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 29px;
    margin: -52.9% 0 0 7.8%;
    z-index: 3;
}

.BorderLineBtn1 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 90px;
    margin: 70px 0 0 -215px;
}

.BorderLineBtn2 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 90px;
    margin: 70px 0 0 -212px;
}


/*=============================================================== Нижняя часть =============================================================== */

.textCripto1 {
    position: absolute;

    margin: -367px 0 0 9.3%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.textCripto2 {

    position: absolute;

    margin: -367px 0 0 35.8%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.NumberCripto1 {
    position: absolute;

    margin: -422px 0 0 9%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}

.NumberCripto2 {
    position: absolute;
    margin: -422px 0 0 35.7%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}
/*=============================================================== Ментор!Скамер? =============================================================== */
.mentorAlexS {
    position: absolute;
    z-index: 3;
    margin: -800px 0 0 63%;

    
    
}
} 



/* ==================================================== Адаптив - Media 4 ====================================================*/

@media screen and (max-width: 1024px) {
    body {
    width: 800px;
    margin: 0;
    padding: 0;
    width: 100vw;
    height: 100vh;

    background: url(../img/City.png);
    background-size: cover;
    background-repeat: no-repeat;
    overflow-x: hidden;
}



nav {
    margin: -90% 0 0 27%;
    position: absolute;
    z-index: 3;
}

ul {
    display: flex;
    padding: 0;

}


li {
    margin-right: 30px;
    list-style-type: none;
}


a {
    text-decoration: none;
    color: rgba(255, 255, 255, 0.834);
    font-size: 12px;
    transition: 0.2s;
}

a:hover {
    color: white;
}

#app {
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    position: fixed;
    
}

.number {
    margin:  5% 0 0 140px;
    font-size: 15px;
}


.LogoAlex {
    position: absolute;
    margin: -6% 0 0 -32%;
}

.LogoPhone {
    position: absolute;
    margin: -6.5% 0 0 75%;    
}

.Menu {
    position: absolute;
    margin: 0 0 0 -1000px;
}

.lineOne {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 -32%;

}

.LineTwo {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 10.5%;

}

.LineThree {
    position: absolute;
    height: 739px;
    background-size: cover;
    margin: -9.2% 0 0 55.5%;

}

.LineFour {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -9.2% 0 0 96.7%;
}

/* Оснвоная часть Main */

.TextOne {
    position: absolute;
    margin: -77% 0 0 3.8%;

    color: white;
    font-size: 42px;
    font-weight: 500;
    font-family: "Raleway", sans-serif;

}

.TextLitle {
    position: absolute;
    margin: -62.9% 0 0 6%;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    font-weight:100;
    font-family: "Raleway", sans-serif;
}

.TwoBtn {
    position: absolute;
    z-index: 3;
    margin: -56% 0 0 3.8%;
}

/* Кнопка консуль - 1 */
.btn1 {
    position: absolute;
    height: 68px;
    width: 285px;
    border: none;
    z-index: 3;  
    transition: 0.1s;

}

.btn1:hover {
    background-color: rgba(255, 255, 255, 0.745);
}

.span1 {
    margin-left: -29%;
    margin-top: -20%;
    font-size: 14px;
    font-weight: 600;
    font-family: "Raleway", sans-serif;
}


.lineBtn1 {
    position: absolute;
    z-index: 4;
    border-left: 2.4px solid #07305D;
    height: 70px;
    width: 20px;
    margin: -1px 0 0 36%;
}

.imgLineBtn1 {
    margin: 37px 0 0 36px;
}

/* Кнопка консуль - 2 */
.btn2 {
    height: 68px;
    width: 285px;
    margin-left: 316.5px;
    background: none;
    border: 1px solid white;
    -webkit-text-fill-color: white;
    z-index: 3;
    transition: 0.1s;
}

.btn2:hover {
    background-color: rgba(255, 255, 255, 0.068);
}

.span2 {
    margin-left: -35%;
    font-family: "Raleway", sans-serif;
    font-weight: 500;
    font-size: 15px;
}

.lineBtn2 {
    position: absolute;
    z-index: 4;
    border-left: 2px solid rgb(254, 254, 254);
    height: 67px;
    width: 20px;
    margin: -68px 0 0 88%;
    
}

.imgLineBtn2 {
    margin: 33px 0 0 36px;

}
/* ==================================== */

.BorderOne {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 29px;
    margin: -62.8% 0 0 3.8%;
    z-index: 3;
}

.BorderLineBtn1 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 110px;
    margin: 60px 0 0 -219.2px;
}

.BorderLineBtn2 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 110px;
    margin: 60px 0 0 -215.8px;
}


/*=============================================================== Нижняя часть =============================================================== */

.textCripto1 {
    position: absolute;

    margin: -383px 0 0 5.6%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.textCripto2 {

    position: absolute;

    margin: -383px 0 0 36.9%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.NumberCripto1 {
    position: absolute;

    margin: -455px 0 0 5.5%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}

.NumberCripto2 {
    position: absolute;
    margin: -458px 0 0 36.5%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}
/*=============================================================== Ментор!Скамер? =============================================================== */
.mentorAlexS {
    position: absolute;
    z-index: 3;
    margin: -830px 0 0 63%;
}
}

/* =================================================== Media - 5 ========================================================================== */


@media screen and (max-width: 800px) {
    
    body {
    width: 360px;
    margin: 0;
    padding: 0;
    width: 100vw;
    height: 100vh;

    background: url(../img/City.png);
    background-size: cover;
    background-repeat: no-repeat;
    overflow-x: hidden;
}



nav {
    margin: -116.7% 0 0 29%;
    position: absolute;
    z-index: 3;
    
}

ul {
    display: flex;

}


li {
    margin-right: 15px;
    list-style-type: none;
}


a {
    text-decoration: none;
    color: rgba(255, 255, 255, 0.834);
    font-size: 11px;
    transition: 0.2s;
    margin: 0;
}

a:hover {
    color: white;
}

#app {
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    position: fixed;
    
}

.number {
    position: relative;

    margin: 0 0 0 100px;
    font-size: 13px;
}


.LogoAlex {
    position: absolute;
    margin: -6.6% 0 0 -32%;
    width: 110px;
    height: 25px;
}

.LogoPhone {
    position: absolute;
    margin: -7.3% 0 0 74%;
    width: 35px;
    height: 35px;
}

.Menu {
    position: absolute;
    margin: 0 0 0 -1000px;
}

.lineOne {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 -32%;

}

.LineTwo {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -10% 0 0 4%;

}

.LineThree {
    position: absolute;
    height: 739px;
    background-size: cover;
    margin: -9.2% 0 0 61%;

}

.LineFour {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -9.2% 0 0 96.7%;
}

/* Оснвоная часть Main */

.TextOne {
    position: absolute;
    margin: -100% 0 0 6.7%;

    color: white;
    font-size: 43px;
    font-weight: 500;
    font-family: "Raleway", sans-serif;

}

.TextLitle {
    position: absolute;
    margin: -81.2% 0 0 9%;
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    font-weight:100;
    font-family: "Raleway", sans-serif;
}

.TwoBtn {
    position: absolute;
    z-index: 3;
    margin: -70% 0 0 6.8%;
}

/* Кнопка консуль - 1 */
.btn1 {
    position: absolute;
    height: 54px;
    width: 185px;
    border: none;
    z-index: 3;  
    transition: 0.1s;

}

.btn1:hover {
    background-color: rgba(255, 255, 255, 0.745);
}

.span1 {
    margin-left: -30%;
    margin-top: -20%;
    font-size: 15px;
    font-weight: 600;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0);
}

.span1:after {
    content: 'Записаться';
    color: black;
    margin: 0 0 0 -250px;
}


.lineBtn1 {
    position: absolute;
    z-index: 4;
    border-left: 2.4px solid #07305D;
    height: 55px;
    width: 20px;
    margin: -1px 0 0 33%;
}

.imgLineBtn1 {
    margin: 33px 0 0 34px;
    width: 18px;
    height: 18px;
}

/* Кнопка консуль - 2 */
.btn2 {
    height: 54px;
    width: 185px;
    margin-left: 200px;
    background: none;
    border: 1px solid white;
    color: rgba(240, 248, 255, 0);
    z-index: 3;
    transition: 0.1s;
}

.btn2:hover {
    background-color: rgba(98, 55, 55, 0.068);
}

.span2  {
    position: absolute;
    margin-left: -25%;
    font-family: "Raleway", sans-serif;
    -webkit-text-fill-color: rgba(237, 237, 237, 0);
    font-weight: 500;
    font-size: 14px;

}

.span2:after {
    position: absolute;
    content: 'Заказать звонок';
    margin: -8px 0 0 -165px;
    -webkit-text-fill-color: rgb(255, 255, 255);
}

.lineBtn2 {
    position: absolute;
    z-index: 4;
    border-left: 2px solid rgb(254, 254, 254);
    height: 54px;
    width: 20px;
    margin: -54px 0 0 85%;
    
}

.imgLineBtn2 {
    margin: 30px 0 0 34px;
    width: 18px;
    height: 18px;

}
/* ==================================== */

.BorderOne {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 29px;
    margin: -81% 0 0 6.7%;
    z-index: 3;
}

.BorderLineBtn1 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 100px;
    margin: 60px 0 0 -130px;
}

.BorderLineBtn2 {
    position: absolute;
    border-left: 1px solid white;
    width: 1px;
    height: 100px;
    margin: 60px 0 0 -129px;
}


/*=============================================================== Нижняя часть =============================================================== */

.textCripto1 {
    position: absolute;

    margin: -385px 0 0 9%;
    font-size: 14px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.textCripto2 {

    position: absolute;

    margin: -385px 0 0 34%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0.61);
}

.NumberCripto1 {
    position: absolute;

    margin: -450px 0 0 8%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}

.NumberCripto2 {
    position: absolute;
    margin: -450px 0 0 33.5%;
    font-family: "Montserrat", sans-serif;
    font-size: 35px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}
/*=============================================================== Ментор!Скамер? =============================================================== */
.mentorAlexS {
    position: absolute;
    z-index: 3;
    margin: -850px 0 0 63%;
}

.img {
    width: 200px;
    height: 200px;
}

/* =========================================================== Zayavka ========================================================== */

.Zayavka {
    position: absolute;
    /* display: none; */
    z-index: 3;
    width: 300px;
    height: 100%;
    background-color: #07305D;
    margin: -953px 0 0 1px;
}

.crest {
    position: absolute;
    margin: 13px 0 0 268px;
}


.btnLogoZayavka {
    position: absolute;
    margin: 10px 0 0 144.3px;

    width: 16px;
    height: 16px;
}

.h1Zayavka {
    position: absolute;
    margin: 110px 0 0 50px;

    font-weight: 600;
    font-family: "Raleway", sans-serif;
    font-size: 25px;
    color: white;
}

.LineName {
    position: absolute;
    width: 220px;
    margin: 280px 0 0 49px;
    
    
}

.LinePhone {
    position: absolute;
    width: 220px;
    margin: 120px 0 0 16px;

}


.btnZayavka {
    position:absolute;
    margin: 560px 0 0 48px;

    border: 1px solid white;
    background-color: #07315d00;
    width: 223px;
    height: 50px;
}

.btnZayavka:hover {
    background-color: rgba(255, 255, 255, 0.084);
}


.TextCheckBox {
    position: absolute;
    font-size: 11px;
    color: white;
    font-family: "Montserrat", sans-serif;
    font-weight: 300;
    margin: 452px 0 0 72px;                         
}


.CheckBox {
    position: absolute;
    margin: 455px 0 0 39px;
    width: 19px;
    height: 19px;
}

.btnZayavkaSpan {
    margin: 0 0 0 -50px;

    color: white;
    font-size: 12.7px;
    font-weight: 400;
    font-family: "Raleway", sans-serif;
}

.lineBtnZayavka {
    position: absolute;

    margin: -32px 0 0 165px;
    border-left: 1px solid white;
    height: 49px;
}


.Hyston2 {
    position: absolute;
    margin: 250px 0 0 33px;
}

.inputPhone {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 99px 0 0 13px;
}

.inputPhone::-webkit-input-placeholder {
    font-size: 14px;
}


.inputName {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 258px 0 0 48px;
}

}


/*=============================================================== Media - 6 =============================================================== */

@media screen and (max-width: 360px)  {
    body {
    margin: 0;
    padding: 0;
    width: 100vw;
    height: 100vh;

    background: url(../img/City.png);
    background-size: cover;
    background-repeat: no-repeat;
    overflow-x: hidden;
}



nav {
    position: absolute;
    z-index: 3;
}

ul {
    display: flex;

}


li {
    margin-right: 30px;
    list-style-type: none;
}


a {
    text-decoration: none;
    color: rgba(255, 255, 255, 0);
    font-size: 14px;
    transition: 0.2s; 
}

a:hover {
    color: white;
}

#app {
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    position: fixed;
    
}

.number {
    position: relative;

    margin:  0 0 0 140px;
    font-size: 16px;
}


.LogoAlex {
    position: absolute;
    margin: -564px 0 0 -12%;
    Width: 118px;
    Height: 25px;
    
}

.LogoPhone {
    position: absolute;
    margin: -578px 0 0 28%;
    width: 50px;
    height: 50px;
}

.Menu {
    position: absolute;
    margin: -578px 0 0 134px;
    width: 50px;
    height: 50px;
    color: white;
}

.lineOne {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -86.5% 0 0 -12%;

}

.LineTwo {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -86.5% 0 0 5%;

}

.LineThree {
    position: absolute;
    height: 739px;
    background-size: cover;
    margin: -86.5% 0 0 18.9%;

}

.LineFour {
    position: absolute;
    height: 100vh;
    background-size: cover;
    margin: -86.5% 0 0 35%;
}

/* Оснвоная часть Main */

.TextOne {
    position: absolute;
    margin: -230% 0 0 6.5%;

    color: white;
    font-size: 27px;
    font-weight: 500;
    font-family: "Raleway", sans-serif;
    line-height: 38px;
}

.TextOne:after {
    content: "/AAA";
    color:rgba(255, 255, 255, 0) ;
}

.TextLitle {
    position: absolute;
    margin: -185% 0 0 30px;
    font-size: 13px;
    color: rgba(255, 255, 255, 0);
    font-weight:100;
    font-family: "Raleway",sans-serif;
    display: flex;
}


.TextLitle:after {
    position: absolute;
    content: 'Ваш успех зависит от ваших действий';
    color: rgba(255, 255, 255, 0.5);
    overflow: wrap;
}



.TwoBtn {
    position: absolute;
    z-index: 3;
    margin: -150% 0 0 0%;
}

/* Кнопка консуль - 1 */
.btn1 {
    position: absolute;
    height: 38px;
    width: 157px;
    border: none;
    z-index: 3;  
    transition: 0.1s;
    margin: -50px 0 0 20px;
}

.btn1:hover {
    background-color: rgba(255, 255, 255, 0.745);
}

.span1 {
    margin-left: -36%;
    margin-top: -21%;
    font-size: 14px;
    font-weight: 600;
    font-family: "Raleway", sans-serif;
}

.span1:after {
    position: absolute;
    margin: -8px 0 0 -107px ;
}


.lineBtn1 {
    position: absolute;
    z-index: 4;
    border-left: 2.4px solid #07305D;
    height: 38px;
    width: 20px;
    margin: -50px 0 0 78.4%;
}

.imgLineBtn1 {
    margin: 16px 0 0 -300px;
    width: 15px;
    height: 15px;

    color: rgba(7, 48, 93, 1);
    
}

.VectorLitle1 {
    position: absolute;
    margin: 22px 0 0 305px;
}

/* Кнопка консуль - 2 */
.btn2 {
    height: 38px;
    width: 157px;
    margin-left: 20px;
    background: none;
    border: 1px solid white;
    -webkit-text-fill-color: white;
    z-index: 3;
    transition: 0.1s;
}

.btn2:hover {
    background-color: rgba(255, 255, 255, 0.068);
}

.span2 {
    margin-left: -35%;
    font-family: "Raleway", sans-serif;
    font-weight: 500;
    font-size: 13px;
}

.span2:after {
    position: absolute;
    margin: -23px 0 0 -120px ;
}


.lineBtn2 {
    position: absolute;
    z-index: 4;
    border-left: 2px solid rgb(254, 254, 254);
    height: 38px;
    width: 20px;
    margin: -38px 0 0 78.8%;
    
}

.imgLineBtn2 {
    margin: 33px 0 0 -200px;

}

.VectorLitle2 {
    position: absolute;
    margin: 20.7px 0 0 200.8px;
}
/* ==================================== */

.BorderOne {
    position: absolute;
    border-left: 1px solid  rgba(255, 255, 255, 0.61);
    width: 1px;
    height: 29px;
    margin: -185% 0 0 5.7%;
    z-index: 3;
}

.BorderLineBtn1 {
    position: absolute;
    border-left: 1px solid  rgba(255, 255, 255, 0.61);
    width: 1px;
    height: 45px;
    margin: 160px 0 0 -120px;
}

.BorderLineBtn2 {
    position: absolute;
    border-left: 1px solid rgba(255, 255, 255, 0.61);
    width: 1px;
    height: 45px;
    margin: 90px 0 0 -1.6px;
}


/*=============================================================== Нижняя часть =============================================================== */

.textCripto1 {
    position: absolute;

    margin: -385px 0 0 -36%;
    font-size: 15px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0);
}

.textCripto1:after {
    content: 'техник';
    color: rgba(255, 255, 255, 0.61);
}

.textCripto2 {
    position: absolute;
    z-index: 4;

    margin: -378px 0 0 17%;
    font-size: 12px;
    font-weight: 100;
    font-family: "Raleway", sans-serif;
    color: rgba(255, 255, 255, 0);
}

.textCripto2:after {
    content: 'продуктивности';
    color: rgba(255, 255, 255, 0.61);
}


.NumberCripto1 {
    position: absolute;

    margin: -395.7px 0 0 9%;
    font-family: "Montserrat", sans-serif;
    font-size: 20px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}

.NumberCripto2 {
    position: absolute;
    margin: -398px 0 0 42%;
    font-family: "Montserrat", sans-serif;
    font-size: 20px;
    font-weight: 600;
    color: rgb(255, 255, 255);

}
/*=============================================================== Ментор!Скамер? =============================================================== */
.mentorAlexS {
    position: absolute;
    z-index: 3;
    margin: -780px 0 0 44.5%;
}

.logoMentor {
    height: 480px;
}


/* =========================================================== Zayavka ========================================================== */

.Zayavka {
    position: absolute;
    /* display: none; */
    z-index: 3;
    width: 380px;
    height: 100%;
    background-color: #07305D;
    margin: -953px 0 0 1px;
    z-index: 5;
}

.crest {
    position: absolute;
    margin: 22px 0 0 319px;
}


.btnLogoZayavka {
    position: absolute;
    margin: 10px 0 0 172px;

    width: 17px;
    height: 17px;
}

.h1Zayavka {
    position: absolute;
    margin: 100px 0 0 40px;

    font-weight: 500;
    font-family: "Raleway", sans-serif;
    font-size: 25px;
    color: white;
}

.LineName {
    position: absolute;
    width: 270px;
    margin: 250px 0 0 40px;
    
    
}

.LinePhone {
    position: absolute;
    width: 270px;
    margin: 79px 0 0 8px;

}


.btnZayavka {
    position:absolute;
    margin: 460px 0 0 43px;

    border: 1px solid white;
    background-color: #07315d00;
    width: 274px;
    height: 55px;
}

.btnZayavka:hover {
    background-color: rgba(255, 255, 255, 0.084);
}


.TextCheckBox {
    position: absolute;
    font-size: 13px;
    color: white;
    font-family: "Montserrat", sans-serif;
    font-weight: 300;
    margin: 365px 0 0 72px;                         
}


.CheckBox {
    position: absolute;
    margin: 370px 0 0 41px;
    width: 16px;
    height: 16px;
    
}

.btnZayavkaSpan {
    margin: 0 0 0 -58px;

    color: white;
    font-size: 14px;
    font-weight: 400;
    font-family: "Raleway", sans-serif;
}

.lineBtnZayavka {
    position: absolute;

    margin: -35px 0 0 210px;

    border-left: 1px solid white;
    height: 53px;
}


.Hyston2 {
    position: absolute;
    margin: 250px 0 0 33px;
}

.inputPhone {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 58px 0 0 8px;
}

.inputPhone::-webkit-input-placeholder {
    font-size: 14px;
}


.inputName {
    position: absolute;
    border: none;
    background: none;
    outline: none;
    color: 
    rgba(255, 255, 255, 0.8);

    margin: 230px 0 0 42px;
}

}
</style>