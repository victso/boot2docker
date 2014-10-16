# Boot2Docker Build

You can clone this repositiory. Cd in to it and build the image:

	$ docker build -t user/boot2docker .

	
It takes a little while. Once finished you need to to extract it's iso. This is how I've done it:

	$ docker run -i -t --rm user/boot2docker /bin/bash

open a new terminal

	$ docker cp <Container-ID>:boot2docker.iso image

You'll find the iso file inside the dir image.

At this point stop your current boot2docker

	$ boot2docker stop

Do a backup

	$ mv ~/.boot2docker/boot2docker.iso ~/.boot2docker/boot2docker.iso.backup

replace the image file with:

	$ mv image/boot2docker.iso ~/.boot2docker/boot2docker.iso

[Comment](https://github.com/boot2docker/boot2docker/pull/534#issuecomment-56432262)
