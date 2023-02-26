<script>
// @ is an alias to /src
import MenuButton from '@/components/MenuButton.vue';
import TransactionComponent from '@/components/TransactionComponent.vue';
import TransactionAsideComponent from '@/components/TransactionAsideComponent.vue';
import AssetsComponent from '@/components/AssetsComponent.vue';
export default {
  name: 'HomeView',
  components: {
    MenuButton,
    TransactionComponent,
    TransactionAsideComponent,
    AssetsComponent,
  },
  mounted(){
    var sidenav = document.getElementById("Aside1");
    var openBtn = document.getElementById("openBtn");
    var closeBtn = document.getElementById("closeBtn");

    openBtn.onclick = openNav;
    closeBtn.onclick = closeNav;

    /* Set the width of the side navigation to 250px */
    function openNav() {
      sidenav.classList.add("active");
    }

    /* Set the width of the side navigation to 0 */
    function closeNav() {
      sidenav.classList.remove('active');
    }
  }
}
</script>

<template>
  
  <aside id="Aside1">
    <a id="closeBtn" href="#" class="close">×</a>
    <img id="Logo" src="../../public/image/Logo.png" alt="Logo">
    <div id="profil2">
      <img src="../../public/image/Notification.png" alt="">
      <img src="../../public/image/Profil.png" alt="">
    </div>
    <button id="Dashboard">
      <img src="../../public/image/Dashboard.png" alt="">
      <p>Dashboard</p>
    </button>
    <div id="Menu">
      <MenuButton img="image/Icone/Invoices.png" text="Invoices" />
      <MenuButton img="image/Icone/Clients.png" text="Clients" />
      <MenuButton img="image/Icone/Products.png" text="Products" />
      <MenuButton img="image/Icone/Messages.png" text="Messages" />
      <MenuButton img="image/Icone/Settings.png" text="Settings" />
      <MenuButton img="image/Icone/Help.png" text="Help" />
      <MenuButton class="logout" img="image/Icone/LogOut.png" text="Log Out" />
    </div>
    
  </aside>
  
  <main>
    <header>
      <h1>Hi, Rogers</h1>
      <div id="search">
        <img src="../../public/image/Search.png" alt="">
        <input placeholder="Search">
      </div>
    </header>
    <div class="InfoGraph">
      <div>
        <p>Total Balance</p>
        <div id="BTC"><p>0.97894652</p><p class="BTC_Text">BTC</p></div>
        <p>$40,123.56</p>
      </div>
      <nav>
        <a class="active">Portfolio</a>
        <a>Funding</a>
        <a>Assets</a>
        <a>P2P</a>
      </nav>
    </div>
    
    <img src="../../public/image/Graphique.png" alt="">
    <div id="Transactiondiv">
      <div>
        <p>Recent Transactions </p>
        <a>See all coins</a>
      </div>
      <TransactionComponent img="image/Crypto/Bitcoin3.png" subimg="image/transactionCurve1.png" name="Bitcoin" subname="BTC" activeColor1="blue" activeColor2="green"/>
      <TransactionComponent img="image/Crypto/Etherum2.png" subimg="image/transactionCurve2.png" name="Etherum" subname="ETH" activeColor1="purple" activeColor2="red"/>
    </div>
  </main>
  <aside id="Aside2">
    <div id="profil1">
      <img src="../../public/image/Notification.png" alt="">
      <img src="../../public/image/Profil.png" alt="">
    </div>
    <p>Recent Transactions</p>
    <div id="TransactionAside">
      <TransactionAsideComponent img="image/Crypto/Usdt.png" name="Usdt" state="Received" price="+ 3,546" date="Today, 13:45 " activeColor1="green"/>
      <TransactionAsideComponent img="image/Crypto/BNB.png" name="BNB" state="Buy" price="+ 0.7546" date="Today, 5:45 " activeColor1="green"/>
      <TransactionAsideComponent img="image/Crypto/LiteCoin.png" name="LiteCoin" state="Received" price="+ 0.7546" date="Today 7:55 " activeColor1="red"/>
      <TransactionAsideComponent img="image/Crypto/Bitcoin.png" name="Bitcoin" state="Received" price="+ 2.7546" date="Today, 8:55 " activeColor1="green"/>
      <TransactionAsideComponent img="image/Crypto/Etherum.png" name="Etherum" state="Received" price="+ 1.646" date="Today, 10:02 " activeColor1="green"/>
    </div>
    <p>Assets</p>
    <div id="Assets">
      <AssetsComponent color="white" img="image/Crypto/Bitcoin2.png" name="Bitcoin" quantity="121,6450.45" subname="BTC" background="linear-gradient(98.73deg, #611D8D 35.75%, #2F7EC1 73.26%)"/>
      <AssetsComponent color="black" img="image/Crypto/Etherum2.png" name="Etherum" quantity="143,850.45" subname="ETH" background="linear-gradient(99.56deg, #FAFF00 35.82%, #29ABE2 64.75%, rgba(255, 255, 255, 0.7) 91.33%)"/>
    </div>
  </aside>
  <a href="#" id="openBtn">
    <span class="burger-icon">
      <span></span>
      <span></span>
      <span></span>
    </span>
  </a>
</template>


<style>
*{
  margin: 0px;
  box-sizing: border-box;
  padding: 0px;
  font-family: "Poppins";

}
#closeBtn{
  display: none;
}
  body{
    background-color: #1E1E1E;
    color: #FFFFFF;
    font-size: 22px;
    
  }
  #app{
    display: grid;
    grid-template-columns: 3fr 8fr 5fr ;
    padding-top: 54px;
  }
  #Logo{
    margin-bottom: 128px;
  }
  aside{
    margin-right: 24px;
    margin-left: 24px;
    position: relative;
  }
  #Dashboard{
    width: min-content;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 10px 29px;
    gap: 17px;
    border-radius:17px;
    background: linear-gradient(266.37deg, #FAFF00 -5.82%, #FAFF00 15.95%, #1970D6 41.2%, #6C1182 72.88%);
    margin-bottom: 44px;
    border: 0;
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
    position: absolute;
    bottom: 12px;
  }

  #Aside1.active {
  display: block;
  left: 0;
}

#Aside1 .close {
  position: absolute;
  top: 10px;
  right: 25px;
  font-size: 36px;
}
.burger-icon span {
  display: block;
  width: 35px;
  height: 5px;
  background-color: black;
  margin: 6px 0;
}
#openBtn{
  display: none;
  position: absolute;
  top: 10px;
  left: 10px;
}



  header{
    margin-top: 8px;
    display: flex;
    gap: 24px;
    height: 6vh;
  }
  h1{
    font-weight: 500;
    font-size: 35px;
    line-height: 52px;
    width: 40%;
  }
  #search{
    display: flex;

    flex-direction: row;
    align-items: center;
    padding-left: 24px;
    width: 50%;
    gap: 10px;
    background: #FFFFFF;
    border-radius: 15px;
    color: #000;
    }
  #search>input{
    width: 100px;
    border: 0;
    font-size: 22px;
  }
  #search ::placeholder{
    opacity: 1;
    color: #000;
  }




  .InfoGraph{
    margin-top: 54px;
    display: grid;
    grid-template-columns: 3fr 5fr;
  }
  .InfoGraph>div{
    display: flex;
    font-size: 22px;
    flex-direction: column;
    margin-left: 16px;
    gap: 16px;
  }
  .InfoGraph>div>p:nth-child(1){
    opacity: 0.8;
  }
  .InfoGraph>div>p:nth-child(3){
    opacity: 0.7;
  }
  #BTC{
    font-size: 29px;

    display: flex;
    gap: 8px;
    color: #FFFFFF;
    align-items: center;
  }
  .BTC_Text{
    color: #000;
    font-size: 15px;
    padding: 4px 8px;
    background: #FAFF00;
    border-radius: 8px;;
  }
  .InfoGraph>nav{
    display: flex;
    gap: 16px;
    padding: 8px 16px;
    background: #292727;
    border-radius: 17px;
    align-items: center;
    height: fit-content;
    width: fit-content;
    margin-top: auto;
    margin-bottom: auto;
    font-size: 22px;
  }
  .InfoGraph>nav>.active{
    padding: 8px 24px;
    background: #0D0C0C;
    border-radius: 17px;
  }
  main>img{
    width: 100%;
    margin-top: 42px;
  }

  #Transactiondiv{
    display: flex;
    flex-direction: column;
    gap: 16px;
    margin-left: 12px;
    margin-top: 24px;
  }
  #Transactiondiv> :nth-child(1){
    width: 90%;
    display: flex;
    justify-content: space-between;
    margin-left: auto;
    margin-right: auto;
  }




  #profil2{
    display: none;
  }
  #profil1{
    display: flex;
    margin-bottom: 60px;
  }
  #profil1>img{
    height: fit-content;
    margin-top: auto;
    margin-bottom: auto;
  }
  #profil1 :nth-child(2){
    margin-left: auto;
  }
  

  aside>p{
    margin-bottom: 16px;
  }
  #TransactionAside{
    display: flex;
    flex-direction: column;
    margin-bottom: 60px;
  }
  #Assets{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    gap: 18px;
  }


  @media (max-width: 1400px) { 
    #Aside1{
      display: none;
    }
    #openBtn{
  display: block;
  position: absolute;
  top: 10px;
  left: 10px;
}
  #closeBtn{
  display: block;
  }
    #app{
      grid-template-columns: 7fr 4fr;
    }
    h1{
      margin-left: 12px;
    }
    #Aside1{
      position: fixed;
      top: 0;
      background-color: #000;
      margin: 0;
      height: 100vh;
      z-index: 10;
    }
    #Dashboard{
      margin-left: 12px;
      margin-right: 12px;
    }
   }
   @media (max-width: 1000px) {
    #app{
      grid-template-columns: 1fr;
      margin: 0 24px;
    }
    #profil1{
      display: none;
    }
    #profil2{
      display: block;
    }
    #profil2{
    display: flex;
    margin-left: 12px;
    margin-right: 12px;
    margin-bottom: 60px;
    }
    #profil2>img{
      height: fit-content;
      margin-top: auto;
      margin-bottom: auto;
    }
    #profil2 :nth-child(2){
      margin-left: auto;
    }
    #Logo{
      margin-bottom: 30px;
    }
    #Assets{
      flex-direction: row;
      flex-wrap: wrap;
    }
    main{
      margin-right: 24px;
    }
    #TransactionAside>div>div{
      margin-left: auto;
      margin-right: auto;
    }
    #TransactionAside>div>img{
      margin-left: 40px
    }
    aside>p{
    margin-top: 32px;
    margin-bottom: 32px;
    }

   }
   @media (max-width: 700px) {
    .InfoGraph{
      grid-template-columns: 1fr;
    }
    .InfoGraph>div{
      display: flex;
      flex-wrap: wrap;
      flex-direction: row;
      align-items: center;
      margin-top: 12px;
      margin-bottom: 24px;
    }
   }
   @media (max-width: 500px) {
    #TransactionAside>div>img {
      margin-left: 0;
    }
    header{
      flex-direction: column;
      height: auto;
    }
    h1{
      width: auto;
    }
    #search{
      width: 80%;
      margin-left: auto;
      margin-right: auto;
      padding: 12px ;
    }
    nav{
      flex-wrap: wrap;
    }
    div,header,aside{
      margin-left: 0 !important;
      margin-right: 0 !important;
    }
    body{
      margin-left: 12px !important;
      margin-right: 12px !important;
    }
    #profil2{
      margin-left: 12px !important;
      margin-right: 12px !important;
    }
    #Aside1{
      width: 100%;
    }
    
  }
  @media (max-width: 400px) {
    #Transactiondiv :nth-child(1){
      flex-direction: column;
    }
  }
   


  
</style>
