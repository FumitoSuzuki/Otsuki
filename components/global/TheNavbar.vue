<template>
  <b-navbar class="m-2" toggleable="lg">
    <b-navbar-brand href="/">
      <b-img src="~/static/image/nuxtjs-typo.svg" alt="Kitten" width="100" />
    </b-navbar-brand>
    <b-navbar-toggle target="nav-collapse" />
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item to="/">私たちの強み</b-nav-item>
        <b-nav-item to="/">サービス</b-nav-item>
        <b-nav-item to="/">実績</b-nav-item>
        <b-nav-item to="/">会社情報</b-nav-item>
        <b-nav-item to="/articles">ブログ</b-nav-item>
        <b-nav-item to="/">ニュース</b-nav-item>
        <b-nav-item to="/">お問い合わせ</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>
