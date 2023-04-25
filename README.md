<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-/bQdsTh/da6pkI1MST/rWKFNjaCP5gBSY4sEBT38Q/9RBh9AH40zEOg7Hlq2THRZ" crossorigin="anonymous"></script>
<script>
    $(function () {
        console.log("aaaa");
        //callAPI();
        callPostCodeAPI("");
    });

    function callPostCodeAPI(addr) {
        var url ="http://zip5.5432.tw/zip5json.py?adrs="+addr
    ....
        console.log(url); //for debug
        $.ajax({
            url: url,
            dataType: "json",
            type: "get",
            //data: data,
//Type: Function(Anything data, String textStatus, jqXHR jqXHR)
            success: function (data, textStatus, jqXHR) {
                console.log(JSON.stringify(data));
            },
//Type: Function(jqXHR jqXHR, String textStatus, String errorThrown)
            error: function (jqXHR, textStatus, errorThrown) {

            }
        });
    }
</script>
</body>
</html>
