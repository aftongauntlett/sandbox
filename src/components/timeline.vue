<template>
<v-container>
    <v-timeline clipped dense>
        <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold --text`"
          v-text="year"
        ></span>
      </template>
      <div>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolore recusandae tempore officia vel adipisci sed reiciendis nemo temporibus possimus quia doloremque placeat facere, nostrum pariatur unde nulla! Fuga, asperiores ex? 
      </div>
        </v-timeline-item>
    </v-timeline>
</v-container>
     <!-- <v-row>
         <v-col cols="2">
             <nav>
                 <ul>
                     <li 
                         v-for="year in years"
                         :key="`${year}-nav`"
                         :class="$route.hash === `#${year}` ? 'active' : ''"
                    >
                        <a :href="`#${year}`">{{year}}</a>
                    </li>
                 </ul>
             </nav>
         </v-col>
         <v-col cols="10">
             <div
                v-for="year in years"
                :key="`${year}`"
                :class="$route.hash === `#${year}` ? `active` : ''"
                class="filler"
             >
                 <h2 :ref="year">{{year}}</h2>
            </div>
         </v-col>
     </v-row> -->
</template>

<script>
export default {
    data() {
        return{
            years: [
                "2000",
                "2001",
                "2002",
                "2003",
                "2004",
            ]
        }
    },
}
</script>

<style scoped>
.filler {
    background-color: red;
    height: 250px;
    margin-bottom: 10px;
}

.active {
    font-size: 36px;
}

/deep/ .v-timeline--dense .v-timeline-item__opposite {
  display: inline-block;
}

/deep/ .v-timeline-item--left .v-timeline-item__opposite, .v-timeline-item:nth-child(odd):not(.v-timeline-item--right) .v-timeline-item__opposite {
  margin-left: 16px;
  margin-right: 86px;
}
/deep/ .v-timeline-item--right .v-timeline-item__opposite, .v-timeline-item:nth-child(2n):not(.v-timeline-item--left) .v-timeline-item__opposite {
  margin-left: 16px;
  margin-right: 86px;
  text-align: left;
}

/deep/ .v-timeline--dense:before {
  left: 110px;
}
/deep/ .v-timeline--dense .v-timeline-item__dot--small {
  left: 99px;
}

</style>