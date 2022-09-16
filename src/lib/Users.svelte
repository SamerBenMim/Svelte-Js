<script>
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
    {#each getUsers() as user , index}
    <div class="flex m-5 bg-white border p-2 rounded-lg shadow-md hover:shadow-lg cursor-pointer  items-center" >
        <p class="w-10"> {1+index}</p>
        <img src={user.image} alt="img" class="rounded-full w-14 h-14 mx-4">
        <p class="mx-4 w-20">{user.name}</p>
        <p  class="mx-4 w-20 ">{user.age}</p>
    </div>
    {:else}
    <p>No user found</p>
    {/each}
</div>
  