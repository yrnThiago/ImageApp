<script setup>
    import { defineEmits } from 'vue';

    const emits = defineEmits(["selectOption"]);

    const selectOption = (isColor) => {
        emits("selectOption", isColor);
    };

</script>

<template>
    <v-navigation-drawer expand-on-hover rail>
        <v-list>
          <v-list-item
            prepend-avatar="https://cdn.discordapp.com/avatars/244933465634504712/16ddc2f5134e5b9a00c47ca9058d0159.webp?size=64"
            title="Thiago Ribeiro"
            subtitle="thiago@hotmail.com"
          ></v-list-item>
        </v-list>

        <v-divider/>

        <v-list density="compact" nav>
            <v-list-item 
                prepend-icon="mdi-image"
                title="Color Gallery"
                value="color"
                @click="selectOption(true)"
            />
            <v-list-item 
                prepend-icon="mdi-dialpad"
                title="Grayspace Gallery"
                value="grayspace"
                @click="selectOption(false)"
            />
            <v-list-item
                prepend-icon="mdi-folder"
                title="Saved"
                value="saved_pics"
            />
        </v-list>
    </v-navigation-drawer>
</template>