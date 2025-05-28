<script setup>
defineProps({
    id: String,
    InCountry: String,
    InCity: String,
    OutCountry: String,
    OutCity: String,
    InDate: Date,
    OutDate: Date,
    WeightCargo: String,
    AcceptanceCargo: String,
    Dogload: String,
    Money: Number,
    NdsInfo: String,
    PayInfo: String,
    Company: String,
    CompanyNumber: Number, 
    isOrderAccept: Boolean,
    OnClickAccept: Function,
})



const Onclick = () =>{
    alert(111)
}
</script>
<template>
        <div class="application">
            <p>{{ id }}</p>
            <div class="content-conteiner">
                <p>{{ InCountry }}. {{InCity}}</p>
                <span>{{ InDate }}</span>
            </div>
            <div class="content-conteiner">
                <p>{{ OutCountry }}. {{ OutCity }}</p>
                <span>{{ OutDate }}</span>
            </div>
            <div class="content-conteiner">
                <p>{{ WeightCargo }}т {{ AcceptanceCargo }}м {{ Dogload }}</p>
                <p style="color: #3E79BC;">паказать больше</p>
            </div>
            <div class="content-conteiner">
                <p>{{ Money }}RUB</p>
                <span>{{ NdsInfo }}, <br> {{ PayInfo }}</span>
            </div>
            <div class="content-conteiner">
                <p>{{ Company }}</p>
                <span>{{ CompanyNumber }}</span>
            </div>
            <button @click="Onclick">
      {{ isOrderAccept ? 'Заказ уже принят' : 'Принять заказ' }}
    </button>
        </div>


</template>

<style scoped>
.application{
    display: flex;
    gap: 5.5rem;
    border-bottom: 1px solid grey;
    margin-bottom: 1rem;
}

.content-conteiner{
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}
</style>
