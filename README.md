# vtiger-fattura-elettronica
Modulo VTiger per la fatturazione elettronica italiana

Con questo modulo le società che creano le fatture con VTiger potranno continuare a farlo anche dopo il 2019. Da questa data sarà obbligatorio usare in Italia la fattura elettronica.
Questo modulo si appoggia al servizio fornito da Fattura24 (https://www.fattura24.com/) per firmare elettronicamente e conservare le fatture, secondo i termini di legge.
La fattura viene automaticamente aggiunta come documento correlato in pdf al record in VTiger, dopo essere stata firmata e memorizzata sul cloud di Fattura24.
L'operazione si innesca cliccando su un pulsante che il modulo aggiunge della finestra di dettaglio della fattura ed avviene tutto in modo automatico.
Per poter procedere bisogna avere un account su Fattura24 e inserire nella configurazione del modulo la "apiKey".

Il modulo è stato sviluppato su VTiger 7.

Dopo aver effettuato l'installazione bisogna inserire i parametri di configurazione. Nel file modules/Fattura24/resources/config.inc.php:

$config = Array();
$config['apiKey'] = "";
$config['iban'] = "IBAN: IT....";
$config['metodopagamento'] = "Banca Popolare.....";
$config['mapping']['org']['partitaiva'] = "Partita I.V.A.";
$config['mapping']['org']['codicefiscale'] = "Codice Fiscale";
$config['mapping']['org']['provinciaconsegna'] = "Provincia consegna";
$config['mapping']['org']['provinciafatturazione'] = "Provincia fatturazione";

Qui bisogna modificare:
1) apiKey;
2) iban;
3) metodopagamento.

Gli altri possono essere personalizzati in caso di crm con personalizzazioni.

Per qualunque informazione o supporto potete contattarmi alla mia email: tommaso@bilotta.biz.

