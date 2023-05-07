<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <style>
    
    .card {
    margin: 20px;
    padding: 20px;
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
    }
    .tutorial-link a {
    color: blue; /* 设置链接的文本颜色 */
    text-decoration: underline; /* 添加下划线效果 */
    cursor: pointer; /* 设置鼠标指针为手型，表示链接可以点击 */
    }
    
    .tutorial-link a:hover {
    color: red; /* 设置链接在鼠标悬停时的文本颜色 */
    }

.btn-custom-success {
background-color: #f0ad4e;
border-color: #f0ad4e;
color: #fff;
}

.btn-custom-success:hover,
.btn-custom-success:focus {
background-color: #ffd369; /* 设置鼠标悬停或获取焦点时的背景颜色，可以调整为适合的淡黄色阴影效果 */
border-color: #ffd369; /* 设置鼠标悬停或获取焦点时的边框颜色，与背景色保持一致 */
}

  .module-separator {
  border-top: 1px solid #ccc; /* 设置顶部边框样式和颜色 */
  margin: 10px 0; /* 设置上下外边距 */
  width: 100%; /* 设置线条的宽度 */
  }
    .card-header,
    h5 {
      text-align: center;
    }
  </style>
  <title>Bootstrap Card</title>
</head>

<body>
  <div class="card">
<div class="card-header text-center" style="background-color: white;">
  <h3>集成下载卡片</h3>

<div>
    <div class="card-body">
      <div class="d-flex flex-column align-items-center">
        <div class="mb-4">
  <h5>仓库地址</h5>
  <input type="text" class="form-control" id="repo" placeholder="Your desired placeholder text" ng-model="repo">
</div>
<div>
  <button type="button" class="btn btn-primary" id="send" ng-click="sendRepo()">发送</button>
</div>

    <div class="module-separator"></div>

      <div class="d-flex flex-column align-items-center mt-4">
        <div class="mb-4">
          <h5>最新版本</h5>
          <span id="latest"></span>
        </div>
        <div class="mb-4">
<button type="button" class="btn btn-custom-success" id="download-latest">下载最新版本</button>
        </div>
      </div>

    <div class="module-separator"></div>

      <div class="d-flex flex-column align-items-center mt-4">
        <div class="mb-4">
          <h5>历史版本</h5>
          <select class="form-control" id="history">
            <option value="">请选择历史版本</option>
            <option value="v1.0">版本 1.0</option>
            <option value="v1.1">版本 1.1</option>
            <option value="v1.2">版本 1.2</option>
            <option value="v1.3">版本 1.3</option>
            <option value="v1.4">版本 1.4</option>
            <option value="v1.5">版本 1.5</option>
            <option value="v1.6">版本 1.6</option>
            <option value="v1.7">版本 1.7</option>
          </select>
        </div>
        <div class="mb-4">
          <button type="button" class="btn btn-success" id="download-history">下载历史版本</button>
        </div>

<div class="panel-footer" style="text-align: center;">
  <div class="tutorial-link">
    <a href="#" onclick="openTutorial('{{msg.payload.tutorialURL}}'); return false;">查看教程</a>
  </div>
</div>

      </div>
    </div>
  </div>

  <script>
    var repo = document.getElementById("repo");
    var send = document.getElementById("send");
    var latest = document.getElementById("latest");
    var downloadLatest = document.getElementById("download-latest");
    var history = document.getElementById("history");
    var downloadHistory = document.getElementById("download-history");

    send.addEventListener("click", function() {
      var repoValue = repo.value;
        if (repoValue) {
        // Send the repository address to downstream nodes
        scope.send({ payload: repoValue });
        } else {
        alert("请输入集成在 GitHub 的仓库地址");
        }
        });
        
        downloadLatest.addEventListener("click", function() {
        var latestValue = latest.textContent;
        if (latestValue) {
        // Send the latest version information to downstream nodes
        scope.send({ payload: latestValue });
        } else {
        alert("没有最新版本信息");
        }
        });

          function openTutorial(url) {
          window.open(url, "_blank");
          };

  (function(scope) {
  scope.sendRepo = function() {
  scope.send({payload: scope.repo});
  }
  })(scope);
        
        downloadHistory.addEventListener("click", function() {
        var historyValue = history.value;
        if (historyValue) {
        // Send the selected history version information to downstream nodes
        scope.send({ payload: historyValue });
        } else {
        alert("没有历史版本信息");
        }
        });
        </script>
        </body>
        
        </html>
