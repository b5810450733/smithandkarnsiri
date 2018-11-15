<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
    <style>
        .text-smith{
            color: whitesmoke;
        }
        #headerText{
            padding: 20px;
            margin-bottom: 30px;
            transition:0.5s;
        }
        #headerText:hover{
            color: whitesmoke;
        }
        .headerZone{
            background: linear-gradient(45deg, #ea6c6e 0%, #f6bd74 100%);
            width: 100%;
        }
        #loading{
            width: 60%;
            position: absolute;
            top: -280px;
            left: 400px;
        }
    </style>
</head>
<body>
<div class="headerZone">
    <h1 class="text-smith" id="headerText">Text Detection by Smith</h1>
    <br>
    <hr>
    <p></p>
</div>
<div class="container">
    <div class="row">
        <div class="col-6 col-sm-6">
            <p></p>
            <input id="file" type="file"  class="form-control"/>
            <hr>
            <div class="row">
                <div class="col-6">
                    <img src="" alt="" id="preview" class="img-fulid" style="width: 200px; max-width: 200px; height: auto" >
                    <p></p>
                    <button id="button" class="btn btn-info">Detection</button>
                </div>
                <div class="col-6 text-center">
                    <img src="imgs/loading.svg" width="250px;" style="display: none;" id="loading">
                    <p><h1 id="price" class="text-center text-success"></h1></p>
                </div>
            </div>
        </div>
        <div class="col-6 col-sm-6">
            <h5>Base64</h5>
            <textarea name="" id="test" cols="100" rows="5" class="form-control"></textarea>
            <p></p>
            <h5>Respones</h5>
            <textarea name="" id="respones" cols="100" rows="5" class="form-control"></textarea>
            <p></p>
            <h5>Query</h5>
            <textarea name="" id="query" cols="100" rows="5" class="form-control"></textarea>
        </div>
    </div>
</div>

<div>
    <img src="imgs/logo-som.png" width="200px" style="z-index: 0;position: absolute;left: 300px;top: 800px;" id="logoShow">
    <img src="imgs/box.jpg" width="800px" style="z-index: 1">
    <p></p>
    <hr>
    <div class="row">
        <div class="col-md-6">
            <input type="range" min="1" max="600" value="300" id="widthSlider">
            <p id="widthValue">Left - Right</p>
            <input type="range" min="700" max="1100" value="800" id="heiSlider">
            <p id="heiValue">Top - Button</p>
        </div>
        <div class="col-md-6">
            <input type="range" min="1" max="500" value="250" id="changeSize">
            <p id="changeSize">Width - Height</p>
            <input type="range" min="0" max="360" value="0" id="rotate">
            <p id="changeSize">Rotate</p>
        </div>
    </div>


</div>



</body>
</html>

<script type="text/javascript">
  document.getElementById('button').addEventListener('click', function() {
    var files = document.getElementById('file').files;
    if (files.length > 0) {
      getBase64(files[0]);
    }
  });

  function getBase64(file) {
      $('#loading').show();
    var reader = new FileReader();
    reader.readAsDataURL(file);
    reader.onload = function () {

      $('#preview').attr('src',reader.result);
      var base64 = reader.result.replace("jpeg","png");
      base64 = base64.substr(22);
      console.log(reader.result);
      $('#test').text(base64);
      var b = JSON.stringify({   "requests": [     {       "image": {         "content": base64       },       "features": [         {           "type": "TEXT_DETECTION"         }       ]     }   ] });
      var e = new XMLHttpRequest;
      e.onload=function(){
        $('#respones').text(e.responseText);
        var parsed = JSON.parse(e.responseText);
        var allDesc = parsed["responses"][0]["textAnnotations"];
        $('#query').text(allDesc[0]["description"]);

        // for each
        var iFoundIt = -1;
        for (var i in allDesc) {
          let string = allDesc[i]["description"];
          if (string.indexOf("THB") != -1){
            iFoundIt = parseInt(i)+1;
          }
        }

        if(iFoundIt != -1){
            $('#price').text("Price is : "+allDesc[iFoundIt]["description"]);
            $('#loading').hide();
        }else{
            $('#price').text("Not price.");
            $('#loading').hide();
        }

      };
      e.open("POST","https://vision.googleapis.com/v1/images:annotate?key=AIzaSyDojrPs_7996MrPXVnG-TuC2d2Rjex08hI",!0);
      e.send(b)


    };
    reader.onerror = function (error) {
      console.log('Error: ', error);
    };
  }

  $('#widthSlider').on("change mousemove", function() {
      var leftValue = parseInt($(this).val());
      $('#logoShow').css({left: leftValue, position:'absolute'});
      // console.log($(this).val());
  });
  $('#heiSlider').on("change mousemove", function() {
      var topValue = parseInt($(this).val());
      $('#logoShow').css({top: topValue, position:'absolute'});
      // console.log($(this).val());
  });
  
  $('#changeSize').on("change mousemove", function () {
      var sizeValue = parseInt($(this).val());
      $('#logoShow').css({width: sizeValue, height:'auto', position:'absolute'})
      
  });
    $('#rotate').on("change mousemove", function () {
          var rotateValue = parseInt($(this).val());
          $('#logoShow').css({ WebkitTransform: 'rotate(' + rotateValue + 'deg)'})

      });

  </script>