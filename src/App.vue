<template>
  <div class="container mt-3">
    <div class="card py-5">
      <div class="card-body text-center">
        <h1>@arutemyanの頸椎を締め上げる</h1>
        <p class="font-weight-bold">お前が締め上げなきゃ誰が締め上げる</p>

        <div class="text-center">
          <a :href="nowUrl" class="btn btn-primary">締め上げる</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import "@/assets/css/bootstrap.min.css";

import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {
  get nowUrl(): string {
    const baseUrl = "https://twitter.com/intent/tweet";
    const homePageUrl = "https://ant2357.github.io/arutemyan/";
    const text =  new Date().getDay() === 4
      ? "鍛え上げられたもくもくもくようびが@arutemyanの頸椎を締め上げる"
      : "%EF%BC%BC @arutemyanとじゃんけん2020 ／私は %23あるてみかんの頸椎を締め上げる %23あるてみかんと頸椎勝負！";

    const aa = "%0D%0A      ╭◜◝  ͡  ◜◝╮%0D%0A  💪 ( ¨̮  💪    )%0D%0A       人      Ｙ%0D%0A      (  ヽ  ﾉ%0D%0A      人   Ｙ%0D%0A     (  ヽ ﾉ%0D%0A     人  Ｙ%0D%0A    (  ヽﾉ%0D%0A    人  ＼%0D%0A   (＿)､＿)%0D%0A";

    return `${baseUrl}?url=${homePageUrl}&text=${text}${aa}`;
  }
}
</script>
