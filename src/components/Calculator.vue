<script>
export default {
   data() {
      return {
         num1: null,
         num2: null,
         calType: "",
         result: null,
      };
   },
   methods: {
      cal() {
         switch (this.calType) {
            case "1":
               this.result = this.num1 + this.num2;
               break;
            case "2":
               this.result = this.num1 - this.num2;
               break;
            case "3":
               this.result = this.num1 * this.num2;
               break;
            case "4":
               this.result = this.num1 / this.num2;
               break;
         }
      },
   },
   mounted() {},
};
</script>

<template>
   <div class="calculator">
      <h1>計算機</h1>
      <div class="cal d-flex">
         <input class="input" type="number" v-model="num1" />
         <select v-model="calType">
            <option value="1">+</option>
            <option value="2">-</option>
            <option value="3">*</option>
            <option value="4">/</option>
         </select>
         <input class="input" type="number" v-model="num2" />
         <p>{{ result }}</p>
      </div>
      <button type="button" @click="cal">計算</button>
   </div>
</template>

<style lang="scss" scoped>
.calculator {
   height: 100vh;
   display: flex;
   flex-direction: column;
   justify-content: center;
   align-items: center;
   .input {
      margin: 0 1rem;
   }
   p {
      text-align: center;
      margin: 0;
   }
   button {
      margin-top: 1rem;
   }
}
</style>
