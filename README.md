# QR--ajax
+ ajax请求实现二维码展示
+ 需要后台把二维码字符串转为base64加密方式，前端也用base64接收
-----
          $.ajax({
                    type:"POST",
                    url:"controller/payment/payToClp/payToClp",
                    data: {
                        paymentId:paymentId,
                        clpType:"1"
                    },
                    contentType:"application/x-www-form-urlencoded;charset=UTF-8",
                    success: function (data) {
                        $("img").attr("src",'data:image/png;base64,'+data);
                    }
                })
-----
