## 	Input Filed Text Animation
### Codigo


`HTML`
~~~
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="css/style.css">
    <title>Input Field Text Animation</title>
</head>
<body>
    <div class="inputBox">
        <input type="text" required="required">
        <span>First Name</span>
    </div>
    <div class="inputBox">
        <input type="text" required="required">
        <span>Last Name</span>
    </div>    
    <div class="return">
        <a href="../../index.html"> Regresar </a>
    </div>
</body>
</html>
~~~

`CSS`
~~~
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap');
*
{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
body
{
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        flex-direction: column;
        gap: 30px;
        background: #1d2b3a;
}

.inputBox
{
    position: relative;
    width: 250px;
}

.inputBox input
{
    width: 100%;
    padding: 10px;
    border: 1px solid rgba(255,255,255,0.25);
    background: #1d2b3a;    
    border-radius: 5px;
    outline: none;
    color: #fff;
    font-size: 1em;
    transition: 0.5s;
}

.inputBox span
{
    position: absolute;
    left: 0;
    padding: 10px;
    pointer-events: none;
    font-size: 1em;
    color: rgba(255,255,255,0.25);
    text-transform: uppercase;
    transition: 0.5s;
}

.inputBox input:valid ~ span,
.inputBox input:focus ~ span
{
    color: #00dfc4;
    transform: translateX(10px) translateY(-7px);
    font-size: .85em;
    padding: 0 10px;
    background: #1d2b3a;
    border-left: 1px solid #00dfc4;
    border-right: 1px solid #00dfc4;  
    letter-spacing: 0.2em;  
}

.inputBox:nth-child(2) input:valid ~ span,
.inputBox:nth-child(2) input:focus ~ span
{
        background: #00dfc4;
        color: #1d2b3a;
        border-radius: 2px;
}

.inputBox input:valid,
.inputBox input:focus
{
    border: 1px solid #00dfc4;
}

.return a
{
    color: #00dfc4;
}
~~~

