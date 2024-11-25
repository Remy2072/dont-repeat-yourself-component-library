<script>
  import { Card } from "$lib";
</script>

<section>
  <img src="/img/wlw.png" alt="">
  <Card></Card>
  <Card></Card>
  <Card></Card>
  <Card></Card>
  <Card></Card>
  <Card></Card>
  <Card></Card>
  <Card></Card>
</section>

<style>
  section {
    display: grid;
    width: 100%;
    grid-template-rows: auto;
    grid-template-columns: 1;
    gap: 1.5rem;

    @media (min-width: 1024px) {
      grid-template-columns: repeat(2, 1fr);
		}
    
    @media (min-width: 1440px) {
      grid-template-columns: repeat(3, 1fr);
		}
  }

  section img {
    width: 100%;
    border-radius: 25px;
    border: 2px solid #e9e0e965;

    @media (min-width: 1024px) {
      grid-row: 1 / 3;
      grid-column: 1 / 3;
		}
  }
</style>
