<template>
  <div class="container">
    <div class="row">
        <h1>My Friends</h1>
    </div>
    <div class="row gap-2" v-if="friends.length">
    <Card v-for="(friend, id) in friends" :key="id" :class="{male: friend.gender.toLowerCase() == 'male', female: friend.gender.toLowerCase() == 'female' }">

    <template #cardHeader>
      <img :src="friend.profile" :alt="friend.firstName" loading="lazy" class="img-fluid">
      </template>
      
      <template #cardBody>
        <p>{{ friend.firstName }} {{ friend.lastName }}</p>
        <p>{{ friend.gender }}</p>
        </template>
    </Card>
  </div>
  <div class="row" v-else>
    <div class="dot-spinner">
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
    <div class="dot-spinner__dot"></div>
</div>
  </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
    name: 'FriendsComp',
    components: {
        Card

    },
    data(){
    return { 
      friends: [
        { 
          id:1,
          firstName: 'Mapule',
          lastName: 'Mbuzwana',
          gender: 'Male',
          profile: 'https://amyj0hn.github.io/project-images/images/picture_placeholder.jpg'


        },
        { 
          id:2, 
          firstName: 'Mbalentle',
          lastName: 'Diko',
          gender:'Female',
          profile: 'https://amyj0hn.github.io/project-images/images/user-profile-icon.jpg'

        },
        { 
          id:3,
          firstName: 'Nasheeta',
          lastName: 'Jacobs',
          gender: 'Female',
          profile: 'https://amyj0hn.github.io/project-images/images/picture_placeholder.jpg'

        },
        {
          id:4,
          firstName: 'Mordecai',
          lastName: 'Dimbu',
          gender: 'Male',
          profile: 'https://amyj0hn.github.io/project-images/images/user-profile-icon.jpg'

        },
        {
          id:5,
          firstName: 'Sipho',
          lastName: 'Nkebe',
          gender: 'Male',
          profile: 'https://amyj0hn.github.io/project-images/images/picture_placeholder.jpg',
          

        },
        {
          id:6,
          firstName: 'Zizipho',
          lastName: 'Copiso',
          gender: 'Female',
          profile: 'https://amyj0hn.github.io/project-images/images/user-profile-icon.jpg'

        },
        {
          id:7,
          firstName: 'Zaida',
          lastName: 'Sulaiman',
          gender: 'Female',
          profile: 'https://amyj0hn.github.io/project-images/images/picture_placeholder.jpg'

        },
        {
          id:8,
          firstName: 'Nikita',
          lastName: 'Jordaan',
          gender: 'Female',
          profile: 'https://amyj0hn.github.io/project-images/images/user-profile-icon.jpg'

        }
      ]
    }
  }
}

</script>

<style scoped>
.male{
    background-color: gold;
}
.female{
    background-color: pink;
}
/* Spinner */
.dot-spinner {
  --uib-size: 2.8rem;
  --uib-speed: .9s;
  --uib-color: #183153;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  height: var(--uib-size);
  width: var(--uib-size);
}

.dot-spinner__dot {
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  height: 100%;
  width: 100%;
}

.dot-spinner__dot::before {
  content: '';
  height: 20%;
  width: 20%;
  border-radius: 50%;
  background-color: var(--uib-color);
  transform: scale(0);
  opacity: 0.5;
  animation: pulse0112 calc(var(--uib-speed) * 1.111) ease-in-out infinite;
  box-shadow: 0 0 20px rgba(18, 31, 53, 0.3);
}

.dot-spinner__dot:nth-child(2) {
  transform: rotate(45deg);
}

.dot-spinner__dot:nth-child(2)::before {
  animation-delay: calc(var(--uib-speed) * -0.875);
}

.dot-spinner__dot:nth-child(3) {
  transform: rotate(90deg);
}

.dot-spinner__dot:nth-child(3)::before {
  animation-delay: calc(var(--uib-speed) * -0.75);
}

.dot-spinner__dot:nth-child(4) {
  transform: rotate(135deg);
}

.dot-spinner__dot:nth-child(4)::before {
  animation-delay: calc(var(--uib-speed) * -0.625);
}

.dot-spinner__dot:nth-child(5) {
  transform: rotate(180deg);
}

.dot-spinner__dot:nth-child(5)::before {
  animation-delay: calc(var(--uib-speed) * -0.5);
}

.dot-spinner__dot:nth-child(6) {
  transform: rotate(225deg);
}

.dot-spinner__dot:nth-child(6)::before {
  animation-delay: calc(var(--uib-speed) * -0.375);
}

.dot-spinner__dot:nth-child(7) {
  transform: rotate(270deg);
}

.dot-spinner__dot:nth-child(7)::before {
  animation-delay: calc(var(--uib-speed) * -0.25);
}

.dot-spinner__dot:nth-child(8) {
  transform: rotate(315deg);
}

.dot-spinner__dot:nth-child(8)::before {
  animation-delay: calc(var(--uib-speed) * -0.125);
}

@keyframes pulse0112 {
  0%,
  100% {
    transform: scale(0);
    opacity: 0.5;
  }

  50% {
    transform: scale(1);
    opacity: 1;
  }
}

</style>