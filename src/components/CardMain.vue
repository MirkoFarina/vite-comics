<script>
export default {
    name:'CardMain',
    props: {
        cardThumb: String,
        cardSeries: String,
        cardPrice: String
    }
};
</script>

<template>
    <div class="card">
        <div class="top">
            <img :src="cardThumb" :alt="cardSeries" />
            <div class="content">
                <h5>PREZZO: {{ cardPrice }}</h5>
            </div>
        </div>
        <div class="bottom">
            <h3>
                {{ cardSeries }}
            </h3>
        </div>
    </div>
</template>



<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
.card {
    width: calc(100% / 6 - 10px);
    padding: 30px 10px;
    cursor: pointer;
    &:hover .top{
        img {
            transform: scale(1.2);
        }
        .content {
            display: block;
        }
    }
}

  .top {
    height: 170px;
    overflow: hidden;
    position: relative;
    img {
        width: 100%;
    }
}

.content {
    background-color: $primary-color;
    position: absolute;
    display: none;
    bottom: 0;
    left: 0;
    padding: 10px 20px;
}
.bottom {
    margin-top: 10px;
    h3  {
        font-size: .9rem;
        font-weight: 400;
    }
}
</style>