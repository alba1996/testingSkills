<template>
  <div class="alba">
    <div class="menu">
     <ul>
         <li > HOME</li>
         <li >BAND</li>
         <li >TOUR</li>
         <li >CONTACT</li>
         <li >MORE</li>
     </ul>
     <i class="fa fa-search" aria-hidden="true"></i>
   </div>
    <div class="foto">
      <img src="../../static/images/fotos.jpg">
      <div class="shkrimet">
        <div>
          <h1 class="h1-wrapper">Los Angelos</h1>
          <h2>Thank you, Chicago - A night we won't forget</h2>
        </div>

      </div>
    </div>
    <div class="secondPart">
      <h1> THE BAND </h1>
      <h3>We love music</h3>
      <p>
            We have created a fictional band website. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
            et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute
            irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident,
            sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
            magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </p>
    </div>
    <div class="fotot">
      <div class="foto1" v-for="item in items">
        <h3> {{item.name}} </h3>
        <img :src=item.message>
      </div>
    </div>
    <div class="thirdPart">
       <div class="tour">
        <h1>TOUR DATES</h1>
       </div>
       <h3>Remember to book your tickets!</h3>
       <div class="whitewrapper">
         <div class="tour-months">
           <h1>September <span style="color:white;background-color: #F44336">Sold out</span></h1>
         </div>
         <div class="tour-months">
           <h1>October <span style="color:white;background-color: #F44336">Sold out</span></h1>
         </div>
         <div class="tour-months">
           <h1>November<span style="color:white;background-color: black; float: right; border-radius: 50%;width: 20px;height: 20px;border-radius: 50%;text-align: center">3</span></h1>
         </div>
       </div>
       <div class="cityWrapper">
         <div class="city">
           <img src="../../static/images/newyork.jpg">
           <div class="wordsWrapper">
             <h1>New York</h1>
             <h2>Fri 27 Nov 2016</h2>
             <p>Praesent tincidunt sed tellus ut rutrum sed vitae justo.</p>
           </div>
           <div class="buttonwrapper">
               <button>Buy Tickets</button>
           </div>
         </div>
         <div class="city">
           <img src="../../static/images/paris.jpg">
           <div class="wordsWrapper">
             <h1>Paris</h1>
             <h2>Sat 28 Nov 2016</h2>
             <p>Praesent tincidunt sed tellus ut rutrum sed vitae justo.</p>
           </div>
           <div class="buttonwrapper">
             <button>Buy Tickets</button>
           </div>
         </div>
         <div class="city">
           <img src="../../static/images/sanfran.jpg">
           <div class="wordsWrapper">
             <h1>San Francisco</h1>
             <h2>Sun 29 Nov 2016</h2>
             <p>Praesent tincidunt sed tellus ut rutrum sed vitae justo.</p>
           </div>
           <div class="buttonwrapper">
             <button>Buy Tickets</button>
           </div>
         </div>
       </div>
     </div>
    <div class="fourthPart">
      <div class="all-container">
        <h1 class="contact"> CONTACT </h1>
        <h2>Fan? Drop a note!</h2>
        <div class="all-contacts">
          <div class="contact-container">
            <div class="contact-wrapper">
              <div class="ikona">
                <i class="fa fa-map-marker" aria-hidden="true"></i>
              </div>
              <h1>Chicago,US</h1>
            </div>
            <div class="contact-wrapper">
              <div class="ikona">
                <i class="fa fa-phone" aria-hidden="true"></i>
              </div>
              <h1>Phone:+00151515</h1>
            </div>
            <div class="contact-wrapper">
              <div class="ikona">
                <i class="fa fa-envelope" aria-hidden="true"></i>
              </div>
              <h1>Email:mail@mail.com</h1>
            </div>
          </div>
          <div class="inputes">
            <div class="user-wrapper">
              <input type="text" placeholder="Name">
              <input type="email" placeholder="Email">
              <input type="text" placeholder="Message" class="message-input">
            </div>
          </div>
          <div class="butoni">
           <button>SEND</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
 <script>
   export default {
     data () {
       return {
         items: [
           {
             message: '../../static/images/bandmember.jpg',
             name: 'Name'
           },
           {
             message: '../../static/images/bandmember.jpg',
             name: 'alba'
           },
           {
             message: '../../static/images/bandmember.jpg',
             name: 'xhulio'
           }
         ]
       }
     }
   }
 </script>
