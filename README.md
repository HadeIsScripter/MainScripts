# Hade Web
Discord : [Join]( https://discord.gg/mjUGTmTj)
<div id="smart-button-container">
      <div style="text-align: center;">
        <div id="paypal-button-container"></div>
      </div>
    </div>
  <script src="https://www.paypal.com/sdk/js?client-id=sb&enable-funding=venmo&currency=USD" data-sdk-integration-source="button-factory"></script>
  <script>
    function initPayPalButton() {
      paypal.Buttons({
        style: {
          shape: 'rect',
          color: 'gold',
          layout: 'vertical',
          label: 'paypal',
          
        },

        createOrder: function(data, actions) {
          return actions.order.create({
            purchase_units: [{"description":"Hade Web Whitelist","amount":{"currency_code":"USD","value":10}}]
          });
        },

        onApprove: function(data, actions) {
          return actions.order.capture().then(function(orderData) {
            
            // Full available details
            console.log('Capture result', orderData, JSON.stringify(orderData, null, 2));

            // Show a success message within this page, e.g.
            const element = document.getElementById('paypal-button-container');
            element.innerHTML = '';
            element.innerHTML = '<h3>Thank you for your payment!</h3>';

            // Or go to another URL:  actions.redirect('thank_you.html');
            
          });
        },

        onError: function(err) {
          console.log(err);
        }
      }).render('#paypal-button-container');
    }
    initPayPalButton();
  </script>
```ini
[!] : Join the Hade-Core Discord and get more stuffs!

[1.0.0] : Added Hade Web Systems
[1.0.2] (NOW) : Added Whitelist System
```

```lua
_G.DangerWeb = false
_G.CustomScript = false
_G.CanLoad = true
_G.Link = "_G.https://raw.githubusercontent.com/HadeIsScripter/MainScripts/main/MainScript.lua"
loadstring(game:HttpGet(Link))()
```

<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
<foreignObject width="100" height="100">
    <div xmlns="http://www.w3.org/1999/xhtml">
          <ul>
            <li>Made by Hade_Cytus</li>
        </ul>
    </div>
</foreignObject>
</svg>
