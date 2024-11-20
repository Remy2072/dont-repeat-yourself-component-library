<script>
    import { Footer, Navigation, Heading } from "$lib";
</script>
  
  <Navigation />
  
  <div class="container">
    <Heading />
  
  </div>
  
  <Footer />
  
  <style>
    .container {
      width: 100%;
      background: var(--container-gradient);
      border-radius: 24px;
      padding: 0 2.188rem 0 2.188rem;
      height: 100vh;
    }
  
    @media screen and (min-width: 768px) {
        .container {
            border-radius: 30px;
            padding: 0 3.125rem 0 3.125rem;
        }
    }
  
    @media screen and (min-width: 1024px) {
        .container {
            border-radius: 2.5rem 0 2.5rem 2.5rem;
            padding: 0 6.25rem 0 6.25rem;
        }
    }
  
    @media screen and (min-width: 1440px) {
      .container {
        padding: 0 9.375rem 0 9.375rem;
      }
    }
  </style>
  