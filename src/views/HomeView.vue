<script>
// @ is an alias to /src
import MenuButton from '@/components/MenuButton.vue';
import TransactionComponent from '@/components/TransactionComponent.vue';
import TransactionAsideComponent from '@/components/TransactionAsideComponent.vue';
export default {
  name: 'HomeView',
  components: {
    MenuButton,
    TransactionComponent,
    TransactionAsideComponent
  },
}
</script>

<template>
  <aside>
    <img id="Logo" src="../../public/image/Logo.png" alt="Logo">
    <button id="Dashboard">
      <img src="../../public/image/Icone/Dashboard.png" alt="">
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
        <img src="../../public/image/Icone/Search.png" alt="">
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
  <aside>
    <div id="profil">
      <img src="../../public/image/Icone/Notification.png" alt="">
      <img src="../../public/image/Profil.png" alt="">
    </div>
    <p>Recent Transactions</p>
    <div id="TransactionAside">
      <TransactionAsideComponent img="image/Crypto/Usdt.png" name="Usdt" state="Received" price="+ 3,546" date="Today, 13:45 pm" activeColor1="green"/>
      <TransactionAsideComponent img="image/Crypto/BNB.png" name="BNB" state="Buy" price="+ 0.7546" date="Today, 5:45 am" activeColor1="green"/>
      <TransactionAsideComponent img="image/Crypto/LiteCoin.png" name="LiteCoin" state="Received" price="+ 0.7546" date="Today 7:55 am" activeColor1="red"/>
      <TransactionAsideComponent img="image/Crypto/Bitcoin.png" name="Bitcoin" state="Received" price="+ 2.7546" date="Today, 8:55 am" activeColor1="green"/>
      <TransactionAsideComponent img="image/Crypto/Etherum.png" name="Etherum" state="Received" price="+ 1.646" date="Today, 10:02 am" activeColor1="green"/>
    </div>
    <p>Assets</p>
  </aside>
</template>


<style>
*{
  margin: 0px;
  box-sizing: border-box;
  padding: 0px;
  font-family: "Poppins";

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
    margin-right: 40px;
    margin-left: 40px;
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
  #Transactiondiv>div{
    width: 90%;
    display: flex;
    justify-content: space-between;
    margin-left: auto;
    margin-right: auto;
  }





  #profil{
    display: flex;
    margin-bottom: 100px;
  }
  #profil>img{
    height: fit-content;
    margin-top: auto;
    margin-bottom: auto;
  }
  #profil :nth-child(2){
    margin-left: auto;
  }

  aside>p{
    margin-bottom: 32px;
  }
  #TransactionAside{
    display: flex;
    flex-direction: column;
    gap: 24px;
    margin-bottom: 32px;
  }
  
</style>
