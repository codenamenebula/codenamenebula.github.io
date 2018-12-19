---
layout: page
title: Contact
---

<form id="form" action="https://getsimpleform.com/messages?form_api_token=cb6647cf30878ba7ded34b2340bf2963" method="post">
  <div class="list-cell">
    <input type='text' autocomplete="off" id='email' name='email' placeholder='Your Email' onkeydown="if(event.keyCode==13)return false;" />
  </div>
  <div class="list-cell">
    <textarea name="message" id="message" rows='8' placeholder='content (length > 6)'></textarea>
  </div>
  <div class="btn-row list-cell">
    <button id="submitBtn" type="button">send</button> 
  </div>
</form>
<script>
    window.onload=function(){
        var Email =document.getElementById("email");
        var Message =document.getElementById("message");
        var Form =document.getElementById("form");
        var emailText =Email.value.trim();
        var messageText =Message.value.trim();
        var Reg =/^[a-zA-Z0-9_.-]+@[a-zA-Z0-9-]+(\.[a-zA-Z0-9-]+)*\.[a-zA-Z0-9]{2,6}$/;
        document.getElementById("submitBtn").onclick=function(){
            if(Reg.test(emailText) && messageText.length > 6){
                document.getElementById("form").submit();
            }else{
                alert("请您老把信息填完整,填正确😊");
            }
        }
    }
</script>
