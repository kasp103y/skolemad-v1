<script></script>

<div class=" flex">
  <h3>Aktuel uge</h3>
  <div class="arrows">
    <div class="right" />
    <p>Skift uge</p>
    <div class="left" />
  </div>

  <ul>
    <li>Mandag: Bananasplit med fyrværkeri og skinke.</li>
    <li>Vegetar: Bananasplit uden skinke</li>
  </ul>
  <ul>
    <li>Tirsdag: Bananasplit med fyrværkeri og skinke.</li>
    <li>Vegetar: Bananasplit uden skinke</li>
  </ul>
  <ul>
    <li>Onsdag: Bananasplit med fyrværkeri og skinke.</li>
    <li>Vegetar: Bananasplit uden skinke</li>
  </ul>
  <ul>
    <li>Torsdag: Bananasplit med fyrværkeri og skinke.</li>
    <li>Vegetar: Bananasplit uden skinke</li>
  </ul>
  <ul>
    <li>Fredag: Bananasplit med fyrværkeri og skinke.</li>
    <li>Vegetar: Bananasplit uden skinke</li>
  </ul>
</div>

<style>
  .flex {
    background-color: var(--accent);
    color: var(--background);

    display: flex;
    margin-top: var(--spacing-16);
    position: fixed;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    align-items: center;
    padding: var(--spacing-8) var(--spacing-2);
    z-index: -1;
  }
  .arrows {
    display: flex;
    justify-content: space-between;
    gap: var(--spacing-4);
    align-content: center;
    align-items: center;
  }
  .right,
  .left {
    width: 1rem;
    height: 1rem;
    border-left: var(--border-width-primary) solid var(--background);
    border-top: var(--border-width-primary) solid var(--background);
  }

  .right {
    transform: rotate(-45deg);
  }

  .left {
    transform: rotate(135deg);
  }
  ul {
    margin-top: var(--spacing-4);
    list-style: none;
  }
</style>
