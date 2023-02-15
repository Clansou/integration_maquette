<script>
// @ is an alias to /src
import MenuButton from '@/components/MenuButton.vue';
export default {
  name: 'HomeView',
  components: {
    MenuButton
  },
}
</script>

<template>
  <aside>
    <img id="Logo" src="../../public/image/Logo.png" alt="Logo">
    <div id="Dashboard">
      <img src="../../public/image/Icone/Dashboard.png" alt="">
      <p>Dashboard</p>
    </div>
    <div id="Menu">
      <MenuButton img="image/Icone/Invoices.png" text="InVoices" />
      <MenuButton img="image/Icone/Clients.png" text="Clients" />
      <MenuButton img="image/Icone/Products.png" text="Products" />
      <MenuButton img="image/Icone/Messages.png" text="Messages" />
      <MenuButton img="image/Icone/Settings.png" text="Settings" />
      <MenuButton img="image/Icone/Help.png" text="Help" />
      <MenuButton class="logout" img="image/Icone/LogOut.png" text="Log Out" />
    </div>
    
  </aside>
  
  
  <div>

  </div>
  <!-- <header>
      <h1>Hi, Rogers</h1>
      <div id="search">
        <img src="../../public/image/Icone/Search.png" alt="">
        <p>Search</p>
      </div>
  </header> -->
</template>


<style>
  body{
    background-color: #1E1E1E;
    color: #FFFFFF;
  }
  #app{
    display: grid;
    grid-template-columns: 3fr 8fr 4fr ;
    padding-top: 54px;
  }
  #Logo{
    margin-bottom: 128px;
  }
  #app>aside{
    margin-left: 52px;
  }
  #Dashboard{
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 13px 29px;
    gap: 17px;
    border-radius:17px;
    background: linear-gradient(266.37deg, #FAFF00 -5.82%, #FAFF00 15.95%, #1970D6 41.2%, #6C1182 72.88%);
    margin-bottom: 44px;
  }
  #Dashboard>p{
    font-weight: 400;
    font-size: 25px;
    line-height: 38px;
    color: #000;
  }
  #Menu{
    color: rgba(255, 255, 255, 0.8)
    
  }
  .logout{
    position: relative;
    bottom: 0;
  }
  header{
    display: flex;
    margin-left: 12px;
    margin-top: 30px;
    align-items: center;
    justify-content: space-between;
    width: 70%;
    height: 93px;
  }
  header>img{
    margin-bottom: 10px;
  }
  h1{
    font-weight: 500;
    font-size: 35px;
    line-height: 52px;
  }
  #search{
    display: flex;
    width: 37%;
    flex-direction: row;
    align-items: center;
    padding-left: 24px;
    gap: 10px;
    background: #FFFFFF;
    border-radius: 15px;
    color: #000;
    }
</style>
