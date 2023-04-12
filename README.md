# sweetaler2_for_nuxtJs
To import SweetAlert2 icons in a Nuxt project, you can follow these steps:

#step1:  Install SweetAlert2 package and its dependencies using npm:

code:  npm install sweetalert2 @sweetalert2/theme-bootstrap-4

#step2:Create a plugin file for SweetAlert2 by creating a new file in the plugins directory of your Nuxt project (e.g. sweetalert2.js).
#step3: Inside the plugin file, import SweetAlert2 and its Bootstrap 4 theme:
code : import Swal from 'sweetalert2/dist/sweetalert2.js'
import 'sweetalert2/dist/sweetalert2.css'
import '@sweetalert2/theme-bootstrap-4/bootstrap-4.css'

#step4:Add the plugin to your Nuxt config file (nuxt.config.js) by adding the following code:
code: plugins: [
  { src: '~/plugins/sweetalert2.js', mode: 'client' }
]


Note the mode: 'client' option which ensures the plugin is only loaded on the client-side.

#step5: Use SweetAlert2 in your components by importing it and calling its methods:

import Swal from 'sweetalert2'

Swal.fire({
  title: 'Hello world!',
  icon: 'success'
})


You can also customize the icon by using the iconHtml option and providing a HTML element that includes the icon class:
Swal.fire({
  title: 'Hello world!',
  iconHtml: '<i class="fas fa-check-circle"></i>'
})

<a href="https://sweetalert2.github.io/">go sweetalert2 website</a>
