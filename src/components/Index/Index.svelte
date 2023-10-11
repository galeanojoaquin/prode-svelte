<script>
  import axios from "axios";

  let arrayTeams = [];

  const callFetch = () => {
    console.log(axios.isCancel("something"));

    var config = {
      method: "get",
      url: "https://v3.football.api-sports.io/teams?country=Argentina&league=1032&season=2023",
      headers: {
        "x-rapidapi-key": "679f606edc2e73ec617c612986387614",
        "x-rapidapi-host": "v3.football.api-sports.io",
      },
    };

    axios(config)
      .then(function (response) {
        console.log(response.data.response);
        arrayTeams = response.data.response;
        console.log(arrayTeams);
      })
      .catch(function (error) {
        console.log(error);
      });
  };

  callFetch();
</script>

<div class="container">
  <div class="row">
    <p class="text-center">Equipos de fútbol en Argentina</p>
      {#each arrayTeams as team (team.team.id)}
        <div class="col-4 text-center">
          <img src={team.team.logo} alt={team.team.name} width="80" />
          <h3>{team.team.name}</h3>
          <p>Estadio: {team.venue.name}</p>
          <p>Dirección: {team.venue.address}</p>
          <p>Ciudad: {team.venue.city}</p>
          <p>Capacidad: {team.venue.capacity}</p>
        </div>
      {/each}
  </div>
</div>
