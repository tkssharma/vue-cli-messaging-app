<template lang="html">
  <li :class="cssClass">
    <span v-html="message.text" />
  </li>
</template>


<script>
export default {
  name: 'Message',

  props: {
    message: Object
  },
  data :function() {
    return{};

  },
  computed: {
    cssClass() {
      return `messagist__list-item-${this.message.author}`
    }
  }
}
</script>

<style>
.messagist__list-item {
	list-style: none;
	margin-bottom: 5px;
}

.messagist__list-item span {
	padding: 10px;
	display: inline-block;
	background: #f0f8ff;
	position: relative;
	border-radius: 0.5rem;
	max-width: 80%;
}

.messagist__list-item-system {
	text-align: left;
}

.messagist__list-item-system span::before {
	content: '';
	display: block;
	position: absolute;
	border: 8px solid transparent;
	border-right-color: #f0f8ff;
	left: -16px;
	bottom: 8px;
}

.messagist__list-item-user {
	text-align: right;
}

.messagist__list-item-user span {
	background: #b3e6a6;
}

.messagist__list-item-user span::after {
	content: '';
	display: block;
	position: absolute;
	border: 8px solid transparent;
	border-left-color: #b3e6a6;
	right: -16px;
	bottom: 8px;
}

.messagist__list-item-system + .messagist__list-item-user,
.messagist__list-item-user + .messagist__list-item-system {
	margin-top: 10px;
}
</style>

