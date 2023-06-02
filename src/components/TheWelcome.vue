<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>About Me</template>

    Halo, nama saya Riska Putri Anggraini. Saya dari Purworejo, Indonesia.
    Saya seorang mahasiswa Sarjana Sistem Telekomunikasi di Universitas Pendidikan Indonesia yang belajar tentang networking, data science, cyber security, dan lain-lain. Saat ini sedang mengikuti kegiatan MSIB di PT. Stechoq Robotika Indonesia yang berlokasi di Sleman, Yogyakarta.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Project</template>

    <h3>1. Project resume Perkembangan teknologi 5G</h3>
    
    <h3>2. Buku Elektronika "Pendekatan Praktikum Real dan Virtual Menggunakan PhET Simulations" </h3>
    <h3>3. Analisis Op-Amp LM741 pada Komparator dengan Software Elektronics Workbench </h3>
    <h3>4. Analisis Dioda pada Rangkaian Rectifier dengan Software Elektronics Workbench </h3>
    <br />
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Pengalaman</template>

  <h2>1. PT. Yogyakarta Tugu Televisi</h2>
Divisi Master Control yang mempelajari CG (Character generic), Audio, Switch, dan Server.
<h2>2. Unit Produksi Multimedia SMKN 2 Purworejo</h2>
Mengelola unit produksi yang difasilitasi oleh SMK N 2 seperti cetak foto, Cetak Mug Custon, gantungan kunci, dokumentasi perpisahan dll.
  </WelcomeItem>


</template>
