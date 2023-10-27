<script>
  import { Link, link, navigate } from "svelte-routing";
  // import { token, user } from "../../store/store";

  // $: isAuthenticated = $token;
  // $: datos = $user;

  // const logout = () => {
  //   token.set(false);
  //   localStorage.clear();
  //   navigate("/login", { replace: false });
  // };

  // const colorThemeDark = () => {
  //   document.querySelector("body").setAttribute("data-bs-theme", "dark");
  // };

  // const colorThemeLight = () => {
  //   document.querySelector("body").setAttribute("data-bs-theme", "light");
  // };
</script>

<nav
  class="navbar navbar-expand-lg shadow p-3 fixed-top py-2"
  style="padding: 0.5rem 0.5rem"
>
  <div class="container">
    <Link class="navbar-brand" to="/prode-svelte">
      <img src="../public/image/copadelaliga.png" alt="brand" width="58px" />
      <span class="mb-2 ms-2">PRODE</span>
    </Link>

    <button
      class="navbar-toggler border-0"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
      ><span class="navbar-toggler-icon" /></button
    >
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0 d-print-none">
        <li class="nav-item">
          <Link
            class="nav-link d-flex aling-items-center"
            aria-current="page"
            to="/ciudadano/buscar"
          >
            <i class="material-icons" title="Buscar"> search </i>
            <span class="nav-link-inner--text d-lg-none ms-2">Buscar</span>
          </Link>
        </li>
        <li class="nav-item">
          <Link
            class="nav-link d-flex aling-items-center"
            aria-current="page"
            to="/ciudadano/alta"
          >
            <i class="material-icons" title="Alta ciudadano"> person_add </i>
            <span class="nav-link-inner--text d-lg-none ms-2"
              >Alta ciudadano</span
            >
          </Link>
        </li>
        <li class="nav-item">
          <Link
            class="nav-link d-flex aling-items-center"
            aria-current="page"
            to="/visita/mis-atenciones"
          >
            <i class="material-icons" title="Inbox (atenciones)"> all_inbox </i>
            <span class="nav-link-inner--text d-lg-none ms-2"
              >Inbox (atenciones)</span
            >
          </Link>
        </li>
        <li class="nav-item">
          <Link
            class="nav-link d-flex aling-items-center"
            aria-current="page"
            to="visita/oficina-atenciones"
          >
            <i class="material-icons" title="Inbox"> inbox </i>
            <span class="nav-link-inner--text d-lg-none ms-2">Inbox</span>
          </Link>
        </li>
        <li class="nav-item py-2 py-lg-1 col-12 col-lg-auto">
          <div class="vr d-none d-lg-flex h-100 mx-lg-2 text-white" />
          <hr class="d-lg-none my-2 text-white-50" />
        </li>
        <li class="nav-item dropdown d-flex align-items-center">
          <a
            class="nav-link dropdown-toggle d-flex align-items-center"
            id="navbarDropdown"
            use:link
            href="/"
            role="button"
            data-bs-toggle="dropdown"
            aria-expanded="false"
          >
            <i class="material-icons" title="Perfil"> account_circle </i>
            <span class="ms-2" title="Perfil">
              <!-- {datos.legajo} -->
            </span>
          </a>
          <ul
            class="dropdown-menu dropdown-menu-end"
            aria-labelledby="navbarDropdown"
          >
            <li>
              <button
                class="dropdown-item d-flex aling-items-center"
                to="/account/profile"
              >
                <span class="material-icons"> person </span>
                Perfil</button
              >
            </li>
            <li><hr class="dropdown-divider" /></li>
            <li>
              <button class="dropdown-item d-flex aling-items-center">
                <span class="material-icons"> logout </span>
                Desconectarse
              </button>
            </li>
          </ul>
        </li>
        <li class="nav-item py-2 py-lg-1 col-12 col-lg-auto">
          <div class="vr d-none d-lg-flex h-100 mx-lg-2 text-white" />
          <hr class="d-lg-none my-2 text-white-50" />
        </li>
        <li class="nav-item dropdown">
          <a
            class="nav-link dropdown-toggle d-flex align-items-center"
            id="theme-menu"
            aria-expanded="false"
            data-bs-toggle="dropdown"
            data-bs-display="static"
            aria-label="Toggle theme"
          >
            <i class="bi bi-circle-half" />
            <span class="material-icons"> contrast </span>
          </a>
          <ul class="dropdown-menu dropdown-menu-end">
            <li>
              <button
                type="button"
                on:click={colorThemeLight}
                class="dropdown-item d-flex align-items-center"
                data-bs-theme-value="light"
                aria-pressed="false"
              >
                <i class="bi bi-sun-fill" /><span class="material-icons ms-2"
                  >sunny</span
                >
                Light mode
              </button>
            </li>
            <li>
              <button
                type="button"
                class="dropdown-item d-flex align-items-center"
                data-bs-theme-value="dark"
                aria-pressed="true"
                on:click={colorThemeDark}
              >
                <i class="bi bi-moon-stars-fill" /><span
                  class="material-icons ms-2">dark_mode</span
                > Dark mode
              </button>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</nav>

<style>
  .nav-link {
    color: aliceblue;
    background-color: #00476b;
  }

  .nav-item {
    color: aliceblue;
    background-color: #00476b;
  }

  .dropdown-item {
    background-color: #00476b;
    color: aliceblue;
  }

  .dropdown-menu {
    background-color: #00476b;
    color: aliceblue;
  }
</style>
