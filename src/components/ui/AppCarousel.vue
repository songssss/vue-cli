<template>
    <div>
        <p class="pst">{{mss}} carousel component aa {{lastMark}}</p>
        <input type="text" v-model="sametxt" placeholder="입력해보세요">
        <p>your text: {{sametxt}}</p>
    </div>
</template>

<script>
    export default {
        data (){
            return {
                mss: 'hello ~',
                lastMark:'^_^',
                sametxt:''
            }
        }
    }
</script>
<style lang="sass" scoped>
$darks: #222
.pst
    border: 1px solid $darks
    color: $darks
    padding: 10px
    border-radius: 5px
</style>

