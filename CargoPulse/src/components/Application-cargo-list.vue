<script setup>
 import { onMounted, ref } from 'vue';
 import axios from "axios";
 import ApplicationCargo from './Application-cargo.vue'
defineProps({
    items: Array
})

const items = ref([]);

onMounted ( async () => {
    try{
        const { data } = await axios.get('https://197cc3b80ab66ad1.mokky.dev/cargoinfo')

        items.value = data;
        
    } catch (err) {
        console.log(err);
        
    }

})


const OnClickAccept = () => {
    alert('добавить!')
}

</script>

<template>
    <!-- <ApplicationCargo id="123" InCountry="RU" InCity="Москва" InDate="12.08.25" OutCountry="EN" OutCity="Лондон" OutDate="25.09.25" WeightCargo="29" AcceptanceCargo="15" Dogload="Отдельная Машина" Money="400000" NdsInfo="Без НДС" PayInfo="Без предоплат" Company="ООО техномир" -company-number="+7(999)999 99-99" :isOrderAccept="false" :OnClickAccept="OnClickAccept"/>   -->
     <ApplicationCargo v-for="item in items" 
     :key="item.id"
     :id="item.id" 
     :InCountry="item.InCountry" 
     :InCity="item.InCity" 
     :InDate="item.InDate" 
     :OutCountry="item.OutCountry" 
     :OutCity="item.OutCity" 
     :OutDate="item.OutDate" 
     :WeightCargo="item.WeightCargo" 
     :AcceptanceCargo="item.AcceptanceCargo" 
     :Dogload="item.Dogload" 
     :Money="item.Money" 
     :NdsInfo="item.NdsInfo" 
     :PayInfo="item.PayInfo" 
     :Company="item.Company" 
     :CompanyNumber="item.CompanyNumber"
      :isOrderAccept="false"
       :OnClickAccept="OnClickAccept"/> 
  
</template>

<style scoped>

</style>