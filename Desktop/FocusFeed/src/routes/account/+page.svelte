<script>
  import { goto } from '$app/navigation';

  let password = '';
  let username = '';

  function handleSubmit() {
    console.log("Username:", username);
    console.log("Password:", password);
  }
</script>

<main class="custom-background">

  <div id="loading-indicator" class="loading-indicator">
    <img src="/spinner.gif" alt="Loading..." />
  </div>

  <div class="header-image">
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img src="https://images.squarespace-cdn.com/content/v1/64ba92ff4c24fe41a3c67b1d/1689953074945-9WI8FKUEAOY9HQX8636Q/Sleek+Objects+1.jpg" alt="Header Image">
     
    <div class="header-text">FocusFeed</div>
    <div class="header-text2">Account Subscription</div>

    <div class="account">
      <a href="/account" class="account-button">Redirect</a>
    </div>
  </div>

  <h1>Enter the required information below to allow FocusFeed to send emails to you to start your day!</h1>


  <div class="username-container">
    <h2>Username</h2>
  </div>

  <div class="username-container">
    <input 
      type="password" 
      bind:value={username}
      class="username-input"
    />
  </div>

  <div class="username-container">
    <h4>Password</h4>
  </div>

  <div class="password-container">
    <input 
      type="password" 
      bind:value={password}
      class="password-input"
    />
  </div>





  <div class="center-button-wrapper">
    <button on:click={handleSubmit} class="submit-button">SEND</button>
  </div>
</main>

    
    
    
<style>
    
  @font-face {
    font-family: 'adonis-web';
    font-style: normal;
    font-weight: 400;
    src:url(https://use.typekit.net/pf/ss/qdyr/n4/l?subset_id=2&primer=9f562d6ca39adae019ef00367c3f3deae3c8627f22e3b025ba425fbc2aac6431&fvd=n4&ec_token=BInhlQ%2Bl4i%2FTK2LNzmpe2QC%2Bdl6Qc7iJa15oy7OfSGK%2BY7lwDRam4FlQCIzQGEqAiJZo10MshaDLZWgX%2FckdPK0bOW%2FAfpkj2O5MO1d7Aul7v1RGoa7OBxfdciGAxZqjHAPKKo0fqkxxKF%2F9mM9JjA%3D%3D) format("woff2"),url(https://use.typekit.net/pf/ss/qdyr/n4/d?subset_id=2&primer=9f562d6ca39adae019ef00367c3f3deae3c8627f22e3b025ba425fbc2aac6431&fvd=n4&ec_token=BInhlQ%2Bl4i%2FTK2LNzmpe2QC%2Bdl6Qc7iJa15oy7OfSGK%2BY7lwDRam4FlQCIzQGEqAiJZo10MshaDLZWgX%2FckdPK0bOW%2FAfpkj2O5MO1d7Aul7v1RGoa7OBxfdciGAxZqjHAPKKo0fqkxxKF%2F9mM9JjA%3D%3D) format("woff"),url(https://use.typekit.net/pf/ss/qdyr/n4/a?subset_id=2&primer=9f562d6ca39adae019ef00367c3f3deae3c8627f22e3b025ba425fbc2aac6431&fvd=n4&ec_token=BInhlQ%2Bl4i%2FTK2LNzmpe2QC%2Bdl6Qc7iJa15oy7OfSGK%2BY7lwDRam4FlQCIzQGEqAiJZo10MshaDLZWgX%2FckdPK0bOW%2FAfpkj2O5MO1d7Aul7v1RGoa7OBxfdciGAxZqjHAPKKo0fqkxxKF%2F9mM9JjA%3D%3D) format("opentype");font-weight:400;font-style:normal;}
  
    @font-face {
    font-family: 'Pontano Sans';
    font-style: normal;
    font-weight: 400;
    src: url(https://fonts.googleapis.com/css2?family=Pontano+Sans:wght@400;700) format('woff2');
    unicode-range: U+0100-02AF, U+0304, U+0308, U+0329, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C0, U+2113, U+2C60-2C7F, U+A720-A7FF;
  }
  
  /* Deepika's chosen background-color: #E9CEB0; */
  
  :global(body) {
    background-color: #E9CEB0; 
    margin: 0;
    padding: 0;
    font-family: 'Pontano Sans', sans-serif;
  }
  
  main.custom-background {
    background-color: #E9CEB0; 
    max-width: 100%; 
    margin: 0 auto;
    padding: 20px;
    overflow: hidden;
    height: 15in;
  }
  
  main {
    max-width: 100%; 
    margin: 0 auto;
    padding: 20px;
    color: white;
    overflow: hidden;
    /* height: auto; */
  } 
  
  .header-image {
    width: 100vw; 
    height: 6in; 
    overflow: hidden;
    margin: 0;
    position: relative; 
  }
  
  .header-image img {
    position: absolute; 
    top: 50%; 
    left: 42%;
    width: 100vw; 
    height: auto; 
    min-height: 100%; 
    object-fit: cover;
    object-position: center; 
    transform: translate(-50%, -50%); 
    display: block; 
  }
  
  .header-text {
    position: absolute;
    top: 10px;
    left: 10px;
    color: white;
    font-family: 'adonis-web', sans-serif;
    font-size: 2em;
  }

  .header-text2 {
    position: absolute;
    top: 250px;
    left: 300px;
    color: white;
    font-family: 'adonis-web', sans-serif;
    font-size: 5em;
  }
  
  .account {
    position: absolute;
    top: 10px;
    right: 130px; 
  }
  
  .account-button {
    width: 2in;
    height: 60px;
    background-color: hsla(22.54, 88.72%, 61.76%, 1);
    border: none;
    border-radius: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    color: white;
    font-size: 1em;
    font-family: 'adonis-web', sans-serif;
    cursor: pointer;
    text-align: center;
    line-height: 1.2;
  }
  
  /* .redirect-button:hover {
    background-color: rgba(189, 107, 6, 0.81);
  } */
    
  h1 {
    text-align: center;
    color: black;
    font-family: 'Pontano Sans', sans-serif;
    font-weight: 10;
    font-size: 18px;
    letter-spacing: 1px;
    margin-top: 120px; 
    margin-bottom: 100px;
    width: 650px;
    margin-left: auto; 
    margin-right: auto; 
    line-height: 2;
  }
  
  /* .header-container {
    display: flex; 
    align-items: baseline;
    font-size: 1em;
    font-weight: 100;
    margin-bottom: 10px;
    margin-left: 360px;
  } */
  
  h2 {
    color: rgba(0, 0, 0, 0.954);
    font-family: 'Pontano Sans', sans-serif;
    margin: 0; 
    font-size: 1em;
    font-weight: 100;
    margin-right: 500px; 
    margin-top: 30px;
  }
  
  .password-container {
    display: flex;
    justify-content: center;
    align-items: baseline; 
    font-size: 1em;
    font-weight: 100;
    margin-bottom: 10px;
    margin-left: .08in;
    color: black;  
    /* width: 50vw;  */
  }
  
  .password-input {
    width: 627px;
    height: 60px;
    padding: 10px;
    font-size: 16px;
    font-family: 'Pontano Sans', sans-serif;
    font-weight: 100;
    border: 1px solid rgb(0, 0, 0); 
    border-radius: 30px;
    outline: none;
    background-color: #E9CEB0;
    color: black;
    transition: placeholder-color 0.3s ease; 
  }
  
  .password-input:hover {
    background-color: rgba(255, 255, 255, 0.5); 
  }
  
  h4 {
    font-size: 1em;
    font-weight: 100;
    margin-right: 515px; 
    margin-top: 30px;
  }
  
  .username-container {
    display: flex;
    justify-content: center;
    align-items: baseline; 
    font-size: 1em;
    font-weight: 100;
    margin-bottom: 10px;
    margin-left: .08in;
    color: black;  
    /* width: 50vw;  */
  }

  .username-input {
    width: 627px;
    height: 60px;
    padding: 10px;
    font-size: 16px;
    font-family: 'Pontano Sans', sans-serif;
    font-weight: 100;
    border: 1px solid rgb(0, 0, 0); 
    border-radius: 30px;
    outline: none;
    background-color: #E9CEB0;
    color: black;
    transition: placeholder-color 0.3s ease; 
  }

  .username-input:hover {
    background-color: rgba(255, 255, 255, 0.5);
  }
  
  .submit-button {
    width: 1.4in;
    height: 85px;
    background-color: rgb(0, 0, 0);
    border-radius: 50px;
    color: white;
    padding: 10px 15px;
    cursor: pointer;
    outline: none;
    margin-top: 20px;
    font-family: 'Pontano Sans', sans-serif;
    font-weight: 10;
    font-size: 18px;
    letter-spacing: 0.15em;
  }
  
  .center-button-wrapper {
    display: flex;
    justify-content: center;
    margin-left: -5in;
  }
  
  .submit-button:hover {
    background-color: rgba(189, 107, 6, 0.81);
  }
  
  .loading-indicator {
  position: fixed;
  top: calc(50% + 20px);
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1000;
  display: none; /* Initially hidden */
}

.loading-indicator img {
  width: 150px; /* Adjust as needed */
  height: auto;
}
  

</style>