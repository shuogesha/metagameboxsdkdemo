# metagameboxsdkdemo
metagameboxsdk Android sdk demo project

MetaGameBox pay SDK 实例代码：
//签名
public String getPostData(String amount,String orderNo) {
    Map<String, String> sParaTemp = new HashMap<String, String>();
    sParaTemp.put("service", "coinPayTask");
    sParaTemp.put("appId", "9d08ac72345240f69560cf3a70ad9026");
    sParaTemp.put("appKey", "ewq2022");
    sParaTemp.put("amount", amount);
    sParaTemp.put("timestamp",String.valueOf(System.currentTimeMillis()/1000));
    sParaTemp.put("orderNo", orderNo);
    String str= MetaBoxUtil.createLinkString(sParaTemp);
    String mysign =MetaBoxUtil.MD5(str);
    System.out.println(mysign);
    sParaTemp.put("sign", mysign);
    sParaTemp=MetaBoxUtil.keyFilter(sParaTemp);
    return MetaBoxUtil.createLinkString(sParaTemp);
}

public void AndroidThunkJava_MetaGameBoxPay(String orderParam){
    final String orderInfo = orderParam;
    System.out.println(orderInfo);
    com.metadreamer.sdk.app.PayTask pay = new com.metadreamer.sdk.app.PayTask(DemoActivity.this);
    pay.payCoin(orderInfo, new OnPayResultListener() {

        @Override
        public void OnSuccess(String data) {
            Toast.makeText(getApplicationContext(), data,
                    Toast.LENGTH_SHORT).show();
        }
        @Override
        public void OnFail() {
            Toast.makeText(getApplicationContext(), "OnFail",
                    Toast.LENGTH_SHORT).show();
        }
    });
}
//其它app 发起一次支付的调用方式
AndroidThunkJava_MetaGameBoxPay(getPostData("0.1","20220232301223"));
