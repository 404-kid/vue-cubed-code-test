<template>
<Scene name="winter">
    <square name="floor"/>
    <SnowFlake pool=200/>
    <Tree/>
    <polygon name="snowman">
        <sphere name="head"/> 
        <sphere name="body"/>
        <sphere name="legs"/>
        <cylinder name="leftArm"/>
        <cylinder name="rightArm"/>
    </polygon>
</Scene>
</template>

<script>
// @ is an alias to /src
import SnowFlake from '@/geometry/SnowFlake.vue'
import Tree from '@/geometry/Tree.vue'

export default {
    name: 'scene1',
    components: {
        SnowFlake,
        Tree
    },
    initialization:{
        winter:{
            size: [70, 70, 70]
        }
        floor:{
            size: [50, 50, 1],
            color: 'rbga(255,255,255,1)'
        },
        SnowFlake:{
            location: ()
        }
        
    },
    step:{

    }
}
</script>
