<template>
  <div class="min-h-screen p-4">
    <RegionSelect label="Region" v-model="regionId" />
    <SubregionSelect label="Sub-Region" v-model="subRegionId" :region="regionId" />
    <CountrySelect label="Country" v-model="countryId" :subregion="subRegionId" />
    <StateSelect label="State" v-model="stateId" :country="countryId" />
    <CitySelect label="City" v-model="cityId" :state="stateId" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import {
  RegionSelect,
  SubregionSelect,
  CountrySelect,
  StateSelect,
  CitySelect
} from '@data-forge-services/core'

const regionId = ref('')
const subRegionId = ref('')
const countryId = ref('')
const stateId = ref('')
const cityId = ref('')
</script>