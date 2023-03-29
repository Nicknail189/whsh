<template>
  <div class="container h-max w-full md:w-max bg-[#f3f3f3] text-[#333]">
    <div class="text-md">
      <div class="pi">
        <h4>Firstname:</h4>
        <span>{{ personal.firstname }}</span>
      </div>
      <div class="pi">
        <h4>Lastname:</h4>
        <span>{{ personal.lastname }}</span>
      </div>
      <div class="pi">
        <h4>Date of birth:</h4>
        <span>{{ personal.dob }}</span>
      </div>
      <div class="pi">
        <h4>Address:</h4>
        <span>{{ personal.address }}</span>
      </div>
      <div class="pi">
        <h4>State:</h4>
        <span>{{ personal.state }}</span>
      </div>
      <div class="pi">
        <h4>Country:</h4>
        <span>{{ personal.country }}</span>
      </div>
      <div class="pi">
        <h4>Sex:</h4>
        <span>{{ personal.sex }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      personal: {
        firstname: 'Langlois',
        lastname: 'Rene',
        dob: '26/09/1962',
        address: '45 boulevard des champs fleuris laprairie J5R3Z1 Québec',
        state: 'Canadian province of Québec',
        country: 'Canada',
        sex: 'Male'
      }
    }
  }
}
</script>

<style scoped>
h4 {
  padding: 4px 10px;
  display: flex;
  justify-content: space-between;
  font-weight: 600;
}

span {
  width: 50%;
  text-align: right;
  font-weight: 400;
  display: flex;
  justify-content: flex-end;
}
</style>