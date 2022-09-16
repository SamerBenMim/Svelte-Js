<script>
    import User from "./User.svelte";


    let users = [
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: "27 129 130"
    },
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: "27 129 130"
    },
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: "27 129 130"
    },
    ] ;

    const getUsers = ()=> {
        return users;
    }
</script>

<div>
    <h1 class="text-2xl text-center mt-10">
      List of users
    </h1>
    {#each getUsers() as {image,name,age} , index}
    <User {image} {index} {age} {name}/>
    {:else}
    <p>No user found</p>
    {/each}
</div>
  