<template>
  <div>
      <template v-for="(animal, index) in animals" :key="index">
          <h2 v-if="animal === 'monkey'">
          {{index}}: {{animal}}
          </h2>

      </template>
        <u1>
            <li v-for="(user, index) in users" :key="index">
                이름: {{user.name}}, mbti: {{user.mbti}}, 직업: {{user.job}}
                <p v-for="item in user.skill" :key="item">{{item}}</p>


            </li>

        </u1>
    <!-- <h2>당신의 나이는 {{age}}살입니다 </h2>
    <h3 v-if="age > 18">당신은 늙었습니다</h3>
    <h3 v-else-if="age > 13 && age <=18">당신은 청소년입니다</h3>
    <h3 v-else>당신은 아기입니다</h3> -->
    <h2 v-if="display">(if)보입니다</h2>
    <!-- show는 안 보여도 개발자 도구에서 확인 가능 -->
    <h2 v-show="display">(show)보입니다</h2>
  </div>
</template>

<script>
export default {
    name: "App",
    data() {
        return {
            age: 14,
            display: true,
            animals: ["cat", "dog", "rat", "rabbit"],
            users: [
                {name: '김소현', mbti: 'intp', job: '백수', skill: ["영화 보기", "책 읽기", "산책하기"]},
                {name: '안유진', mbti: 'istp', job: '아이돌', skill: ["영화 보기", "책 읽기", "산책하기"]},
                {name: '김민주', mbti: 'infj', job: '배우', skill: ["영화 보기", "책 읽기", "산책하기"]},
            ]
        };
    }

}
</script>

<style>

</style>