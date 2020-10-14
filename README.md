<?php

$server = "localhost";
$username = "root";
$password ="";

$con = mysqli_connect($server,$username,$password);

if(!$con)
{
    die("connection failed");
}
$first_name = $_POST['first-name'];
$last_name = $_POST['last-name'];
$email = $_POST['email'];
$phone = $_POST['phone'];
$sem = $_POST['sem'];
$year = $_POST['year'];
$sql = "INSERT INTO `victim`.`data` ( `first-name`, `last-name`, `email`, `phone`, `sem`, `year`) VALUES ('$first_name', '$last_name', '$email', '$phone', '$sem', '$year')";
}

    $con->close();

?>













<html lang="">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;1,100;1,300&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="stylesheet.css">
    <title>sign page</title>
</head>

<body>
    <div class="container">
    <h1>medicaps university ,indore</h1>
        <p>the page to get information from the students by filling from and get record in the database<br><span class="span"><b>enter your data properly</b></span></p>
        <form action="index.php" method="post">
            <table>
            <tr>
                <td>NAME:</td>
                <td><input type="text" name="first-name" id="first-name" class="input" placeholder="first name" required></td>
                <td><input type="text" name="last-name" id="last-name"class="input" placeholder="last name" required></td>
            </tr>
             
            <tr>
                <td>EMAIL ID:</td>
                <td><input type="email" name="email" id="email" class="input" placeholder="ex: abc@gmail.com" required></td>
            </tr>
                
                <tr>
                <td>PHONE NO.:</td>
                <td><input type="text" name="phone" class="input" id="phone" placeholder="0000000000" required></td>
            </tr>

                
                <tr>
                <td>YEAR:</td>
                <td><input type="text" name="sem" class="input" id="sem" placeholder="First,Second,Third,Fourth" required></td>
            </tr>
                   
                <tr>
                <td>BIRTH DATE:</td>
                <td><input type="date" name="year" class="input" id="date" placeholder="First,Second,Third,Fourth" required></td>
            </tr>
                <tr>
                <td> <input type="submit" name="submit">  </td>
                
                </tr>
            </table>
        
        
        </form>
    </div>
    
</body>
</html>
