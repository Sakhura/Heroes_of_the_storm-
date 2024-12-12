<template>
    <v-app>
        <v-main>
            <div class="heroes-background">
                <v-container>
                    <h1 class="display-1 text-center white--text">Héroes</h1>
                    <v-row justify="center" class="my-4">
                        <v-chip color="red" dark>Agresor</v-chip>
                        <v-chip color="green" dark>Guerrero</v-chip>
                        <v-chip color="blue" dark>Sanadora</v-chip>
                        <v-chip color="purple" dark>Tanque</v-chip>
                    </v-row> 

                    <v-simple-table>
                        <thead>
                            <tr>
                                <th>Imagen</th>
                                <th>Nombre</th>
                                <th>Función</th>
                                <th>Título</th>
                                <th>Ataque</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="hero in heroes" :key="hero.name">
                                <td><img :src="hero.image" :alt="hero.name" class="hero-image"></td>
                                <td>{{ hero.name }}</td>
                                <td>{{ hero.rol }}</td>
                                <td>{{ hero.title }}</td>
                                <td>{{ hero.attack }}</td>
                            </tr>
                        </tbody> 
                    </v-simple-table>
                    <v-btn color="orange darken-3" @click="$router.push('/')">Volver al Home</v-btn>
                </v-container>
            </div>
        </v-main>
    </v-app>
</template>

<script>
export default{
    name: 'HeroesView',
    data: () => ({
        heroes: [
            {
                name: 'Artanis',
                role: 'Agresor',
                title: 'Jerarca de los Daelaam',  
                attack: 111,
                image: 'https://static.heroesofthestorm.com/heroes/yrel/skins/light-of-hope-800.jpg',

            },

            //agregar + heroes
        ],
    }),
};
</script>

<style>
.heroes-background{
    background: url('https://static.heroesofthestorm.com/heroes/yrel/skins/light-of-hope-800.jpg') no-repeat center center fixed;
    background-size: cover;
    filter: blur(8px);
}

.hero-image{
    width: 100px;
    height: auto;
}
</style>
