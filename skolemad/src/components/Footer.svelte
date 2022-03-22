<script></script>

<footer>
  <article>
    <p class="p-lead">Kontakt</p>
    <ul>
      <li>SkoleMad ApS</li>
      <li>Klaringen 15</li>
      <li>4174 Jystrup</li>
      <li>Tlf: 70222910</li>
      <li>Mail: post@skolemad.dk</li>
    </ul>
  </article>
  <article class="center">
    <p class="p-lead">Skolemad</p>
    <ul>
      <li><a href="#">Konto</a></li>
      <li><a href="#">Bestil mad</a></li>
      <li><a href="#">Afbestil mad</a></li>
      <li><a href="#">Om</a></li>
      <li><a href="#">Kontakt</a></li>
      <li><a href="#">Indsæt penge</a></li>
    </ul>
  </article>
  <article class="right">
    <p class="p-lead">Bruger</p>
    <ul>
      <li><a href="#">Log ind</a></li>
      <li><a href="#">Opret bruger</a></li>
      <li><a href="#">Glemt kodeord</a></li>
      <li><a href="#">Skift kodeord</a></li>
    </ul>
  </article>
</footer>

<style>
  footer {
    display: flex;
    justify-content: space-around;
    background-color: var(--primary-nav);
    color: var(--background);
    margin-top: var(--spacing-4);
    padding: var(--spacing-4);
    flex-flow: wrap;
  }
  .center {
    text-align: center;
  }

  .right {
    text-align: right;
  }

  a {
    text-decoration: none;
    color: inherit;
    transition: 250ms ease;
  }

  a:hover {
    color: var(--font);
  }

  ul {
    list-style: none;
  }
</style>
