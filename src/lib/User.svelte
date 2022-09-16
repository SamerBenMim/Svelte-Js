<script>
   export let image;
   export let age;
   export let name;
   export let index;
</script>

<div class="flex m-5 bg-white border p-2 rounded-lg shadow-md hover:shadow-lg cursor-pointer  items-center" >
    <p class="w-10"> {1+index}</p>
    <img src={image} alt="img" class="rounded-full w-14 h-14 mx-4">
    <p class="mx-4 w-20">{name}</p>
    <p  class="mx-4 w-20 ">{age}</p>
</div>