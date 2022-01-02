# 林文浩的个人主页


## 简单介绍
-学校：福州大学  \
-学院：软件学院  \
-专业：软件工程  \
-学号：222000416  \
-电子邮箱：2604951145@qq.com  

### 爱好
-游戏  \
-动画  \
-写代码  

### 技能
-C/C++ \
-算法与数据结构 

### 荣誉
-福州大学2020\~2021第一学年一等奖学金  \
-福州大学2020\~2021第二学年一等奖学金  \
-多次获得福州大学"前海杯"程序设计竞赛优秀奖  

### 曾发表的文章
<a href="https://www.luogu.com.cn/blog/SenriAkane/solution-cf1601b">CF1601B题解</a><br/>
<a href="https://www.luogu.com.cn/blog/SenriAkane/solution-cf1552b">CF1552B题解</a><br/>
### 图片
<style type="text/css">

        div,ul,li{
            margin: 0;
            padding: 0;
        }


        .container{
            width: 500px;
            height: 280px;
            position: relative;
            top: 0px;
            left: 30%;
            /*border: 1px solid #ccc;*/
        }


        .container img{
            position: absolute;       
            width: 100%;
            transition-duration: 1s;   
            opacity: 0;             
        }

        .container img.on{
            opacity: 1;               
        }

 
        .left, .right{
            position: absolute;
            top: 30%;
            width: 60px;
            height: 100px;
            line-height: 100px;
            background-color: #666;
            opacity: 0.5;
            text-align: center;
            font-size: 60px;
            color: #ccc;
            display: none;    
            cursor: pointer;    
        }
        .left{
            left: 0;
        }
        .right{
            right: 0;
        }
        .container:hover .left, .container:hover .right{
            display: block;           
        }
        .left:hover, .right:hover{
            color: #fff;
        }

  
        .container ul{
            position: absolute;
            bottom: 0;
            max-width: 500px;
            padding: 5px 200px;
        }
        .container ul li{
            list-style: none;
            float: left;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-left: 10px;
            background-color: #ccc;
            cursor: pointer;
        }
        .container ul li.active{
            background-color: #fff;      

    </style>
</head>
<body>
    <div class="container">

        <img class="on" src="img/1.jpg" />
        <img src="img/2.jpg" />
        <img src="img/3.jpg" />
        <img src="img/4.jpg" />
        <img src="img/5.jpg" />

 
        <div class="left"><</div>
        <div class="right">></div>

        <!-- 焦点 -->
        <ul>
            <li class="active"></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </div>


    <script type="text/javascript">
    
        var aImgs = document.querySelectorAll('.container img');
        var aLis = document.querySelectorAll('.container li');
        var btnLeft = document.querySelector('.container .left');
        var btnRight = document.querySelector('.container .right');

    

 
        var index = 0;     
        var lastIndex = 0;
        btnRight.onclick = function(){
          
            lastIndex = index;
        
            aImgs[lastIndex].className = '';
            aLis[lastIndex].className = '';

            index++;
            index %= aImgs.length;   
        
            aImgs[index].className = 'on';
            aLis[index].className = 'active';
        }
   
        btnLeft.onclick = function(){
       
            lastIndex = index;
      
            aImgs[lastIndex].className = '';
            aLis[lastIndex].className = '';

            index--;
            if (index < 0) {
                index = aImgs.length - 1;
            }
           
            aImgs[index].className = 'on';
            aLis[index].className = 'active';
        }
    </script>
</body>
</html>
