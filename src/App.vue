<template>
  <div>
    <TopNav />
    <div class="px-20 flex flex-wrap">
      <div v-for="(arr, index) in subArrays" :key="index" class="w-1/5">
        <div v-for="(card, i) in arr" :key="i" class="w-full">
          <div class="full p-2">
            <Card :src="`${card.src}`" :board="`${card.recommend}`" class="w-full h-full" />
            <div class="text-sm leading-tight p-2">
              <p class="font-bold">{{ card.title }}</p>
              <p class="">{{card.user}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div> 
</template>

<script>
import TopNav from './components/TopNav.vue'
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    TopNav,
    Card
  },
  computed: {
    subArrays() {
      var length = Math.ceil(this.cards.length / 5)

      const result = new Array(length)
        .fill()
        .map((i) => {
          return this.cards.splice(0, length)
        })

      return result
    }
  },
  data () {
    return {
      cards: [
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommend: 'Technology'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommend: 'Technology'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommend: 'Technology'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommend: 'Technology'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommend: 'Technology'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommend: 'Technology'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommend: 'Technology'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommend: 'Technology'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommend: 'Technology'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommend: 'Technology'
        },
      ]
    }
  }
}
</script>

<style>

</style>
