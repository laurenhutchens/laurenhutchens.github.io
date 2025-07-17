<script>
  import ImageCard from "./lib/ImageCard.svelte";

  let name = "Lauren Hutchens"; // Your name
  let favoriteNumber = 19; // Favorite number
  let bio = "I am an undergrad student studying software development with machine learning!";
  let hobbies = ["Coding", "Journaling", "Watching tv shows & movies"]; // List some hobbies

  let cardData = [
  {
    image:
    "https://i.pinimg.com/736x/9c/21/f3/9c21f34be8ab236fa7f549ae4e406c08.jpg",
    title: "Coding",
    description:
    "I love solving problems and writing code to build aesthetic things.",
  },
  {
    image: "https://i.pinimg.com/736x/64/fc/65/64fc651f2248828d7a89ca25397ed1c9.jpg",
    title: "Journaling",
    description: "Journaling allows all of the words & dreams from my wind to flow on beautiful pages that will last a lifetime",
  },
  {
    image: "https://i.pinimg.com/736x/e8/e0/d2/e8e0d23ae13841071e4291e637f915c1.jpg",
    title: "Traveling",
    description: "The foggy Oregon coast is a dream of mine to travel",
  },
  ];
</script>

<style>
  h1 {
    color: #8F0013;
    font-family: "EB Garamond", serif;
  }
  .card-container{
    display: flex;
    background-color: #B7C9CC;
  }
  .card-container > div {
    background-color: #B7C9CC;
    margin: 10px;
    padding: 20px;
    font-size: 30px;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #B7C9CC;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
</style>

<div class="container">
  <h1>About Me</h1>
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
  <p>{bio}</p>

  <h2>My Hobbies</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>

  <h2>Some of My Favorite Things</h2>
    <div class="card-container">
      {#each cardData as { image, title, description }}
        <ImageCard {image} {title} {description} />
      {/each}
    </div>


</div>