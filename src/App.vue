<template>
  <v-app>
    <v-main>
      <v-container>
        <v-badge offset-x="20" offset-y="20" overlap color="rgba(0,0,0,0)">
          <!-- クリックイベントを発生させるためのボタン -->
          <v-btn
            slot="badge"
            color="grey white--text"
            class="delete-button"
            fab
            @click="onClickDelete"
          >
            <!-- ×アイコン -->
            <v-icon small>fas fa-times</v-icon>
          </v-btn>
          <!-- 画像描画領域 -->
          <v-avatar size="80" class="mb-3 avatar">
            <!-- プロフィール画像 -->
            <img
              ref="fileInput"
              :src="imageUrl"
              alt="avatarImage"
              class="avatar-image"
              @click="onCickImage"
            />
          </v-avatar>
        </v-badge>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    //
  }),
  methods: {
    onClickImage: function () {
      alert("click image");
    },
    onClickDelete: function () {
      alert("click delete");
    },
  },
};
</script>

<style>
.avatar-image {
  object-fit: cover;
}
.delete-button {
  width: 20px;
  height: 20px;
}
</style>
