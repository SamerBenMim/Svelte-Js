<script>
    let users = [
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: 30
    },
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: 30
    },
    {
        image :"https://cdn-icons-png.flaticon.com/128/3135/3135715.png", 
        name: "John",
        age: 30
    },
    ] ;

    const getUsers = ()=> {
        return users;
    }
</script>

<div>
    <h1>
      List of users
    </h1>
    {#each getUsers() as user , index}
    <div >
        <p> {1+index}</p>
        <img src={user.image} alt="img">
        <p>{user.name}</p>
        <p>{user.age}</p>
    </div>
    {:else}
    <p>No user found</p>
    {/each}
</div>
  