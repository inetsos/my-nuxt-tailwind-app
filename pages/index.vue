<template>
  <div class="min-h-screen bg-gray-100 p-8 space-y-4">
    <!-- 버튼 -->
    <BaseButton>커피 주문하기</BaseButton>

    <!-- 카드 -->
    <Card
      image="https://images.ctfassets.net/v601h1fyjgba/1vlXSpBbgUo9yLzh71tnOT/a1afdbe54a383d064576b5e628035f04/Iced_Americano.jpg"
      title="아이스 아메리카노"
    >
      <template #description>
        시원하고 쌉싸름한 커피 한 잔 어때요?
      </template>
      <template #action>
        <BaseButton>자세히 보기</BaseButton>
      </template>
    </Card>

    <!-- 알림 -->
    <Alert>오후 5시 이후 주문은 다음날 수령됩니다 ☕</Alert>

    <!-- 입력 필드 -->
    <InputField
      id="email"
      label="이메일 주소"
      placeholder="you@example.com"
      type="email"
      v-model="email"
    />

    <!-- 모달 -->
    <BaseButton @click="modalOpen = true">모달 열기</BaseButton>
    <Modal
      :show="modalOpen"
      title="확인 요청"
      @confirm="handleConfirm"
      @cancel="modalOpen = false"
    >
      정말로 주문을 완료하시겠습니까?
    </Modal>
  </div>
</template>

<script setup lang="ts">
import BaseButton from '~/components/BaseButton.vue'
import Card from '~/components/Card.vue'
import Alert from '~/components/Alert.vue'
import InputField from '~/components/InputField.vue'
import Modal from '~/components/Modal.vue'

const email = ref('')
const modalOpen = ref(false)

const handleConfirm = () => {
  modalOpen.value = false
  alert(`감사합니다! 이메일(${email.value})로 주문 내역을 보내드릴게요.`)
}
</script>