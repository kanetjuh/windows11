# Windows 11

This is the unofficial documentation on how to install Windows 11.

We highly recommend you to read EVERY SINGLE LINE for installing Windows 11, otherwise we aren't responsible for the problems you cause.

# Installing
In the first instances, you need to download the .iso file to boot your PC with it in the future!                  
To do this there are many possibilities on the internet, but I have listed the download links I used below.

Download the Windows 11 Beta 21996.iso file [here](https://drive.google.com/file/d/1J6dPZMr5dlZyrrzTTPzaUCeV0yHaZTAk/view).
> Note: `Secure Boot and TPM` must be enabled in Bios (For the above .iso file)!

Download the Windows 11 Non TPM 2.0 Non Bootable.iso [here](https://drive.google.com/file/d/1QGvcjEM_SM1eDnoHYzSxSe9wq_t5Jpsw/view)

## One more installation required! ##

If you have downloaded one of the .iso files that is best for your PC, you need to create a so-called `Bootable USB` that you will start with further in this tutorial Windows 11 installation menu.

To create a 'Bootable USB' you need a program called 'Rufus'
> Rufus is a small application that creates bootable USB drives, which can then be used to install or run Microsoft Windows, Linux or DOS. In just a few minutes, and with very few clicks, Rufus can help you run a new Operating System on your computer.

Download Rufus [here](https://rufus.ie/)

## Creating the bootable USB ##

Now it is finally time to start the real thing, because we now have to make a bootable USB in rufus, to do this you have to open Rufus!

> Note: Most of the time 8 GB is enough, 16 GB is guaranteed to be enough (This is for the USB we will be using)
>> !!! Important: All data you have on that USB will be deleted when you make a bootable USB, so we advise you to make a backup of it, or put it on another PC / USB!

Now open the program called `Rufus`, it should look like this when you opened it
> Note: On the screenshot my disk (USB) is already selected
> I've already inserted the USB (Which I recommend doing before opening the program)



```js
// requires
var express = require("express");
var lxd = require("node-lxd");
var client = lxd();
var app = express();

var containers = {};

app.post("/create", function(req, res) {
	client.launch(req.query.name, function(err, container) {
		if (err) res.json({success: false, message: err.getMessage()});
		else {
			containers[req.query.name] = container;
			res.json({success: true, message: "Container launched"});
		}
	});
});

app.post("/run", function(req, res) {
	if (!containers.hasOwnProperty(req.query.name)) {
		res.json({success: false, message: "Container does not exist"});
		return;
	}

	containers[req.query.name].run(req.query.cmd.split(" "), function(err, stdOut, stdErr) {
		if (err) res.json({success: false, message: err.getMessage()});
		else if (stdErr.length > 0) res.json({success: false, message: stdErr});
		else {
			res.json({success: true, message: stdOut});
		}
	});
});

app.listen(3000, function(err) {
	if (!err)
		console.log("listening on port 3000");
});
```

## Documentation ##

The client class is documented [here](https://github.com/Wolfo-Gaming/node-lxd/blob/master/docs/client.md).

The container class is documented [here](https://github.com/Wolfo-Gaming/node-lxd/blob/master/docs/container.md).

The process class is documented [here](https://github.com/Wolfo-Gaming/node-lxd/blob/master/docs/process.md).
