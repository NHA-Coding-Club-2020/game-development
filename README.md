# NHA Coding Club 2020 - Build a Game in HTML, CSS, and JavaScript
We're going to build a game!

# Feb 28, 2020 Assignment
Step 1. From the 022820 branch open Gitpod

Step 2. Create your own branch called "your-name" (for example: eric-hendrickson would be my branch name)

Step 3. Create a new file called "game.html"

Step 4. Add the following HTML code - STOP AND SHOW!

```
<html>
<head>
<title>This is a title!</title>
</head>
<body>
<div class="wrapper">
    <div>
    If you click me, then I'll go away!
    </div>

    <div>
    If you click me, then... 
    </div>
</div>
</body>
</html>
```

Step 5. Update the ```<div>``` tags with inline styles like below - STOP AND SHOW!

```
    <div style="font-size:20px; cursor: pointer;">
    If you click me, then I'll go away!
    </div>

    <div style="color: red; cursor: pointer;">
    If you click me, then... 
    </div>
```

Step 6. Add the following CSS style tag code above ```<div>``` with the ```class="wrapper"``` - STOP AND SHOW!

```
<style>
   .wrapper {
       height: 50%;
       border: 0px red solid;
       margin-top: 50px;
       margin-bottom: 50px;       
       margin-left: 50px;
       margin-right: 50px;
   }
   
   .wrapper div {
       padding: 3px;
   }
</style>
```

Step 7. Add the following ```<script>``` tag below the last ```<div>``` tag - STOP AND SHOW!

```
<script>
    $(".wrapper div:first()").on("click", 
    function(){ 
        $(this).hide(); 
    });

    $(".wrapper div:last()").on("click", 
    function(){ 
        window.alert("...see what I say!")
    });
</script>
```

Step 8. Add the following two ```<button>``` tags to your ```<div class="wrapper">``` tag - STOP AND SHOW!

```
    <button class="reset-all">Reset</button>
    <button class="hide-all">Hide Everything</button>
```

Step 9. Add the following JavaScript to your ```<script>``` tag - STOP AND SHOW!

```
    $(".reset-all").on("click",
    function(){
        $(".wrapper div").show();
    });
    
    $(".hide-all").on("click",
    function(){
        $(".wrapper div").hide();
    });
```

Step 10. Add the following JavaScript to your ```<script>``` tag - STOP AND SHOW!

```
    $(".wrapper div").on("mouseenter", 
    function() {
        $(this).css("background", "grey");
    });

    $(".wrapper div").on("mouseleave", 
    function() {
        $(this).css("background", "white");
    });
```