<script>
  import Homeinfo from "./Homeinfo.svelte";
  /*  import "carbon-components-svelte/css/all.css";
  import { Accordion, AccordionItem } from "carbon-components-svelte"; */
  import MyAccordion from "../components/MyAccordion.svelte";

  const data = {
    Kunden: [
      "få fuld adgang til netsystemet via Internet, app, mobiltelefon eller sms",
      "oprette en konto, logge ind og ud med selvvalgt kode",
      "indbetale penge på kontoen med de fleste betalingskort, Mobilepay, indbetalingskort, netbank, BetalingsService, eller kontant",
      "benytte automatisk optankning med betalingskort eller BetalingsService",
      "bestille eller afbestille mad frem til det af leverandøren valgte tidspunkt",
      "benytte automatisk bestilling, som sammen med automatisk optankning fuldautomatiserer maden",
      "benytte App, sms eller ID-kort med billede og/eller stregkode som betalingsmiddel i f.eks. skolebod og kantine",
      "knytte konti sammen, så det er let at købe til flere",
      "overføre penge mellem konti",
      "få et overblik over hvad der er bestilt og leveret",
      "få en e-mail og/eller sms med ved ændringer på kontoen, når der er bestilt eller ikke bestilt mad, når saldoen kommer under et selvvalgt beløb m.m.",
      "få udbetalt penge fra kontoen uden gebyr",
      "få hurtig hjælp døgnet rundt på telefon, mail, chat, Skype og sms",
    ],
    Leverandøren: [
      "få fuld adgang til netsystemet via Internet, app, mobiltelefon eller sms",
      "oprette en konto, logge ind og ud med selvvalgt kode",
      "indbetale penge på kontoen med de fleste betalingskort, Mobilepay, indbetalingskort, netbank, BetalingsService, eller kontant",
      "benytte automatisk optankning med betalingskort eller BetalingsService",
      "bestille eller afbestille mad frem til det af leverandøren valgte tidspunkt",
      "benytte automatisk bestilling, som sammen med automatisk optankning fuldautomatiserer maden",
      "benytte App, sms eller ID-kort med billede og/eller stregkode som betalingsmiddel i f.eks. skolebod og kantine",
      "knytte konti sammen, så det er let at købe til flere",
      "overføre penge mellem konti",
      "få et overblik over hvad der er bestilt og leveret",
      "få en e-mail og/eller sms med ved ændringer på kontoen, når der er bestilt eller ikke bestilt mad, når saldoen kommer under et selvvalgt beløb m.m.",
      "få udbetalt penge fra kontoen uden gebyr",
      "få hurtig hjælp døgnet rundt på telefon, mail, chat, Skype og sms",
    ],
    Modtageren: [
      "få fuld adgang til netsystemet via Internet, app, mobiltelefon eller sms",
      "oprette en konto, logge ind og ud med selvvalgt kode",
      "indbetale penge på kontoen med de fleste betalingskort, Mobilepay, indbetalingskort, netbank, BetalingsService, eller kontant",
      "benytte automatisk optankning med betalingskort eller BetalingsService",
      "bestille eller afbestille mad frem til det af leverandøren valgte tidspunkt",
      "benytte automatisk bestilling, som sammen med automatisk optankning fuldautomatiserer maden",
      "benytte App, sms eller ID-kort med billede og/eller stregkode som betalingsmiddel i f.eks. skolebod og kantine",
      "knytte konti sammen, så det er let at købe til flere",
      "overføre penge mellem konti",
      "få et overblik over hvad der er bestilt og leveret",
      "få en e-mail og/eller sms med ved ændringer på kontoen, når der er bestilt eller ikke bestilt mad, når saldoen kommer under et selvvalgt beløb m.m.",
      "få udbetalt penge fra kontoen uden gebyr",
      "få hurtig hjælp døgnet rundt på telefon, mail, chat, Skype og sms",
    ],
  };
</script>

<div>
  <Homeinfo />
  <article>
    <h2>Fordele for:</h2>
    {#each Object.entries(data) as entry}
      <MyAccordion {entry} />
    {/each}
  </article>
</div>

<style>
  /* @media screen and (min-width: 800px) {
    div {
      display: flex;
    }
  } */
</style>
