<script>
  import Homeinfo from "./Homeinfo.svelte";
  /*  import "carbon-components-svelte/css/all.css";
  import { Accordion, AccordionItem } from "carbon-components-svelte"; */
</script>

<div>
  <Homeinfo />
  <article>
    <!--  <h2>Fordele for:</h2>
    <Accordion>
      <AccordionItem title="Kunden">
        <p>
          Natural Language Classifier uses advanced natural language processing
          and machine learning techniques to create custom classification
          models. Users train their data and the service predicts the
          appropriate category for the inputted text.
        </p>
      </AccordionItem>
      <AccordionItem title="Leverandøren">
        <p>
          Analyze text to extract meta-data from content such as concepts,
          entities, emotion, relations, sentiment and more.
        </p>
      </AccordionItem>
      <AccordionItem title="Modtageren">
        <p>
          Translate text, documents, and websites from one language to another.
          Create industry or region-specific translations via the service's
          customization capability.
        </p>
      </AccordionItem>
    </Accordion> -->
  </article>
</div>

<style>
  @media screen and (min-width: 800px) {
    div {
      display: flex;
    }
  }
</style>
