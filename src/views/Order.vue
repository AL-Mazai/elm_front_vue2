<template>
    <div class="wrapper">

        <!-- header部分 -->
        <header>
            <p>确认订单</p>
        </header>

        <!-- 订单信息部分 -->
        <div class="order-info">
            <h5>订单配送至：</h5>
            <div class="order-info-address">
                <p>云南大学楸苑三栋</p>
                <i class="fa fa-angle-right"></i>
            </div>
            <p>zzw 先生 15877712345</p>
        </div>

        <h3>万家饺子（软件园E18店）</h3>
        <!-- 订单明细部分 -->
        <div class="order-detailed">
            <li>
                <div class="order-detailed-left">
                    <img src="../assets/img/sp01.png">
                    <p>纯肉鲜肉（水饺） x 2</p>
                </div>
                <p>&#165;15</p>
            </li>
            <li>
                <div class="order-detailed-left">
                    <img src="../assets/img/sp02.png">
                    <p>玉米鲜肉（水饺） x 1</p>
                </div>
                <p>&#165;16</p>
            </li>
        </div>
        <div class="order-deliveryfee">
            <p>配送费</p>
            <p>&#165;3</p>
        </div>

        <!-- 合计部分 -->
        <div class="total">
            <div class="total-left">
                &#165;49
            </div>
            <div class="total-right" @click="$router.push('/payment')">
                去支付
            </div>
        </div>
    </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Order",
}
</script>

<style scoped>
/****************** 总容器 ******************/
.wrapper {
    width: 100%;
    height: 100%;
}

/****************** header部分 ******************/
.wrapper header {
    width: 100%;
    height: 12vw;
    background-color: #0097FF;
    color: #fff;
    font-size: 4.8vw;

    position: fixed;
    left: 0;
    top: 0;
    z-index: 1000;

    display: flex;
    justify-content: center;
    align-items: center;
}

/****************** 订单信息部分 ******************/
.wrapper .order-info {
    /*注意这里，不设置高，靠内容撑开。因为地址有可能折行*/
    width: 100%;
    margin-top: 12vw;
    background-color: #0097EF;
    box-sizing: border-box;
    padding: 2vw;
    color: #fff;
}

.wrapper .order-info h5 {
    font-size: 3vw;
    font-weight: 300;
}

.wrapper .order-info .order-info-address {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;

    font-weight: 700;
    user-select: none;
    cursor: pointer;
    margin: 1vw 0;
}

.wrapper .order-info .order-info-address p {
    width: 90%;
    font-size: 5vw;
}

.wrapper .order-info .order-info-address i {
    font-size: 6vw;
}

.wrapper .order-info p {
    font-size: 3vw;
}

.wrapper h3 {
    box-sizing: border-box;
    padding: 3vw;
    font-size: 4vw;
    color: #666;
    border-bottom: solid 1px #DDD;
}

/****************** 订单明细部分 ******************/
.wrapper .order-detailed {
    width: 100%;
}

.wrapper .order-detailed li {
    width: 100%;
    height: 16vw;
    box-sizing: border-box;
    padding: 3vw;
    color: #666;

    display: flex;
    justify-content: space-between;
    align-items: center;
}

.wrapper .order-detailed li .order-detailed-left {
    display: flex;
    align-items: center;
}

.wrapper .order-detailed li .order-detailed-left img {
    width: 10vw;
    height: 10vw;
}

.wrapper .order-detailed li .order-detailed-left p {
    font-size: 3.5vw;
    margin-left: 3vw;
}

.wrapper .order-detailed li p {
    font-size: 3.5vw;
}

.wrapper .order-deliveryfee {
    width: 100%;
    height: 16vw;
    box-sizing: border-box;
    padding: 3vw;
    color: #666;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 3.5vw;
}

/****************** 订单合计部分 ******************/
.wrapper .total {
    width: 100%;
    height: 14vw;

    position: fixed;
    left: 0;
    bottom: 0;

    display: flex;
}

.wrapper .total .total-left {
    flex: 2;
    background-color: #505051;
    color: #fff;
    font-size: 4.5vw;
    font-weight: 700;
    user-select: none;

    display: flex;
    justify-content: center;
    align-items: center;
}

.wrapper .total .total-right {
    flex: 1;
    background-color: #38CA73;
    color: #fff;
    font-size: 4.5vw;
    font-weight: 700;
    user-select: none;
    cursor: pointer;

    display: flex;
    justify-content: center;
    align-items: center;
}
</style>