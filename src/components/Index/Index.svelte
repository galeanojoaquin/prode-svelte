<script>
  import axios from "axios";

  const callFetch = () => {
    console.log(axios.isCancel("something"));

    var config = {
      method: "get",
      url: "https://v3.football.api-sports.io/fixtures/rounds?season=2023&league=1032",
      headers: {
        "x-rapidapi-key": "679f606edc2e73ec617c612986387614",
        "x-rapidapi-host": "v3.football.api-sports.io",
      },
    };

    axios(config)
      .then(function (response) {
        console.log(response.data);
      })
      .catch(function (error) {
        console.log(error);
      });
  };

  callFetch();
</script>

<div class="nes-container with-title is-centered">
  <p class="title">
    <br />
  </p>
  <p>
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus explicabo
    error blanditiis nulla quidem tenetur, labore impedit quaerat modi velit
    asperiores pariatur facere ipsum dolores atque dolorem amet minima sunt!
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus repudiandae
    itaque incidunt, soluta quaerat voluptas! Itaque fuga, dicta, corrupti ipsam
    voluptas deleniti provident iure quia quam ea ipsum blanditiis officiis!
  </p>
</div>
