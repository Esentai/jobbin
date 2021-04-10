<template>
  <view class="container">
      <scroll-view :content-container-style="{contentContainer: {paddingVertical: 20}}">
        <view class="person">
          <image
            :style="{width: 300, height: 300, marginLeft: 55, borderRadius: 160}"
            :source="{uri: 'https://pbs.twimg.com/media/Ef-CtmIXYAANPv-.jpg'}"
          /> 
          <Text :style="{textAlign: 'center', fontSize: 32, marginTop: 10}">Василий Пупкин</Text>
        </view>
        <Text class="info">Пол: муж.</Text>
        <Text class="info">Email: vasily@gmail.com</Text>
        <Text class="info">Номер телефона: 87475240682</Text>
        <Text class="info">День рождения: 01.01.1995</Text>
        <Text class="info">Опыт работы: 6 месяцев</Text>
        <view class="btn">
            <button title="Редактировать данные" color="#0d9edf"  :style="{borderRadius: 30, height: 45}" />
        </view>
        </scroll-view>
  </view>
</template>

<style>
.container {
  flex: 1;
  background-color: #f5f5f5;
}
.person{
  margin-top: 30;
  text-align: center;
  margin-bottom: 20;
}
.info{
  padding-left: 20px;
  margin-top: 20px;
  font-size: 18px;
}
.heading {
  font-size: 30px;
  font-weight: bold;
  color: darkolivegreen;
  margin: 20px;
}
.btn{
  margin-top: 60px;
  margin-left: 40px;
  margin-right: 40px;
  border-radius: 15px;
}
</style>
