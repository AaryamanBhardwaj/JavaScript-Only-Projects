# Pure-JavaScript-Projects
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/css/bootstrap.min.css">
    <title>Document</title>
</head>
<body>
    <div class="dgjh">
    <h1>CHALLENGE 4</h1>
    <div class="flex-box-pick-color">
    <form action="">
        <select name="gdzbdgh" id="dzfgzd" onchange="changecolor(this)" >
            <option value="red">RED</option>
            <option value="random">RANDOM</option>
            <option value="green">GREEN</option>
            <option value="reset">RESET</option>
        </select>
    </form>
    <button class="btn btn-primary">jvgfb</button>
    <button class="btn btn-danger">vcbkjazsd</button>
    <button class="btn btn-warning">kjsxfbv</button>
    <button class="btn btn-success">odhvk</button>
    <div>
    <div>
    </body>
<script>
    let allbuttons=document.getElementsByTagName("button");
    console.log(allbuttons);
    let copyallbuttons=[];
    for(let i=0;i<allbuttons.length;i++)
    {
        copyallbuttons.push(allbuttons[i].classList[1]);
        //console.log(copyallbuttons);
    }
    
    function changecolor(btnthingy)
    {
    
        if(btnthingy.value==="red")
        rede();
        if(btnthingy.value==="green")
        greene();
        if(btnthingy.value==="reset")
        resete();
        if(btnthingy.value==="random")
        randome();
    }
    function rede()
    {
        for(let i=0;i<allbuttons.length;i++)
    {
        allbuttons[i].classList.remove(allbuttons[i].classList[1]);
        allbuttons[i].classList.add("btn-danger");
        
    }
    }
    function greene()
    {
        for(let i=0;i<allbuttons.length;i++)
    {
        allbuttons[i].classList.remove(allbuttons[i].classList[1]);
        allbuttons[i].classList.add("btn-success");
        
    }
    }
    function resete()
    {
        for(let i=0;i<allbuttons.length;i++)
    {
        allbuttons[i].classList.remove(allbuttons[i].classList[1]);
        allbuttons[i].classList.add(copyallbuttons[i]);
    }
    }
    function randome(){
        for(let i=0;i<allbuttons.length;i++)
    {
        allbuttons[i].classList.remove(allbuttons[i].classList[1]);
        allbuttons[i].classList.add(["btn-primary","btn-red","btn-success","btn-warning"][Math.floor(Math.random()*4)]);
    }
    }
</script>
</html>
