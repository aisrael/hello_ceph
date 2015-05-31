CFLAGS=-std=c99

ceph-client:
	gcc $(CFLAGS) ceph-client.c -lrados -o ceph-client
clean:
	if [ -f ceph-client ]; then rm ceph-client; fi
