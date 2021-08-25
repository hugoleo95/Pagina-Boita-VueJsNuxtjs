<template>
<div>
  <div>
  <Header/>
  </div>
  <div>
  <Cuerpo/>
  </div>
  <div>
  <Footer/>
  </div>

</div>
</template>

<script>
import Header from '../components/Header'
import Cuerpo from '../components/Cuerpo'
import Footer from '../components/Footer'

export default {
  components: {//aqui indicamos el post de componentes
			Header,
      Cuerpo,
      Footer
      
		},
	
}
</script>
