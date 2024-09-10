<template>
  <div>
    <div>{{ greet }} {{ name }}</div>
    <div v-html="channel"></div>
    <h2 :id="headingId">heading</h2>
    <button :disabled="isDisabble">bind</button>
    <h2 class="underline">underline text</h2>
    <h2 class="underline" :class="status">status</h2>
    <h2 :class="isPromoted && 'promoted'">status</h2>
    <h2 :class="isSoldout ? 'soldout' : 'new'">soldout movie</h2>
    <h2 :class="['new', 'promoted']">newly promoted movie</h2>
    <h2 :class="[isPromoted && 'promoted', isSoldout ? 'soldout' : 'new']">
      array conditional movie
    </h2>
    <h2
      :class="{
        promoted: isPromoted,
        soldout: isSoldout,
        new: !isPromoted && !isSoldout,
      }"
    >
      object conditional movie
    </h2>
  </div>
</template>

<script>
export default {
  name: "VBind",
  data() {
    return {
      greet: "hallo",
      name: "aris kiflan",
      channel: "<b>ariskeren</b>",
      headingId: "heading",
      isDisabble: true,
      status: "success",
      isPromoted: true,
      isSoldout: true,
    };
  },
};
</script>

<style>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.soldout {
  color: red;
}

.new {
  color: green;
}
</style>
