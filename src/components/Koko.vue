<template>
<div>
    <div class="inf">
      <div class="card" @click="tampilkanData('PUBG', '  adalah gim battle royale yang dirancang oleh Brendan Greene. Secara resmi, gim ini dirilis secara global pada bulan Maret 2018. Awalnya, PUBG tersedia untuk platform PC Windows melalui Steam, dan kemudian tersedia untuk Xbox One dan perangkat mobile seperti sekarang ini. Dalam gameplay-nya, ada 100 pemain yang bertempur untuk menjadi pemenang. ')">
        <span></span>
        <div class="content">
          <img src="/pubg.jpeg" alt="gambar" class="gambar">
        </div>
      </div>

      <div class="card" @click="tampilkanData('Mobile Legends', 'Mobile Legends: Bang Bang atau ML merupakan game MOBA yang dirilis oleh Moontoon. Game ini bisa dimainkan di ponsel Android maupun IOS. Dalam game MOBA ini akan ada 10 pemain yang akan dibagi menjadi 2 tim. ')">
        <span></span>
        <div class="content">
          <img src="/ml.webp" alt="gambar" class="gambar">
        </div>
      </div>

      <div class="card" @click="tampilkanData('Free Fire', 'Gameplay Free Fire adalah dimana semua pemain dikerahkan dengan pesawat dan wajib melakukan terjun bebas. Tiap pemain juga harus mencari senjata dan peralatan medis ketika dikirim untuk bertarung melawan pemain lain dan bertahan hidup. Di tengah permainan nanti akan ada pesawat yang lewat dan meluncurkan airdrop dalam bentuk kotak besar berisi rompi anti peluru, helm, senjata khusus seperti AWM, Groza , M79 dan M249 ataupun senapan mesin. Menemukan airdrop juga tidak sulit.')">
        <span></span>
        <div class="content">
          <img src="/ff.jpeg" alt="gambar" class="gambar">
        </div>
      </div>

      <div class="card" @click="tampilkanData('Clash of Clans', 'adalah permainan video strategi seluler freemium yang dikembangkan dan diterbitkan oleh pengembang permainan Finlandia, Supercell. Permainan ini dirilis untuk platform iOS pada 2 Agustus 2012, dan di Google Play untuk Android pada 7 Oktober 2013. Permainan ini berlatarkan tema fantasi dunia persistent dimana pemainnya adalah kepala desa. Clash of Clans menugaskan pemain untuk membangun desa mereka sendiri menggunakan sumber daya yang diperoleh dari menyerang desa pemain lain atau memproduksinya di desa sendiri')">
        <span></span>
        <div class="content">
          <img src="/coc.jpeg" alt="gambar" class="gambar">
        </div>
      </div>
    </div>

    <div v-if="dataTerpilih" class="tampilan-data">
      <h2>{{ dataTerpilih.judul }}</h2>
      <p>{{ dataTerpilih.informasi }}</p>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      dataTerpilih: null
    };
  },
  methods: {
    tampilkanData(judul, informasi) {
      if (this.dataTerpilih && this.dataTerpilih.judul === judul) {
        this.dataTerpilih = null;
      } else {
        this.dataTerpilih = { judul, informasi };
      }
    }
  }
};
</script>


