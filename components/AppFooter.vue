<script setup lang="ts">

const columns = [
  {
    label: 'Ressources',
    children: [
      { label: 'Starter Kits' },
      { label: 'Release Notes' },
      { label: 'Blog', },
      { label: 'Partners', },
      { label: 'News', },
      { label: 'Jobs', },
      { label: 'Careers', },
    ],
  },
  {
    label: 'Products',
    children: [
      { label: 'Cloud' },
      { label: 'Forge' },
      { label: 'Nightwatch' },
      { label: 'Nova' },
    ]
  },
  {
    label: 'Packages',
    children: [
      { label: 'Cashier' },
      { label: 'Dusk' },
      { label: 'Horizon' },
      { label: 'Octane' },
      { label: 'Scout' },
      { label: 'Pennant' },
      { label: 'Pint' },
    ],
  }
];
</script>
<template>
  <UFooter>
    <template #top>
      <UContainer>
          <UFooterColumns :colums="columns">
          <template #right>
            <form>
              <UFormField name="email" label="S'inscrire à notre newsletter" size="lg">
                <UInput type="email" placeholder="Votre adresse email" required>
                  <template #trauling>
                    <UButton type="submit" color="orange" size="xs" icon="mail" label="S'inscrire"/>
                  </template>
                </UInput>
              </UFormField>
            </form>
          </template>
        </UFooterColumns>
      </UContainer>
    </template>

    <template #left>
      <p class="text-sm">
        Copyright &copy; 2021 Connectly; {{ new Date().getFullYear()}}. Tous droits réservés
      </p>
    </template>

    <template #right>
      <UFooterSocialLinks />
    </template>

    <template #center>
      <Ubutton to="https://github.com/Wifak10?tab=repositories  " target="_blank" icon="devicon:githubcodespaces" ></Ubutton>
    </template>
  </UFooter>
</template>
<style scoped></style>
