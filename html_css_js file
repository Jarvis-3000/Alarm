<html>

<head>
 //   <script src="alarm.js"></script>
    <style>
        #container {
            width: 350px;
            height: auto;
            position: absolute;
            top: 30%;
            left: calc(50% - 175px);
        }
        
        button {
            width: 175px;
            /* border: 1px solid gray; */
            padding: 10px;
            text-align: center;
            font-size: 20px;
            outline: none;
        }
        
        #btn1 {
            background-color: whitesmoke;
        }
        
        #btn2 {
            background-color: #c8c7c8;
        }
        
        #box {
            /* border: 1px solid black; */
            border-top: none;
            border-bottom-left-radius: 5px;
            border-bottom-right-radius: 5px;
            background-color: #c8c7c8;
            margin-top: -22px;
        }
        
        #timeContainer {
            text-align: center;
        }
        
        #dateContainer {
            text-align: center;
        }
        
        input {
            width: 80px;
            height: 30px;
            padding: 5px;
            outline: none;
            border: none;
        }
        
        span {
            border: 1px solid black;
        }
        
        #inp {
            display: inline-flex;
        }
    </style>

</head>

<body>

    <div id="container">
        <!-- Option buttons -->

        <button id="opt1" style="margin-right:-4px; border-top-left-radius: 5px;">Time</button>
        <button id="opt2" style="border-top-right-radius: 5px;">Date</button>


        <div id="box">
            <!-- the time section -->
            <div id="timeContainer">
                <br><br>
                <h1>SET THE TIME</h1>
                <div id="inp">
                    <span><input type="number" class="time_edit" placeholder="Hour"></span>
                    <span><input type="number" class="time_edit" placeholder="Minute"></span>
                    <span><input type="number" class="time_edit" placeholder="Second"></span>
                </div> <br><br><br><br>
                <button onclick="alarm1()">Set The Time</button>
                <br><br>
            </div>
            <!-- the date section -->
            <div id="dateContainer">
                <br><br>
                <h1>SET THE DATE</h1>
                <div id="inp">
                    <span><input type="text" class="date_edit" placeholder="Date"></span>
                    <span><input type="text" class="date_edit" placeholder="Month"></span>
                    <span><input type="text" class="date_edit" placeholder="Year"></span>
                </div> <br><br><br><br>
                <button onclick="alarm2()">Set The Date</button>
                <br><br>
            </div>
        </div>
    </div>

    <script>
        var timeContainer = document.getElementById("timeContainer");
        var dateContainer = document.getElementById("dateContainer");
        var btn1 = document.getElementById("opt1");
        var btn2 = document.getElementById("opt2");


        dateContainer.style.display = "none";

        btn1.addEventListener("click", tc);
        btn2.addEventListener("click", dc);

        function tc() {
            dateContainer.style.display = "none";
            timeContainer.style.display = "block";

        }

        function dc() {
            dateContainer.style.display = "block";

            timeContainer.style.display = "none";
        }
        
        
        
        var count;
var ok = 1;

function alarm1() {
    var time_edit = document.getElementsByClassName("time_edit");
    var val = ((time_edit[0].value) * (time_edit[1].value) * (time_edit[2].value));

    // setting the time cookie

    document.cookie = "Name=Satish; max-age=" + val;
    document.cookie = "Time=bill; max-age=" + val * 2;
    count = 2;
    alert("Alarm set successfully !")
    var i = 1;
    setInterval(function() { if (ok) { check(i); } }, 2000);

}

function alarm2() {
    var date_edit = document.getElementsByClassName("date_edit");
    var val = (date_edit[0].value * 1).toString() + "-Apr-" + "2020";
    alert(val);

    // setting the time cookie

    document.cookie = "Name=Satish; expires=Fri, 16-Apr-2020 19:13:00 UTC";
    alert(document.cookie);
    document.cookie = "Time=bill; max-age=" + 120 * 2;
    count = 2;
    var i = 1;
    alert("Alarm set successfully !")
    setInterval(function() { if (ok) { check(i); } }, 2000);

}



function check(i) {

    if (i != 0) {
        var l = document.cookie.split(";");
        if (l.length != 2) {
            alert("Please pay your bill first");
            ok = 0;
            window.open("https:\\www.youtube.com");
        }
    } else {
        alert("Welcome Again !");
    }
}

if (document.cookie == "") {
    alert("Welcome !");
} else {
    var i = 0;
    if (ok) {
        setInterval(function() {
            if (ok) { check(i); }
            i++;
        }, 2000);
    }
}
    </script>
    
</body>

</html>
