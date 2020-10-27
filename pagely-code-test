<?php

$data = $_COOKIE['saved_data'];

$i = unserialize($data);

$dbh = new mysqli('localhost', 'user', 'password', 'db');

$query = "SELECT id, firstname, lastname FROM Guests where id = '".$i['id']."'";

$qh = $dbh->query($query);

$row = mysqli_fetch_assoc($qh);

if ((count($row) == 0) {

printf("I'm sorry your account has been removed <em>%s</em> does not match any of our records \n", $i['id']);

} else {

printf("Welcome to the website %s\n", $row['name']);

}

?>
