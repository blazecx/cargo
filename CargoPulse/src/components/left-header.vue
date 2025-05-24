<template>
    <div class="conteiner">
        <div class="logo">
            <img src="../assets/img/logo.svg" alt="" class="logoimg">
            <p class="logotext">CARGO <span>PULSE</span></p>
        </div>
        <nav>
            <div class="conteiner-nav"><a href="#">Профиль</a></div>
            <div class="conteiner-nav"><a href="#">Грузы</a></div>
            <div class="conteiner-nav"><a href="#">Транспорт</a></div>
            <div class="conteiner-nav"><a href="#">Заявки</a></div>
            <div class="conteiner-nav"><a href="#">Компании</a></div>
            <div class="conteiner-nav"><a href="#">Новости</a></div>
        </nav>
    </div>
</template>

<style scoped>
.conteiner{
    background-color: #2D303A;
    width: 23rem;
    height: 100vh;
    box-shadow: 0px 4px 7px rgba(204, 158, 248, 0.3);
    padding-top: 4rem;
    display: flex;
    flex-direction: column;
    gap: 8rem;
    border-radius: 0rem 2rem 2rem 0rem;
    margin-right: 2rem;
}

.logo{
    display: flex;
    align-items: center;
    margin-left: 2rem;
}

.logo .logotext, span{
    font-family: 'Anton', sans-serif;
    font-size: 2rem;
}

.logo .logotext{
    color: #90989B;
    margin-left: 1rem;
}

.logo span{
    color: #EAEAEA;
}

a{
    color: #EAEAEA;
    transition: color 0.3s ease
}


nav .conteiner-nav{
    width: 22rem;
    height: 3.3rem;
    display: flex;
    align-items: center;
    border-radius: 0rem 0.5rem 0.5rem 0rem;
    padding-left: 3rem;
}

nav .conteiner-nav:hover{
    background-color: #847A71;
}

nav .conteiner-nav:hover a{
    color: #0F181F;
}

nav .conteiner-nav:active{
    background-color: #847A71;
}

</style>
