# Pure-JavaScript-Projects
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
  <h1>challenge 3</h1>
  <div id='box'>
    <img src="https://th.bing.com/th/id/OIP.LJ5Hj0ev5uzyVVnbgUgTUgHaE8?w=267&h=180&c=7&o=5&dpr=1.25&pid=1.7" alt="" onclick="rps(this)" id="rock">
    <img src="https://th.bing.com/th/id/OIP.HhIk_8qAW2Zhz64Qsr_YhQHaE7?w=254&h=180&c=7&o=5&dpr=1.25&pid=1.7" alt="" onclick="rps(this)" id="paper">
    <img src="https://th.bing.com/th/id/OIP.z5ZQPoGN64Jag3Rr0Ua6mAHaHl?w=179&h=183&c=7&o=5&dpr=1.25&pid=1.7" alt="" onclick="rps(this)" id="scissors">
  </div>
  
  <script>
      function rps(yourchoice){
          console.log(yourchoice);
          var humanchoice,botchoice;
          botchoice=["rock","paper","scissors"][Math.floor(Math.random()*3)];
          //console.log("computer choice", botchoice);
          //yourchoice.id-it will pass that element's ID(this keyword gives us the element,so yourchoice's value is that element and yourchoice.id will give that elemenet;s id)
          results=decidewinner(yourchoice.id,botchoice);
          //console.log(results);
          message=finalmessage(results);
          //console.log(message);
          let imagedatabase={
             "rock":document.getElementById("rock").src,
             "paper":document.getElementById("paper").src,
             "scissors":document.getElementById("scissors").src
         }
         //lets remove all the images
         document.getElementById("rock").remove();
         document.getElementById("paper").remove();
         document.getElementById("scissors").remove();
         var humandiv=document.createElement("div");
         var botdiv=document.createElement("div");
         var messagediv=document.createElement("div");
         humandiv.innerHTML="<img src='"+imagedatabase[yourchoice.id]+"'>";
         messagediv.innerHTML="<h1>" +message.a +"</h1>";
         botdiv.innerHTML="<img src='"+imagedatabase[botchoice]+"'>";
         document.getElementById('box').appendChild(humandiv);
         document.getElementById('box').appendChild(messagediv);
         document.getElementById('box').appendChild(botdiv);
          
      }
      function decidewinner(yourchoice,computerchoice){
          var rpsdatabase={
            "rock":{"scissors":1,"paper":0,"rock":0.5},
            "paper":{"scissors":0,"paper":0.5,"rock":1},
            "scissors":{"scissors":0.5,"paper":1,"rock":0}
          }
          var yourscore=rpsdatabase[yourchoice][computerchoice];//console.log(yourscore);
          //var computerscore=rpsdatabase[computerchoice][yourchoice];console.log(computerscore);
          return [yourscore];
      }
      function finalmessage([yourscore]){
        if(yourscore===0)
         {
             return {a:"U LOSAT"};//it is returning an object
         }
         else if(yourscore===0.5)
         {return {a:"DRAW"};}
         else
         {return {a: "U WON"};}
    }
  </script>
</body>
</html>
