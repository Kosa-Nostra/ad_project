<template>
  <v-container>
  <v-row justify="center">
    <v-col cols="12" xs="12">
         <v-carousel>
          <v-carousel-item v-for="ad in ads" :key="ad.id" :src="ad.src" cover>
            <div class="ad-link">
               <v-btn class="error" :to="'/ad/' + ad.id">
                 {{ ad.title }}
               </v-btn>
             </div>
          </v-carousel-item>
         </v-carousel>
       </v-col>
     </v-row>
   </v-container>
   <v-container>
     <v-row justify="center">
       <v-col cols="12" xs="12">
         <v-card>
           <v-img height="200px"></v-img>
           <v-card-title primary-title>
             <div>
               <h3 class="headline mb0">Здесь будет заголовок</h3>
               <div>Здесь будет описание</div>
             </div>
           </v-card-title>
           <v-card-actions>
             <v-spacer></v-spacer>
             <v-btn text>Open</v-btn>
             <v-btn raised color="primary">
               Buy
             </v-btn>
           </v-card-actions>
         </v-card>
       </v-col>
     </v-row>
   </v-container>
 </template>
 
 <script>
 export default {
   data() {
     return {
     }
   }
 }
 </script>

<style scoped>
.ad-link {
  position:absolute;
  bottom: 50px;
  left:50%;
  background: rgb(0,0,0,0.5);
  transform: translate(-50%,0);
  padding: 5px 15px;
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;
}
</style>
