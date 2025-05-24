<script setup>
 import ApplicationCargo from './Application-cargo.vue'
</script>

<template>
    <ApplicationCargo id="123" InCountry="RU" InCity="Москва" InDate="12.08.25" OutCountry="EN" OutCity="Лондон" OutDate="25.09.25" WeightCargo="29" AcceptanceCargo="15" Dogload="Отдельная Машина" Money="400000" NdsInfo="Без НДС" PayInfo="Без предоплат" Company="ООО техномир" -company-number="+7(999)999 99-99" isOrderAccept="false"/>
    <ApplicationCargo :isOrderAccept="true"/>
    <ApplicationCargo :isOrderAccept="false"/>
    <ApplicationCargo :isOrderAccept="false"/>
    <ApplicationCargo :isOrderAccept="true"/>
</template>

<style scoped>

</style>