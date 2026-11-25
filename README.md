# Comande Pino d'Oro — app

App Android del Ristorante Pino d'Oro per le comande in cucina e al bar. I camerieri scrivono la comanda sul tablet; ogni postazione (antipasti, primi, secondi, bar e dolci) vede sul proprio schermo cosa preparare e quando iniziare, così i piatti della stessa uscita di un tavolo escono insieme.

È un'app per uso interno, sviluppata dal ristorante per il proprio personale. Non è in vendita.

Qui ci sono solo i file di installazione (APK): l'app controlla da sola questa pagina e propone l'aggiornamento quando esce una versione nuova.

L'ultima versione è sempre in [Releases](../../releases/latest).

Per collegare un dispositivo serve il codice mostrato sul dispositivo principale del ristorante: senza quello l'app non si collega a nulla.

## Chi la sviluppa

**Lido Pino d'Oro SAS di Sorvillo Antonio**

- Sede: Via Tommaso Maria Fusco, 29 – 81034 Mondragone (CE)
- P.IVA: IT03012490615
- Sito: <https://ristorantepinodoro.it>
- PEC: lidopinodorosas@pec.it

## Dati e sicurezza

- **Dove stanno le comande.** Su un solo dispositivo del ristorante, il «principale». Gli altri dispositivi le leggono attraverso il Wi-Fi del locale. Non ci sono server esterni, cloud o account.
- **Quali dati.** Numero del tavolo, coperti, piatti, note per la cucina (per esempio «senza aglio») e orari. L'app non chiede nomi né altri dati personali dei clienti. Le comande chiuse si cancellano da sole dopo 24 ore.
- **Collegamento tra i dispositivi.** È cifrato (HTTPS con il certificato del dispositivo principale). Un dispositivo nuovo si collega solo con il codice mostrato sul principale, e solo mentre il principale ha le impostazioni aperte.
- **Internet.** Serve solo per cercare e scaricare gli aggiornamenti da questa pagina. L'app non contiene pubblicità, statistiche o tracciamenti.
- **Chiavi e password.** Nell'APK e su GitHub non ce ne sono: le chiavi del collegamento vengono create sul dispositivo principale quando lo si imposta e passano solo ai dispositivi collegati con il codice.

### Permessi Android

| Permesso | A cosa serve |
|---|---|
| `INTERNET`, `ACCESS_NETWORK_STATE` | Collegamento tra i dispositivi sul Wi-Fi del locale e ricerca degli aggiornamenti |
| `REQUEST_INSTALL_PACKAGES` | Passare l'aggiornamento scaricato all'installatore di Android; l'utente conferma ogni installazione |
| `POST_NOTIFICATIONS` | Avvisare che è uscita una versione nuova |
| `RECEIVE_BOOT_COMPLETED` | Riprendere la ricerca periodica degli aggiornamenti dopo un riavvio del dispositivo |

## Collegamento con la cassa (in preparazione)

Oggi l'app non è collegata a nessun sistema esterno: le comande si scrivono a mano. Il ristorante usa la cassa Tilby e vuole collegarla all'app, per leggere le comande dei tavoli senza scriverle due volte. Il collegamento non è ancora attivo: l'accesso alle API va richiesto a Tilby e certificato da Tilby.

Come sarà fatto:

- solo con le API ufficiali di Tilby, con il token del nostro punto vendita e solo per i dati del nostro ristorante;
- l'app leggerà le vendite (le comande dei tavoli) e le sale;
- il token si inserirà a mano sul dispositivo principale e resterà lì, cifrato: non sarà mai dentro l'APK, su GitHub o sugli altri dispositivi.

Tilby è un marchio del suo titolare. Quest'app non è sviluppata, approvata o sponsorizzata da Tilby.

## Licenza

Software proprietario, tutti i diritti riservati: vedi [LICENSE](LICENSE).

L'app contiene librerie open source: l'elenco e le loro licenze sono in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
