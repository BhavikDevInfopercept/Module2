var express = require('express');
var bodyParser = require('body-parser');
var app = express();

/*app.use(function middleware(req,res,next){
  console.log(req.method + " " + req.path + " - " + req.ip);
  next();
});*/

// express hello world
/*app.get("/",function(req,res)
{
  res.send("Hello Express");
});*/

// attaching the assets files i.e. css,js and bootstrap files
app.use("/public",express.static(__dirname + "/public"));
app.get("/",function(req,res)
{
  absolutePath = __dirname + "/views/index.html";
  res.sendFile(absolutePath);
});

// return json object
/*app.get("/json",function(req,res)
{
  if(process.env.MESSAGE_STYLE == "uppercase")
  {
    res.json({"message": "HELLO JSON"});
  }
  else
  {
    res.json({"message": "Hello json"});
  }
  
});*/

// applying middleware function with chain
/*app.get("/now",function(req,res,next){
  req.time = new Date().toString();
  next();
},function(req,res){
  res.json({"time":req.time});
});*/

//URLs parameters
/*app.get("/:word/echo",function(req,res){
  res.json({"echo":req.params.word});
});*/

//query string using route, get and post method
/*app.get("/name",function(req,res){
  req.firstName = req.query.first;
  req.lastName = req.query.last;
  res.json({name : `${req.firstName} ${req.lastName}`});
});*/

app.use(bodyParser.urlencoded({extended:false}));
app.use(bodyParser.json());

app.post("/name",function(req,res){
  res.json({"name": req.body.first+" "+req.body.last});
});





 module.exports = app;
