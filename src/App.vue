<template>
  <v-app>
    <v-main>
      <v-container>
        <v-badge offset-x="20" offset-y="20" overlap color="rgba(0,0,0,0)">
          <!-- 削除クリックイベントを発生させるためのボタン -->
          <v-btn
            slot="badge"
            color="grey white--text"
            class="delete-button"
            fab
            height="20"
            width="20"
            @click="onClickDelete"
          >
            <!-- ×アイコン -->
            <v-icon small>fas fa-times</v-icon>
          </v-btn>
          <!-- 画像描画領域 -->
          <v-avatar size="80" class="mb-3 avatar" @click="onClickImage">
            <!-- プロフィール画像 -->
            <img
              ref="fileInput"
              src="@/assets/logo.png"
              alt="avatarImage"
              class="avatar-image"
            />
          </v-avatar>
        </v-badge>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
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

<style scoped>
.avatar {
  cursor: pointer;
  background-color: #eee;
}
.avatar-image {
  object-fit: cover;
}
</style>
