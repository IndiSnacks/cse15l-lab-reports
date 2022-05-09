# Lab Week 6 - Report 3
## by Sahil Gathe
May 8, 2022ls

# Streamlining ```ssh``` Configuration

![Image](ImagesReport3\sshConfig.png)

1. This is a screen shot of the config file that will allow me to more quicky long into my ```ieng6``` server. In this file I inclue the host, hostname, and my username. These pieces of information are automatially.

![Image](ImagesReport3\ieng6.png)

2. Here we can see that I now no longer need to input my username to get into the ```ieng6``` server simply using the command ```ssh ieng6``` is enough.

![Image](ImagesReport3\scp.png)

3. This also makes using teh ```scp``` command esier since I no longer need to enter my entire ```ssh``` username instead I am able to just use ```ieng6```.

# Setup Github Access from ```ieng6```

![Image](ImagesReport3\gitssh.png)

1. here is a screenshot of the key used by github to acces my ```ieng6`` server.

![Image](ImagesReport3\gitkey.png)

2. Here is where the private key for the public key is stored within my local mechine.

![Image](ImagesReport3\gitsshcommit.png)

3. [Commit Link](https://github.com/IndiSnacks/cse15l-lab-reports/commit/671339d7b520adfe53bf210602dcaaa1953fd566): This to the commit that is commited from ```ieng6``` that is shown above.

# Copy whole directories with ```scp -r```

![Image](ImagesReport3\markdown-phaser.png)

1. In the photo above I use the ```git clone``` command to clone over all of the markdown-phaser directory.

![Image](ImagesReport3\testingInssh.png)

2. The sreenshot show me running the markdown phaser test using the ```make test``` command.

![Image](ImagesReport3\ssh-r.png)

3. Lastly I remove the direcotry form my ``ssh`` and re-copy it using the ```scp -r``` command as seen above. 

