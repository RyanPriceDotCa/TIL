Map disks in linux to SCSI as displayed in vSphere:

```bash
ls -d /sys/block/sd*/device/scsi_device/* |awk -F '[:/]' '{print $4,"- SCSI",$8":"$9}'
```
