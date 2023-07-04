# Descrizione:

Creare un nuovo progetto utilizzando Vite e Vue 3, definire i componenti necessari per strutturare un layout a tema Pokémon.
Al caricamento della pagina, effettuare una chiamata all'API di Pokémon
Cercare di utilizzare lo store management per prenderci confidenza

> Qui la documentazione:
> https://documenter.getpostman.com/view/1276443/2s8ZDbVLPF

## NOTE

Usare Postman per studiare la risposta. Con i dati restituiti:

- stampare una card per ogni Pokémon.
- Creare un componente loader da visualizzare fino a quando i risultati non siano pronti.

Aggiungere un filtro di ricerca. Il filtro deve essere fatto con una tendina e deve permettere all'utente di filtrare i pokemon per tipo.

<select>
    <option>
        tipo 1..
    </option>
</select>

Per conoscere quali tipi sono disponibili, effettuate una chiamata via Postman all'indirizzo https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons/types1 .
Copiate manualmente l'array che vi arriverà come risposta da Postman e usatelo per produrre dinamicamente le <options> opzioni.

Quando l'utente cambia il valore della tendina, potete usare il valore scelto per fare partire la chiamata API e mostrare i risultati in pagina!

> Documentazione: https://documenter.getpostman.com/view/1276443/2s8ZDbVLPF#31f11fae-574f-4ac4-8882-c235058f517e

Dare all'utente la possibilità di annullare il filtro e tornare alla chiamata "normale".

### Punti extra

Provare ad inserire i tipi chiamandoli direttamente dalle API e passandoli al componente della tendina.

Provare a inserire una paginazione (bisogna studiare bene i dati forniti dalla risposta delle API)

Provare ad aggiungere anche un filtro di tipo text per cercare tramite il nome dei pokemon!
