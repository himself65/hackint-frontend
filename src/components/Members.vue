<template>
  <v-container fluid grid-list-md>
    <v-layout
      justify-center
      align-center
      wrap
    >
      <v-flex
        :key="member.name"
        v-for="member in members"
        class="xs12 lg5"
      >
        <v-hover>
          <v-card
            slot-scope="{ hover }"
            :class="`elevation-${hover ? 12 : 2}`"
            class="mx-auto member"
            :color="member.color"
            dark
            max-width="400"
          >
            <v-card-title>
              <v-list-tile class="grow">
                <v-list-tile-avatar color="grey darken-3">
                  <v-img
                    class="elevation-3"
                    :src="require(`../assets/member/${member.avatar}`)"
                  ></v-img>
                </v-list-tile-avatar>

                <v-list-tile-content>
                  <v-list-tile-title class="font-weight-bold">{{ member.name }}</v-list-tile-title>
                </v-list-tile-content>
              </v-list-tile>
            </v-card-title>

            <v-card-text class="headline font-weight-light">
              {{ member.description || '这个人很强，什么也不想写' }}
            </v-card-text>

            <v-card-actions>
              <v-btn
                flat
                color="grey lighten-5"
                :href="`https://github.com/${member.github}`"
                target="_blank">
                Github
              </v-btn>
              <v-btn
                flat
                color="light-blue lighten-1"
                :href="`https://zhihu.com/people/${member.zhihu}`"
                target="_blank">
                知乎
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-hover>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Members',
  data () {
    return {
      members: [
        {
          name: 'lemon（队长）',
          avatar: 'lemon.png',
          description: '',
          color: 'deep-purple darken-1',
          github: 'LemonHX',
          zhihu: 'ning-meng-wan-xiong-99'
        },
        {
          name: 'Ray Eldath',
          avatar: 'ray.png',
          description: 'Kotlin专精，全栈开发者',
          color: 'orange darken-2',
          github: 'Ray-Eldath',
          zhihu: 'eldath-ray'
        },
        {
          name: '郑泓',
          avatar: 'xjj.png',
          description: '',
          color: 'teal darken-1',
          github: ''
        },
        {
          name: '扩散性百万甜面包',
          avatar: 'bread.jpg',
          description: '曾为洛谷前端开发。最近贡献开源，Node.js Contributor',
          color: 'indigo accent-3',
          github: 'himself65',
          zhihu: 'Himself65'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .member {
    margin 0.25em
  }
</style>
