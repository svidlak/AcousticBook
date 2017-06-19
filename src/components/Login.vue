<template>
<div class="formStyle">
    <form>
        <div class="form-group">
            <label for="email">Email address:</label>
            <input type="email" class="form-control" id="email">
        </div>
        <div class="form-group">
            <label for="pwd">Password:</label>
            <input type="password" class="form-control" id="pwd">
        </div>
        <input type="button" class="btn btn-default" value="submit">
    </form>

    <div class="reg-text">
        <p>Not acoustic yet?</p>
        <p @click="switchToRegisterComp"><a>register now!</a></p>
        
    </div>
</div>
</template>

<script>
export default {
    methods: {
        switchToRegisterComp(event){
            this.$emit('viewChange')
        }
    }
}
</script>

<style>
.formStyle{
    background-color:rgba(0, 0, 0, 0.5);
    /*padding: 150px 72px;*/
    height: 700px;
    padding-top: 40%;
    padding-left: 40px;
    padding-right: 40px;
    border:1px solid white;
}

.reg-text{
     padding-top: 50px;

}

a:hover{
    cursor: pointer;
    color: red;
}
</style>
