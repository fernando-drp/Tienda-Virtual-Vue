<script setup>
import { collection, addDoc } from 'firebase/firestore'
import { useFirestore } from 'vuefire'
import { products } from '../../data/products'

const db = useFirestore()

async function seedDB() {
  try {
    const productsCollection = collection(db, 'products')

    for (let i = 0; i < products.length; i++) {
      await addDoc(productsCollection, {
        name: products[i].name,
        price: products[i].price,
        availability: products[i].availability,
        category: products[i].category,
        image: `/images/products/producto${i + 1}.jpg`,
      })

      // console.log(`Producto ${i + 1} agregado`)
    }

    alert('Se agregaron todos los productos correctamente')
  } catch (error) {
    console.error('Error al agregar productos:', error)
    alert('Ocurrió un error al agregar los productos. Revisa la consola.')
  }
}
</script>

<template>
  <div class="mt-10">
    <Link to="products">Volver</Link>

    <h1 class="text-4xl my-10 font-extrabold">Seeder</h1>

    <div class="flex justify-center bg-white shadow">
      <div class="mx-auto mt-10 p-10 w-full 2xl:w-2/4">
        <div class="mt-16">
          <FormKit
            type="form"
            submit-label="Agregar Productos"
            incomplete-message="No se pudo enviar, revisa los mensajes"
            @submit="seedDB"
          />
        </div>
      </div>
    </div>
  </div>
</template>
