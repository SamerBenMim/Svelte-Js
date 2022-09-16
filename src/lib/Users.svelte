<script>
    import User from "./User.svelte";


    let users = [
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: "27 129 130",
        active : true
    },
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: "27 129 130",
        active : true,


    },
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: "27 129 130",
        active : false

    },
    ] ;
    let filteredUsers = users;

</script>

<div>
    <h1 class="text-2xl text-center mt-10">
      List of users
    </h1>
    <select
    on:change="{(e) => {
        const status= e.target.value=="true";

        if(e.target.value ===null){
            filteredUsers = users;
            return
        }
        else{

            filteredUsers = users.filter((user) => {
                
                return    user.active == status 
            });
        }
    }}"
    name="user-filter" class="border-rounded-lg px-4 py-2 ml-4" >
        <option value={null}>ALL</option>
        <option value={true}>ACTIVE</option>
        <option value={false}>INACTIVE</option>
    </select>
    {#each filteredUsers as {image,name,age} , index}
    <User {image} {index} {age} {name}/>
    {:else}
    <p>No user found</p>
    {/each}
</div>
  