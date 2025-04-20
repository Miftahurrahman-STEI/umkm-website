<script setup>
import CardMinuman from '../components/cards/MinumanVue.vue'
</script>

<template>
  <main class="w-full h-[651px] flex justify-center items-center">
    <div class="m-20">
        <div class="flex justify-around items-center m-40">
            <div class="w-full h-full">
              <h1 class="font-medium text-4xl mb-4 whitespace-normal">Pastrylife Manisnya Setiap Sudut Rumah</h1>
              <p class="text-gray-400">
                Enak dimulai hari ini, Pastry kami dibuat dengan
                kualitas yang tinggi dengan Resep turun temurun
              </p>
              <div class="mt-[43px]">
                <div>
                  <a href="#" class="flex justify-center items-center w-[198px] h-[57px] bg-[#704FE6] text-white font-medium text-xl rounded-full gap-[9px]">
                    Get Started
                    <div class="rounded-full w-[30px] h-[30px] bg-white flex justify-center items-center">
                      <img src="../assets/icon/right-arrow.png" alt="arrow" />
                    </div>
                  </a>
                </div>
              </div>
            </div>
            <div>
              <img src="../assets/icon/image 3.png" alt="icon"/>
            </div>
          </div>
      </div>
  </main>
  <div class="w-full h-screen">
    <div class="flex flex-col justify-center items-center text-center">
        <h2 class="text-center text-3xl font-bold text-black p-4">
          Rekomendasi Makanan Dan Minuman Untuk Setiap Suasana Hati
        </h2>
        <p>Kami memiliki menu yang disukai banyak orang </p>
        <div class="flex justify-center items-center w-[200px] h-[40px] bg-gray-100 gap-4 text-center rounded-full mt-4">
          <div class="flex justify-center items-center w-[100px] h-[27px] bg-white rounded-full">
            <a href="#">
              Makanan
            </a>
          </div>
          <div class="flex justify-center items-center w-[70px] h-[27px] bg-transparent rounded-full">
            <a href="#">Minuman</a>
          </div>
        </div>
    </div>

      <CardMinuman/>
  </div>
</template>

<style scoped>
</style>
