<script lang="ts">
  let name: string = "world";
</script>

<header>
  <ul>
    <li>
      <svg
        width="31"
        height="30"
        viewBox="0 0 31 30"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M28.1134 10.76V20.9375C28.1134 21.9752 27.7159 22.9735 27.0022 23.7278C26.2886 24.482 25.313 24.935 24.2756 24.9938L24.0452 25H7.14676C6.10765 25.0001 5.1079 24.6031 4.35259 23.8904C3.59729 23.1778 3.1437 22.2035 3.08487 21.1675L3.07861 20.9375V10.76L15.1604 17.08C15.2948 17.1503 15.4443 17.187 15.596 17.187C15.7477 17.187 15.8972 17.1503 16.0316 17.08L28.1134 10.76ZM7.14676 5H24.0452C25.0536 4.99988 26.0261 5.37374 26.7741 6.04908C27.522 6.72442 27.9922 7.6531 28.0934 8.655L15.596 15.1925L3.09864 8.655C3.19568 7.69289 3.6332 6.7969 4.33254 6.12808C5.03189 5.45926 5.9472 5.06148 6.91394 5.00625L7.14676 5H24.0452H7.14676Z"
          fill="white"
        />
      </svg>
      <a href="mailto: INFO@E-ELEC.BE"> INFO@E-ELEC.BE </a>
    </li>
    <li>
      <svg
        width="29"
        height="29"
        viewBox="0 0 29 29"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M11.9452 17.2C13.6872 18.9647 15.795 20.3272 18.1205 21.1917L21.2665 18.6917C21.3598 18.6275 21.4704 18.5932 21.5836 18.5932C21.6969 18.5932 21.8074 18.6275 21.9007 18.6917L27.7422 22.45C27.9639 22.5831 28.1517 22.766 28.2905 22.984C28.4294 23.202 28.5156 23.4493 28.5423 23.7064C28.569 23.9634 28.5355 24.2231 28.4444 24.4649C28.3533 24.7068 28.2072 24.9242 28.0175 25.1L25.2804 27.8C24.8884 28.1868 24.4066 28.4706 23.8781 28.6262C23.3495 28.7818 22.7906 28.8043 22.2512 28.6917C16.8706 27.5819 11.9111 24.9829 7.93966 21.1917C4.05633 17.3627 1.36909 12.4907 0.203912 7.16666C0.088807 6.63636 0.112831 6.08536 0.273655 5.56706C0.43448 5.04875 0.726651 4.58073 1.12185 4.20833L3.95913 1.475C4.1347 1.29482 4.34882 1.15664 4.58545 1.07081C4.82208 0.98498 5.07509 0.95372 5.32553 0.97937C5.57598 1.00502 5.81736 1.08692 6.03162 1.21893C6.24587 1.35094 6.42745 1.52965 6.56274 1.74166L10.4515 7.5C10.5186 7.59042 10.5548 7.69997 10.5548 7.8125C10.5548 7.92502 10.5186 8.03457 10.4515 8.125L7.88959 11.2C8.7788 13.4758 10.1642 15.5253 11.9452 17.2V17.2Z"
          fill="white"
        />
      </svg>
      <a href="tel:+32 69 420 666"> +32 69 420 666</a>
    </li>
  </ul>
</header>
<nav>
  <div class="wrapper">
    <h2>E-ELEC</h2>
    <ul>
      <li><a href="#"> over ons </a></li>
      <li><a href="#"> realisatie </a></li>
      <li><a href="#"> contact </a></li>
    </ul>
  </div>
</nav>
<div id="banner">
  <div class="wrapper">
    <div class="title">
      <h1>WE SHAPE LIGHT</h1>
      <p>
        Wij zijn een jong en dynamisch bedrijf dat instaat voor al uw algemene
        elektriciteitswerken in nieuwbouw, verbouwingen en automatisatie
      </p>
      <button class="button">
        <a href="#">Contacteer ons</a>
      </button>
    </div>
    <div class="logo">
      <img src="./assets/logo.png" alt="logo" />
    </div>
  </div>
</div>
<div>
  <svg
    id="svg-triangle-top"
    viewBox="0 0 175 15"
    preserveAspectRatio="none"
    class="bgSlobed"><polygon points="0,15 200,0 0,0" /></svg
  >
  <svg
    id="svg-triangle-top"
    viewBox="0 0 200 15"
    preserveAspectRatio="none"
    class="bgSlobedUnderline"><polygon points="0,15 200,0 0,0" /></svg
  >
</div>
<main />

<style lang="scss">
  $blue: #6bc9ef;
  $orange: #ef916b;
  $lightBlue: #aaddf6;

  ul {
    display: flex;
    margin: 0.5rem;

    li {
      padding: 0 1rem;
      list-style: none;
      display: flex;
      align-items: center;

      a {
        padding-left: 0.5em;
      }
    }
  }

  header {
    background-color: $orange;
    color: white;
    display: flex;
    justify-content: flex-end;
  }

  nav {
    color: white;
    background-color: $blue;

    h2 {
      font-size: 2rem;
      text-shadow: 4px 4px 0px rgba(170, 221, 246, 0.6);
    }
  }

  #banner {
    color: white;
    background-color: $blue;
    padding: 5rem 0;

    h1 {
      font-size: 2.5rem;
    }

    button {
      background: $orange;
      padding: 0.25em 0.5rem;
      border-radius: 5px;
      cursor: pointer;
      margin: 1em 0;
      text-decoration: none;
      color: inherit;
      border: 0;
    }

    img {
      width: 15rem;
    }
  }

  .bgSlobed {
    fill: $lightBlue;
  }

  .bgSlobedUnderline {
    position: absolute;
    left: 0;
    fill: $blue;
  }

  .wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1200px;
    margin: 0 auto;
  }
</style>
