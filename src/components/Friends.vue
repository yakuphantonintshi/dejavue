<template>
    <div class="container">
        <div class="row">
            <h2 class="display-2">Best Friends</h2>
        </div>
        <div class="row gap-2 justify-content-center" v-if="friends.length">
            <Card v-for="friend in friends" :key="friend.id" :class="{
            male: friend.gender.toLowerCase() == 'male',
            female: friend.gender.toLowerCase() == 'female'
        }">
                <template #cardHeader>
                    <img :src="friend.profile" :alt="friend.firstName" class="img-fluid" loading="lazy">
                </template>
                <template #cardBody>
                    <p class="lead">{{ friend.firstName }} {{ friend.lastName }}</p>
                </template>

            </Card>
        </div>
        <div class="d-flex justify-content-center" v-else>
            <div class="spinner-border" role="status">
            </div>
        </div>
    </div>
</template>

<script>
import Card from './Card.vue'
export default {
    name: "FriendComp",
    components: {
        Card
    },
    data() {
        return {
            friends: [
            {
                    id:0, 
                    firstName: "Yakupha",
                    lastName: "Ntonintshi",
                    gender: "Female",
                    profile: "https://yakuphantonintshi.github.io/myimages/Images/my_picture2.jpg"
                },
                {
                    id: 1,
                    firstName: "Simanye",
                    lastName: "Somdaka",
                    gender: "Male",
                    profile: "https://yakuphantonintshi.github.io/myimages/Images/simanye.jpg"
                },
                {
                    id: 2,
                    firstName: "Khanya",
                    lastName: "Pupuma",
                    gender: "Male",
                    profile: "https://yakuphantonintshi.github.io/myimages/Images/Khanya.jpg"
                }
                
            ]
        }
    }

}
</script>

<style scoped>
.male {
    border: 2px solid gold;
    box-shadow: .3vw .2vw .5vw green;
}

.female {
    border: 2px solid pink;
    box-shadow: .3vw .2vw .5vw orange;
}
</style>