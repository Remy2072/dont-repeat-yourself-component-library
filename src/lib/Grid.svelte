<script>
  import { Card } from "$lib";
</script>

<section>
  <picture>
    <img src="/img/wlw.png" alt="">
  </picture>
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
      grid-template-rows: repeat(2, calc(185px + .75rem)) repeat(2, 1fr);
		}
  }

  section picture {
    width: 100%;
    height: auto;
    overflow: hidden;
    display: flex;
    align-items: center;

    @media (min-width: 1024px) {
      grid-row: 1 / 3;
      grid-column: 1 / 3;
		}
  }

  section picture img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 25px;
    border: 2px solid #e9e0e965;
  }
</style>
