## cat /etc/exports

\# /mnt/media 192.168.1.0/24(rw,sync,no_subtree_check,no_root_squash)

/mnt/media 10.0.1.3/24(rw,sync,no_subtree_check,no_root_squash)

/mnt/media 10.0.1.4/24(rw,sync,no_subtree_check,no_root_squash)

/mnt/media/Downloads 10.0.4.6/24(rw,sync,no_subtree_check,no_root_squash)

## sudo exportfs -v

/mnt/media    	10.0.1.3/24(sync,wdelay,hide,no_subtree_check,sec=sys,rw,secure,no_root_squash,no_all_squash)
/mnt/media    	10.0.1.4/24(sync,wdelay,hide,no_subtree_check,sec=sys,rw,secure,no_root_squash,no_all_squash)
/mnt/media/Downloads
		10.0.4.6/24(sync,wdelay,hide,no_subtree_check,sec=sys,rw,secure,no_root_squash,no_all_squash)

## sudo systemctl status nfs-server
● nfs-server.service - NFS server and services
     Loaded: loaded (/usr/lib/systemd/system/nfs-server.service; enabled; preset: enabled)
    Drop-In: /run/systemd/generator/nfs-server.service.d
             └─order-with-mounts.conf
     Active: active (exited) since Sat 2026-02-07 16:27:40 UTC; 2 weeks 1 day ago
   Main PID: 1231 (code=exited, status=0/SUCCESS)
        CPU: 13ms

Feb 07 16:27:40 nas systemd[1]: Starting nfs-server.service - NFS server and services...
Feb 07 16:27:40 nas systemd[1]: Finished nfs-server.service - NFS server and services.