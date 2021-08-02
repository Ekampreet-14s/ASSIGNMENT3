	<html>
    <head>
        <title>Document</title>
  <link rel="stylesheet" href="style.css">
    </head>
<style>
*{
    margin:0;
    padding:0;
    box-sizing: border-box;
}
html,body{
    display:grid;
    height:100%;
    place-items: center;
    background: black;
}
.center{
    display: flex;
    text-align: center;
    align-items: center;
    justify-content: center;
}
.outer{
    position: relative;
    margin:0 50px;
    background: orange;
}
.button{
    height: 70px;
    width: 220px;
    border-radius:50px;
}
.circle{
    height: 200px;
    width: 200px;
    border-radius: 50%;
}
.outer button, .outer span{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.outer button{
    background: #111;
    color: #f2f2f2;
    outerline: none;
    border: none;
    font-size: 20px;
    z-index: 9;
    letter-spacing: 1px;
    text-transform: uppercase;
    cursor: pointer;
}

.button button{
    height: 60px;
    width: 210px;
    border-radius: 50px;
}
.circle button{
    height: 180px;
    width: 180px;
    border-radius: 50%;
}
.outer span{
    height: 100%;
    width: 100%;
    background: inherit;
}
 .button span{
    border-radius: 50px;
}
.circle span{
    border-radius: 50%;
}
.outer:hover span:nth-child(1){
    filter: blur(7px);
}
.outer:hover span:nth-child(2){
    filter: blur(14px);
}
.outer:hover{
    background: red;
    
}
@keyframes rotate {
    0%{
        filter: hue-rotate(0deg);
    }
    100%{
         filter: hue-rotate(360deg);
    }
}
    @media (max-width: 640px)
    {
.center{
    flex-wrap: wrap;
    flex-direction: column;
    
}
.outer{
    margin: 50px 0px;
}
    }
    </style>
<body>
    <div class="center">
         <div class="outer button">
            <button>Hover Me</button>
            <span></span>
            <span></span>
        </div> 
        
    </div>
</body>
</html>
