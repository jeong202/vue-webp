<template>
    <section id="textType" class="text__wrap" :class="element">
        <span>{{ title }}</span>
        <h2 class="mb70">스크립트를 익히는 방법</h2>
        <div class="text__inner container">
            <div :class="'text t'+(key+1)" v-for="(text, key) in TextInfo" :key="key">
                <h3 class="text__title">{{ text.title }}</h3>
                <p class="text__desc">{{ text.desc }}</p>
                <a class="text__btn" href="/">더보기</a>
            </div>
        </div>
    </section>
</template>
<script>

export default {
    props: {
        element: String,
        title: String
    },
    data: function () {
        return {
            TextInfo: [
                {
                    title: "웹표준 사이트 만들기",
                    desc: "사이트를 만들기 위한 기초 강의입니다. 기본 코딩에 대한 감각을 익히고, 웹 표준을 준수하면서 코딩하는 방법을 익힙니다. 다양한 예제를 통해 사이트를 만드는"
                },
                {
                    title: "반응형 사이트 만들기",
                    desc: "웹표준 사이트를 완성하고, 반응형을 익히는 사이트입니다. 기본 코딩을 익히고, 반응형 감각을 키우면 모바일 및 반응형 사이트도 만들 수 있습니다. 웹표준 사이트를....."
                },
                {
                    title: "패랠렉스 사이트 만들기",
                    desc: "기업 사이트 중 50% 이상이 패랙렉스 스크로링 효과로 만들어져 있습니다. 웹 표준, 반응형 사이트를 완성하였다면, 이제는 인터랙티브한 패랠렉스 스크롤링 사이트를....."
                },
                {
                    title: "웹표준 사이트 만들기",
                    desc: "사이트를 만들기 위한 기초 강의입니다. 기본 코딩에 대한 감각을 익히고, 웹 표준을 준수하면서 코딩하는 방법을 익힙니다. 다양한 예제를 통해 사이트를 만드는"
                },
                {
                    title: "반응형 사이트 만들기",
                    desc: "웹표준 사이트를 완성하고, 반응형을 익히는 사이트입니다. 기본 코딩을 익히고, 반응형 감각을 키우면 모바일 및 반응형 사이트도 만들 수 있습니다. 웹표준 사이트를....."
                },
                {
                    title: "패랠렉스 사이트 만들기",
                    desc: "기업 사이트 중 50% 이상이 패랙렉스 스크로링 효과로 만들어져 있습니다. 웹 표준, 반응형 사이트를 완성하였다면, 이제는 인터랙티브한 패랠렉스 스크롤링 사이트를....."
                }
            ]
        }
    }
}
</script>

<style>
.imgText__inner {
    display: flex;
    justify-content: space-between;
}

.imgText__inner>div {
    width: 32%;
    height: 500px;
}

.imgText__txt .small {
    font-size: 16px;
    color: #666;
    text-decoration: underline;
    margin-bottom: 20px;
    display: block;
    text-align: left;
}

.imgText__txt .title {
    font-size: 50px;
    font-weight: 300;
    word-break: keep-all;
    line-height: 1.4;
    margin-bottom: 20px;
}

.imgText__txt .desc {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.5;
    color: #666;
    margin-bottom: 10px;
}

.imgText__txt .list {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.6;
}

.imgText__txt .list li {
    position: relative;
    padding-left: 20px;
}

.imgText__txt .list li::before {
    content: '';
    width: 5px;
    height: 5px;
    background: #666;
    border-radius: 50%;
    position: absolute;
    left: 5px;
    top: 9px;
}

.imgText__txt .list li a {
    color: #666;
}

.imgText__img {
    border-radius: 10px;
    position: relative;
}

.imgText__img a {
    background-color: #7C2B39;
    color: #fff;
    padding: 10px 30px;
    font-size: 18px;
    border-radius: 30px;
    display: inline-block;
    position: absolute;
    left: 30px;
    bottom: 30px;
}

.imgText__img a.blue {
    background-color: #2B387C;
}

.imgText__img.img1 {
    background: url(../img/imgText_bg01.jpg) no-repeat center / cover;
}

.imgText__img.img2 {
    background: url(../img/imgText_bg02.jpg) no-repeat center / cover;
}
</style>