<template>
  <div class="q-pa-md" style="max-width: 400px">

    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
<<<<<<< HEAD
=======
    <q-input
        filled
        v-model="langluage"
        label="ภาษา *"
        hint="ภาษา"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'กรุณาใส่ภาษา']"
      />
>>>>>>> thai-lang
    <!-- ID -->
    <q-input
        filled
        v-model="id"
        label="Your id *"
        hint="id"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type your id code']"
        />
    <!-- name -->
      <q-input
        filled
        v-model="name"
        label="Your name *"
        hint="name"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type your name']"
      />
    <!-- surname -->
      <q-input
        filled
        v-model="surname"
        label="Your surname *"
        hint="surname"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type your surname']"
      />
    <!-- age -->
      <q-input
        filled
        type="number"
        v-model="age"
        label="Your age *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Please type your age',
          val => val > 0 && val < 100 || 'Please type a real age'
        ]"
      />

      <q-toggle v-model="accept" label="I accept the license and terms" />

      <div>
        <q-btn label="Submit" type="submit" color="primary"/>
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>

  </div>
</template>

<script>
import { useQuasar } from 'quasar'
import { ref } from 'vue'

export default {
  setup () {
    const $q = useQuasar()
<<<<<<< HEAD
    const id = ref("****************")
    const name = ref("ศิศิกร")
    const surname = ref("แถบทอง")
=======
    const id = ref ("6604101383")
    const name = ref("Sisikorn")
    const surname = ref("Thaepthong")
>>>>>>> thai-lang
    const age = ref(null)
    const accept = ref(false)

    return {
      name,
      id,
      surname,
      age,
      accept,

      onSubmit () {
        if (accept.value !== true) {
          $q.notify({
            color: 'red-5',
            textColor: 'white',
            icon: 'warning',
            message: 'You need to accept the license and terms first'
          })
        }
        else {
          $q.notify({
            color: 'green-4',
            textColor: 'white',
            icon: 'cloud_done',
            message: 'Submitted'
          })
        }
      },

      onReset () {
        name.value = null
<<<<<<< HEAD
        id.value = null
        surname.value = null
=======
        surnamename.value = null
        id.value = null
>>>>>>> thai-lang
        age.value = null
        accept.value = false
      }
    }
  }
}
</script>
