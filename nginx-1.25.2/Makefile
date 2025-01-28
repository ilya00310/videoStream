
default:	build

clean:
	rm -rf Makefile objs

.PHONY:	default clean

build:
	$(MAKE) -f objs/Makefile

install:
	$(MAKE) -f objs/Makefile install

modules:
	$(MAKE) -f objs/Makefile modules

upgrade:
	/home/ilya/videoStream/nginx-1.25.2/sbin/nginx -t

	kill -USR2 `cat /home/ilya/videoStream/nginx-1.25.2/logs/nginx.pid`
	sleep 1
	test -f /home/ilya/videoStream/nginx-1.25.2/logs/nginx.pid.oldbin

	kill -QUIT `cat /home/ilya/videoStream/nginx-1.25.2/logs/nginx.pid.oldbin`

.PHONY:	build install modules upgrade
