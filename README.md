# SL
url reprizitorija - https://github.com/lezajas/SL.git

SQL KOMANDE:

SELECT 
    zaposlenik.ime_prezime, 
    evidencija.zaposlenik, 
    SUM(evidencija.broj_sati) AS zbroj
FROM 
    evidencija
JOIN 
    zaposlenik ON evidencija.zaposlenik = zaposlenik.id
WHERE 
    evidencija.zaposlenik = 2
GROUP BY 
    zaposlenik.ime_prezime, evidencija.zaposlenik;