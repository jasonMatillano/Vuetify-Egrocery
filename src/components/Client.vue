<template>
  <v-row class="mt-10 mb-5">
    <v-col
      cols="12"
      xs="12"
      sm="6"
      md="4"
      v-for="(client, i) in clients"
      :key="i"
    >
      <v-card class="elevation-16 mx-auto" width="300">
        <v-list subheader two-line>
          <v-list-item>
            <v-list-item-avatar>
              <v-img :src="client.img"></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>{{ client.title }}</v-list-item-title>

              <v-list-item-subtitle>{{ client.subtitle }}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-card-text>
          <div class="mt-n7">
            <v-rating
              v-model="client.rating"
              color="yellow darken-3"
              background-color="grey darken-1"
              empty-icon="$ratingFull"
              half-increments
              hover
              small
            ></v-rating>
          </div>
          {{ client.bio }}
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    clients: [
      {
        img: './client-assets/jann.jpg',
        title: 'Jann Benedick Mendoza',
        subtitle: 'CPO on Maqua',
        bio: '"I was so pleased with the service I received from this business. They went above and beyond to help me find the perfect item."',
        rating: 4
      },
      {
        img: './client-assets/jae.jpg',
        title: 'Jae  Mendoza',
        subtitle: 'CPO on Maqua',
        bio: '“I had an amazing experience with this company. The customer service was outstanding, and the product was exactly what I was looking for.”',
        rating: 5
      },
      {
        img: './client-assets/kara.jpg',
        title: 'Kara Jane Maquiling',
        subtitle: 'CPO on Maqua',
        bio: '“The customer service at this company is excellent. They were accommodating and responsive to my questions.”',
        rating: 3
      }
    ]
  })
}
</script>

<style>

</style>
