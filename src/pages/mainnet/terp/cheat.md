---
layout: '~/layouts/MarkdownLayout.astro'
title: Node CLI Cheatsheet
network: Mainnet
icon: terp
chain: morocco-1
version: barberry
---


<style>
  .my-pre {
    background-color: #1f1f1f;
    color: #c9d1d9;
    font-size: 14px;
    padding: 10px;
    position: relative;
  }
.my-pre .copy-btn {
      background-color: transparent;
      border: none;
      cursor: pointer;
      font-size: 16px;
      position: absolute;
      top: 50%;
      right: 10px;
      transform: translateY(-50%);
    }
    .my-pre .copy-btn:hover {
      color: #c9d1d9;
    }
    .my-pre .copy-btn::before {
      content: "\f0ea";
      font-family: "Font Awesome 5 Free";
      font-weight: 900;
    }


   .input-row {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.input-col {
  width: 48%;
}

.input-group {
  margin-bottom: 20px;
}
#ff03a9f4
.input-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

.input-group input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 16px;
}

.input-group input:focus {
  outline: none;
  border-color: #0000FF;
}

.popup {
		  position: fixed;
		  top: 0;
		  left: 0;
		  width: 100%;
		  height: 100%;
		  background-color: rgba(0, 0, 0, 0.5);
		  display: flex;
		  justify-content: center;
		  align-items: center;
		  z-index: 9999;
		}

		.popup-content {
		  background-color: white;
		  padding: 20px;
		  border-radius: 10px;
		  text-align: center;
		  font-size: 18px;
		  max-width: 80%;
		  max-height: 80%;
		  overflow: auto;
		  color: red;
		}

		.closebtn {
		  position: absolute;
		  top: 10px;
		  right: 10px;
		  font-size: 20px;
		  font-weight: bold;
		  cursor: pointer;
		}
    .input-moci {
  width: calc(50% - 20px);
  margin-bottom: 20px;
}

.input-moci label {
  display: block;
  margin-bottom: 5px;
}

.input-moci input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
.container {
 display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 20px;
}
  ############################## INI ANU NAH WALLET MANAGEMENT #######################
</style>
 <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" />
<h3 for="iwallet">Wallet Management</h3>
<div class="input-group">
  <input id="iwallet" type="text" placeholder="Enter wallet name" oninput="updatePre()" />
</div>

<label for="iwallet" style="vertical-align: top;">1. Create New Wallet</label>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;">terpd keys add <span class="rwallet1"></span> <button class="copy-btn" data-clipboard-text="" onclick="copyText(1)"></button></pre>

<label for="iwallet" style="vertical-align: top;">2. Recovery New Wallet</label>
<pre class="my-pre">terpd keys add <span class="rwallet2"></span> --recover  <button class="copy-btn" data-clipboard-text="" onclick="copyText(2)"></button></pre>

<label for="iwallet" style="vertical-align: top;">3. List All Wallet</label>
<pre class="my-pre">terpd keys list<span class="rwallet3"></span> <span class="rrecipient3"></span> <span class="ramount3"></span>  <span class="rfrom3"></span> <button class="copy-btn" data-clipboard-text="" onclick="copyText(3)"></button></pre>


<label for="iwallet" style="vertical-align: top;">4. Delete Wallet</label>
<pre class="my-pre">terpd keys delete <span class="rwallet4"></span> <button class="copy-btn" data-clipboard-text="" onclick="copyText(4)"></button></pre>

<label for="iwallet" style="vertical-align: top;">5. Export Wallet</label>
<pre class="my-pre">terpd keys export <span class="rwallet5"></span> <button class="copy-btn" data-clipboard-text="" onclick="copyText(5)"></button></pre>

<label for="iwallet" style="vertical-align: top;">6. Import key</label>
<pre class="my-pre">terpd keys import <span class="rwallet6"> </span>.backup <button class="copy-btn" data-clipboard-text="" onclick="copyText(6)"></button></pre>

<label for="iwallet" style="vertical-align: top;">7. Check balance</label>
<pre class="my-pre">terpd q bank balances $(terpd keys show <span class="rwallet7"></span> -a)<button class="copy-btn" data-clipboard-text="" onclick="copyText(7)"></button></pre>


<h3 for="imoniker">Validator Management</h3>
<label for="ivalidator" style="vertical-align: top;">1. Create New Validator</label>
<div class="input-row">
  <div class="input-col">
    <div class="input-group">
      <label for="imoniker">Moniker</label>
      <input id="imoniker" type="text" placeholder="Enter Moniker" oninput="updatePre()" />
    </div>
    <div class="input-group">
      <label for="iidentity">Identity</label>
      <input id="iidentity" type="text" placeholder="Enter Identity" oninput="updatePre()" />
    </div>
    <div class="input-group">
      <label for="idetails">Details</label>
      <input id="idetails" type="text" placeholder="Enter Details" oninput="updatePre()" />
    </div>
  </div>
  <div class="input-col">
    <div class="input-group">
      <label for="iwebsite">Website</label>
      <input id="iwebsite" type="text" placeholder="Enter Website" oninput="updatePre()" />
    </div>
    <div class="input-group">
      <label for="icontact">Contact</label>
      <input id="icontact" type="text" placeholder="Enter Contact" oninput="updatePre()" />
    </div>
    <div class="input-group">
      <label for="iamount">Amount</label>
      <input id="iamount" type="text" placeholder="Enter Amount" oninput="updatePre()" />
    </div>
    <div class="input-group">
      <label for="icommission">Commission</label>
      <input id="icommission" type="text" placeholder="Enter Commission" oninput="updatePre()" />
    </div>
  </div>
</div>


<pre class="my-pre">terpd tx staking create-validator \
--amount=<span class="ramount1"></span>1000000000uthiol \
--moniker="<span class="rmoniker1"></span>" \
--pubkey=$(terpd tendermint show-validator) \
--identity="<span class="ridentity1"></span>" \
--details="<span class="rdetails1"></span>" \
--website="<span class="rwebsite1"></span>" \
--security-contact=<span class="rcontact1"></span> \
--chain-id morocco-1 \
--commission-rate=<span class="rcommission1"></span> \
--commission-max-rate=0.20\
--commission-max-change-rate=0.01 \
--min-self-delegation=1 \
--from=<span class="rwallet8"> \
--gas="auto" \
--gas-prices 0uthiol</pre>

 <label for="imoniker">2. Edit Validator</label>
<div class="container">
<div class="input-group">
      <label for="ieditmoniker">New Moniker</label>
      <input id="ieditmoniker" type="text" placeholder="Enter New Moniker" oninput="updatePre()" />
    </div>
<div class="input-group">
      <label for="ieditidentity">New identity</label>
      <input id="ieditidentity" type="text" placeholder="Enter New identity" oninput="updatePre()" />
    </div>
<div class="input-group">
      <label for="ieditdetails">New Details</label>
      <input id="ieditdetails" type="text" placeholder="Enter New Details" oninput="updatePre()" />
    </div>
  <div class="input-group">
      <label for="ieditweb">New Website</label>
      <input id="ieditweb" type="text" placeholder="Enter New Website" oninput="updatePre()" />
    </div>
</div>
  </div>
  </div>

<pre class="my-pre">
terpd tx staking edit-validator \
--new-moniker="<span class="reditmoniker1"></span>" \
--identity="<span class="reditidentity1"></span>" \
--details="<span class="reditdetails1"></span>" \
--website="<span class="reditweb1"></span>" \
--chain-id morocco-1 \
--commission-rate=0.07 \
--from=<span class="rwallet9"> \
--gas="auto" \
--gas-prices="0uthiol"</pre>


<label for="iwallet" style="vertical-align: top;">3. Unjail Validator</label>
<pre class="my-pre"> terpd tx slashing unjail --broadcast-mode=block --from <span class="rwallet10">  </span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"
</pre>

<label for="iwallet" style="vertical-align: top;">4. Jail Reason</label>
<pre class="my-pre">terpd query slashing signing-info $(terpd tendermint show-validator)<span class="rwallet3"></span> <span class="rrecipient3"></span> <span class="ramount3"></span>  <span class="rfrom3"></span> </pre>

<label for="iwallet" style="vertical-align: top;">5. View validator details</label>
<pre class="my-pre"> terpd q staking validator $(terpd keys show <span class="rwallet11"></span> --bech val -a)
</pre>


<h3 for="imoniker">Token Management</h3>
<label for="ivalidator" style="vertical-align: top;">1. Withdraw rewards from all validators</label>
<pre class="my-pre"> terpd tx distribution withdraw-all-rewards --from <span class="rwallet12"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"</pre>

<label for="ivalidator" style="vertical-align: top;">2. Withdraw commission and rewards from your validator</label>
<pre class="my-pre"> terpd tx distribution withdraw-rewards $(terpd keys show <span class="rwallet13"></span> --bech val -a) --commission --from <span class="rwallet14"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"</pre>

<div class="input-group">

<label for="idelegetet" style="vertical-align: top;">3. Delegate tokens to yourself</label>
  <input id="idelegete" type="text" placeholder="Enter Amount" oninput="updatePre()" />
</div>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;">terpd tx staking delegate $(terpd keys show <span class="rwallet15"></span> --bech val -a) <span class="rdelegete1"></span>1000000000uthiol --from <span class="rwallet16"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"  </pre>

 <div class="input-group">

<label for="iredelegetet" style="vertical-align: top;">4. Redelegate tokens to another validator</label>
  <input id="iredelegete" type="text" placeholder="Enter <TO_VALOPER_ADDRESS>" oninput="updatePre()" />
</div>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;"> terpd tx staking redelegate $(terpd keys show <span class="rwallet17"></span> --bech val -a) <span class="rredelegete1"></span> <span class="rdelegete2"></span>10000000uthiol --from <span class="rwallet18"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"
</pre>

<label for="iredelegetet" style="vertical-align: top;">5. Delegate tokens to validator</label>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;"> terpd tx staking delegate <span class="rredelegete2"></span> <span class="rdelegete3"></span>1000000000uthiol --from <span class="rwallet19"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"
 </pre>

<label for="iredelegetet" style="vertical-align: top;">6. Unbond tokens from your validator</label>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;"> terpd tx staking unbond $(terpd keys show <span class="rwallet20"></span> --bech val -a) <span class="rdelegete4"></span>1000uthiol --from <span class="rwallet21"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"
</pre>
</div>

<div class="input-group">

<label for="idelegetet" style="vertical-align: top;">7. Send tokens to Any wallet</label>
  <input id="itoken" type="text" placeholder="Enter Address Wallet" oninput="updatePre()" />

</div>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;">
terpd tx bank send<span class="rwallet22"></span> <span class="rtoken1"></span> <span class="rdelegete5"></span>1000000000uthiol --from <span class="rwallet23"></span> --chain-id morocco-1 --gas="auto" --gas-prices="0uthiol"
</pre></div>

<h3 for="iwallet">Costum Port</h3>
<div class="input-group ">
  <input id="iport" type="text" placeholder="Enter Costum Port" oninput="updatePre()" />
</div>
 <pre class="my-pre" id="pre1" style="margin-top: 5px;">CUSTOM_PORT=<span class="rport1"></span>
sed -i.bak -e "s%^proxy_app = \"tcp://127.0.0.1:26658\"%proxy_app = \"tcp://127.0.0.1:${CUSTOM_PORT}658\"%; s%^laddr = \"tcp://127.0.0.1:26657\"%laddr = \"tcp://127.0.0.1:${CUSTOM_PORT}657\"%; s%^pprof_laddr = \"localhost:6060\"%pprof_laddr = \"localhost:${CUSTOM_PORT}060\"%; s%^laddr = \"tcp://0.0.0.0:26656\"%laddr = \"tcp://0.0.0.0:${CUSTOM_PORT}656\"%; s%^prometheus_listen_addr = \":26660\"%prometheus_listen_addr = \":${CUSTOM_PORT}660\"%" $HOME/.terp/config/config.toml
sed -i.bak -e "s%^address = \"tcp://0.0.0.0:1317\"%address = \"tcp://0.0.0.0:${CUSTOM_PORT}317\"%; s%^address = \":8080\"%address = \":${CUSTOM_PORT}080\"%; s%^address = \"0.0.0.0:9090\"%address = \"0.0.0.0:${CUSTOM_PORT}090\"%; s%^address = \"0.0.0.0:9091\"%address = \"0.0.0.0:${CUSTOM_PORT}091\"%" $HOME/.terp/config/app.toml  ></pre>  </div>
 </div>

<script>
  function updatePre() {
    const walletInput = document.getElementById('iwallet').value.trim();
    document.querySelector('.rwallet1').textContent = walletInput;
    document.querySelector('.rwallet2').textContent = walletInput;
    document.querySelector('.rwallet4').textContent = walletInput;
    document.querySelector('.rwallet5').textContent = walletInput;
    document.querySelector('.rwallet6').textContent = walletInput;
    document.querySelector('.rwallet7').textContent = walletInput;
    document.querySelector('.rwallet8').textContent = walletInput;
    document.querySelector('.rwallet9').textContent = walletInput;
    document.querySelector('.rwallet10').textContent = walletInput;
    document.querySelector('.rwallet11').textContent = walletInput;
    document.querySelector('.rwallet12').textContent = walletInput;
    document.querySelector('.rwallet13').textContent = walletInput;
    document.querySelector('.rwallet14').textContent = walletInput;
     document.querySelector('.rwallet15').textContent = walletInput;
      document.querySelector('.rwallet16').textContent = walletInput;
        document.querySelector('.rwallet17').textContent = walletInput;
          document.querySelector('.rwallet18').textContent = walletInput;
          document.querySelector('.rwallet19').textContent = walletInput;
          document.querySelector('.rwallet20').textContent = walletInput;
          document.querySelector('.rwallet21').textContent = walletInput;
          document.querySelector('.rwallet22').textContent = walletInput;
          document.querySelector('.rwallet23').textContent = walletInput;

    const monikerInput = document.getElementById('imoniker').value.trim();
    document.querySelector('.rmoniker1').textContent = monikerInput;

     const identityInput = document.getElementById('iidentity').value.trim();
    document.querySelector('.ridentity1').textContent = identityInput;
   
   const detailsInput = document.getElementById('idetails').value.trim();
    document.querySelector('.rdetails1').textContent = detailsInput;

    const websiteInput = document.getElementById('iwebsite').value.trim();
    document.querySelector('.rwebsite1').textContent = websiteInput;

    const contactInput = document.getElementById('icontact').value.trim();
    document.querySelector('.rcontact1').textContent = contactInput;

    const amountInput = document.getElementById('iamount').value.trim();
    document.querySelector('.ramount1').textContent = amountInput;
    
    const commissionInput = document.getElementById('icommission').value.trim();
    document.querySelector('.rcommission1').textContent = commissionInput;

    const editmonikerInput = document.getElementById('ieditmoniker').value.trim();
    document.querySelector('.reditmoniker1').textContent = editmonikerInput;
    
    const editidentityInput = document.getElementById('ieditidentity').value.trim();
    document.querySelector('.reditidentity1').textContent = editidentityInput;

     const editdetailsInput = document.getElementById('ieditdetails').value.trim();
    document.querySelector('.reditdetails1').textContent = editdetailsInput;

    const editwebInput = document.getElementById('ieditweb').value.trim();
    document.querySelector('.reditweb1').textContent = editwebInput;

    const delegeteInput = document.getElementById('idelegete').value.trim();
    document.querySelector('.rdelegete1').textContent = delegeteInput;
      document.querySelector('.rdelegete2').textContent = delegeteInput;
document.querySelector('.rdelegete3').textContent = delegeteInput;
document.querySelector('.rdelegete4').textContent = delegeteInput;
document.querySelector('.rdelegete5').textContent = delegeteInput;
    const redelegeteInput = document.getElementById('iredelegete').value.trim();
    document.querySelector('.rredelegete1').textContent = redelegeteInput;
       document.querySelector('.rredelegete2').textContent = redelegeteInput;

const tokenInput = document.getElementById('itoken').value.trim();
    document.querySelector('.rtoken1').textContent = tokenInput;

    const portInput = document.getElementById('iport').value.trim();
    document.querySelector('.rport1').textContent = portInput;
  }

  function copyText(index) {
    const preElement = document.querySelector(`.rwallet${index} .rmoniker .ridentity .rdetails .rwebsite .rcontact .ramount `).parentNode;
    const text = preElement.textContent.trim();
    navigator.clipboard.writeText(text)
      .then(() => {
        console.log('Text copied to clipboard');
      })
      .catch(err => {
        console.error('Failed to copy text: ', err);
      });
  }

		function closePopup() {
			document.getElementById("popup").style.display = "none";
		}

		window.onclick = function(event) {
			if (event.target == document.getElementById("popup")) {
				closePopup();
			}
		}

</script>
