<template>
  <view class="container">
    <scroll-view :content-container-style="{contentContainer: {paddingVertical: 20}}">
    <!-- <flat-list
        :data="$data.myJson"
        :render-item="(item) => renderList(item)"
    /> -->
     <flat-list
      :data="$data.myJson" >
      <view render-prop-fn="renderItem" >
        <view :style="{backgroundColor: '#fff', marginBottom: 10, marginTop: 10,marginLeft: 10, marginRight: 10, borderRadius:15 , paddingLeft: 20,paddingTop:20, paddingBottom:20 , flex: 1}" >
          <text>{{args.item.fullName}}</text>
          <text>{{args.item.schedule.monday}}</text>
        </view>
      </view>
    </flat-list>
    </scroll-view>
  </view>
</template>

<script>
import React from 'react';
import {Text, View} from 'react-native';

import json from '../final.json'

export default {
        data(){
            return{
                myJson: json.residents
            }
        },

        methods: {

            renderList: function(item) {
                return (
                  <View class="item">
                    <Text>{item.item.fullName}</Text>
                  </View>
                
                )
            }
        }
    }

</script>


<style>
.container {
  flex: 1;
  background-color: #f5f5f5;
}
.item{
  background-color: #fff;
  margin-top: 20px;
  color: #fff;
}
</style>
