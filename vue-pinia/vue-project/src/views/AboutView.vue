<script setup>
import { useCountOptionStore} from '@/stores/countOption';
import { useCountSetupStore} from '@/stores/countSetup';
import { storeToRefs} from 'pinia'; // 비구조화 할당
const optionStore = useCountOptionStore();
const setupStore = useCountSetupStore();

const {num, doubleNum} = storeToRefs(optionStore); // setupStore 도 가능 

console.log(optionStore.num);
console.log(setupStore.doubleNumnum);
optionStore.increment();
setupStore.getJSON('https://jsonplaceholder.typicode.com/posts');
console.log(num, doubleNum);

</script>

<template>
  <h1>About View</h1>
</template>
