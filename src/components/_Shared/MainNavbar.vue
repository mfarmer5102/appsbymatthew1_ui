<template>
    <div id="nav" class='bg-light' style="width: 100%; overflow-x: scroll;">

        <nav class="navbar navbar-expand navbar-light bg-light" style="position: relative; height: 35px">
            <a class="navbar-brand" href="#" style=" font-family: 'MuseoModerno', cursive;">appsbymatthew.com</a>
            <div class="text-left pl-3" style="position: absolute; right: 10px">
                <small>Version {{softwareVersion}}</small>
            </div>
        </nav>
        
        <nav class="navbar navbar-expand navbar-light bg-light">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <router-link :to="{name:'Welcome_Index'}">Welcome</router-link>
                </li>
                <li class='nav-item'>
                    <router-link :to="{name:'Applications_ListFeatured'}">Applications</router-link>
                </li>
                <li class='nav-item'>
                    <router-link :to="{name:'Skills_ListAll'}">Skills</router-link>
                </li>
                <li class='nav-item'>
                    <router-link :to="{name:'Contact_Index'}">Contact</router-link>
                </li>
                <!-- <li class='nav-item'>
                    <router-link :to="{name:'Metrics_Index'}">Metrics</router-link>
                </li> -->
            </ul>
        </nav>
    </div>
</template>

<script>

import packageJson from "../../../package.json";
import common from "@/common";

export default {
    name: "NavbarMain",
    mounted: function() {
    },  
    methods: {
    },
    data() {
        return {
            softwareVersion: packageJson.version
        }
    }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height: 100vh;
}

#nav a {
    margin-right: 20px;
    font-weight: bold;
    color: #2c3e50;
    padding: 5px;
}

#nav a.router-link-exact-active {
    background-color: #42b983;
    border-radius: 10px;
    color: white;
    transition: background-color 0.5s, color 0.5s;
}

</style>