<template>
  
    <div class="page-border">
      <div class="bg--white">

        <!-- header -->
        <header class="mt-1">
          <div class="container text-center">
            <h1 style="font-weight: 700;">COVID-19 App</h1>
            <h2 class="mt-2">Covid-19 live data all around the world.</h2>
          </div>
        </header>
        <!-- End: header -->

        <!-- Main -->
        <main class="mb-1 pt-4 pb-4" style="margin-top: 10px;">
          <div class="container text-center">
            <!-- <div class="flag flag-icon-background flag-icon-un flag-covid" title="un" id="un"></div> -->
            <h3 style="font-weight: 700;">Global Situation <img src="@/assets/flags/4x3/un.svg" style="border-radius: 10px;" alt="UN" id="United Nation Flag" width="70px"></h3>

            <div class="row text-center mt-4">
              <div class="col-sm-4">
                <div class="covid-card">
                  <div class="row">
                    <div class="col-sm-8">
                      Confirmed Cases
                    </div>
                    <div class="col-sm-4">
                      <!-- <span class="badge bg-warning text-dark">+ 52.232</span> -->
                    </div>
                    <div class="col-sm-12 mt-3">
                      <h3 style="font-weight: 800;">{{ covid.confirmed.value }}</h3>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-sm-4">
                <div class="covid-card">
                  <div class="row">
                    <div class="col-sm-8">
                      Recovery Cases
                    </div>
                    <div class="col-sm-4">
                      <!-- <span class="badge bg-success text-dark">+ 112.132</span> -->
                    </div>
                    <div class="col-sm-12 mt-3">
                      <h3 style="font-weight: 800;">{{ covid.recovered.value }}</h3>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-sm-4">
                <div class="covid-card">
                  <div class="row">
                    <div class="col-sm-8">
                      Death Cases
                    </div>
                    <div class="col-sm-4">
                      <!-- <span class="badge bg-danger text-dark">+ 12.323</span> -->
                    </div>
                    <div class="col-sm-12 mt-3">
                      <h3 style="font-weight: 800;">{{ covid.deaths.value }}</h3>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </main>
        
        <main class="">
          <div class="container text-center">
            <h3 style="font-weight: 700;">Indonesia Situation <img src="@/assets/flags/4x3/id.svg" style="border-radius: 10px; background-color: gray; padding: 0.1px; text-align: center;" alt="UN" id="United Nation Flag" width="70px"></h3>
            <!-- <div class="select mt-3">
              <select style="width: 70%;" id="">
                  <option selected>Select Country Case</option>
                  <option data-img_src="id.svg">Indonesia</option>
                  <option>Afghanistan</option>
                  <option>Albania</option>
                  <option>Algeria</option>
                  <option>Andorra</option>
                  <option>Angola</option>
                  <option>Afghanistan</option>
              </select>
            </div> -->
            <div class="row text-center mt-4">
              <div class="col-sm-4">
                <div class="covid-card">
                  <div class="row">
                    <div class="col-sm-8">
                      Confirmed Cases
                    </div>
                    <div class="col-sm-4">
                      <span class="badge bg-warning text-dark">+ {{ indonesiaToday.Confirmed - indonesiaYesterday.Confirmed}}</span>
                      <!-- <span class="badge bg-warning text-dark">+ 8.221</span> -->
                    </div>
                    <div class="col-sm-12 mt-3">
                      <h3 style="font-weight: 800;">{{ indonesiaData.confirmed.value }}</h3>
                      <h6 style="font-weight: 800; color: #d8d9d8;">test</h6>
                      <!-- <h3 style="font-weight: 800;">13113</h3> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-sm-4">
                <div class="covid-card">
                  <div class="row">
                    <div class="col-sm-8">
                      Recovery Cases
                    </div>
                    <div class="col-sm-4">
                      <span class="badge bg-success text-dark">+ {{ indonesiaToday.Recovered - indonesiaYesterday.Recovered}}</span>
                      <!-- <span class="badge bg-success text-dark">+ 12.389</span> -->
                    </div>
                    <div class="col-sm-12 mt-3">
                      <h3 style="font-weight: 800;">{{ indonesiaData.recovered.value }}</h3>
                      <h6 class="text-success" style="font-weight: 800;">({{ Number(indonesiaData.recovered.value / indonesiaData.confirmed.value * 100).toFixed(2) }} %)</h6>
                      <!-- <h3 style="font-weight: 800;">12313</h3> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-sm-4">
                <div class="covid-card">
                  <div class="row">
                    <div class="col-sm-8">
                      Death Cases
                    </div>
                    <div class="col-sm-4">
                      <span class="badge bg-danger text-dark">+ {{ indonesiaToday.Deaths - indonesiaYesterday.Deaths}}</span>
                      <!-- <span class="badge bg-danger text-dark">+ 2.987</span> -->
                    </div>
                    <div class="col-sm-12 mt-3">
                      <h3 style="font-weight: 800;">{{ indonesiaData.deaths.value }}</h3>
                      <h6 class="text-danger" style="font-weight: 800;">({{ Number(indonesiaData.deaths.value / indonesiaData.confirmed.value * 100).toFixed(2) }} %)</h6>
                      <!-- <h3 style="font-weight: 800;">123</h3> -->
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <h5 class="mt-4">Last Update : {{ lastUpdate }}</h5>
            <!-- <h5 class="mt-4">Last Update : {{ covid.lastUpdate }}</h5> -->
          </div>
        </main>
        <h5 style="text-align: center;">API From <a href="https://github.com/mathdroid/covid-19-api">https://github.com/mathdroid/covid-19-api</a></h5>
        <!-- End: Main -->

        </div>
        <h6 style="text-align: center; margin-top: -20px">Covid-19 App version 1.0 | Github Repository from <a href="https://github.com/dandypramudyaa/covid19-nuxt">Dandy Pramudya</a> | Design from Dinda Alfhia</h6>
    </div>

</template>

<script  lang="ts">
import axios from 'axios'
import moment from 'moment'

export default {
    async asyncData() {
        const today = moment().format('YYYY-MM-DD');
        const yesterday = moment().subtract(1, 'days').format('YYYY-MM-DD');
        // const api = "https://api.covid19api.com/country/indonesia?from=" + yesterday + "&to=" + today
        const api = "https://api.covid19api.com/country/indonesia?from=2021-03-09&to=2021-03-10"
        const covid = await axios.get(
            `https://covid19.mathdro.id/api`
        );
        const indonesia = await axios.get(
            // `https://covid19.mathdro.id/api/countries/Indonesia`
            api
        );
        const indonesiaData = await axios.get(
            `https://covid19.mathdro.id/api/countries/Indonesia`
        );
        console.log(api);
        console.log(indonesia.data[1]);
        const getLastUpdate = covid.data.lastUpdate;
        const lastUpdate = moment(getLastUpdate).format('DD-MM-YYYY hh:mm');
        return { covid: covid.data, indonesiaYesterday: indonesia.data[0], indonesiaToday: indonesia.data[1], indonesiaData: indonesiaData.data, lastUpdate };
        // const { data } = await axios.get('https://covid19.mathdro.id/api')  
        // return {covid: data}
    },
}
</script>