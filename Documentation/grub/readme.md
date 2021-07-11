<h2><a href="https://github.com/mahendragandham/Conqueror/blob/main/boot/grub/grub.cfg"><b>[ grub.cfg ]</b></a></h2>
<h3>Getting Started with <a href="https://github.com/mahendragandham/Conqueror/blob/main/boot/grub/grub.cfg"><b>[ grub.cfg ]</b></a></h3>
<ul>
  <li>Set default to 0              =>  set default=0</li>
  <li>Set timeout to 0              =>  set timeout=0</li>
  <li>Let's create <b>Menuentry</b> and name it with OS Name => menuentry "Conqueror"</li>
  <li>Declare the <b>Kernel Version</b> with linux keyword
  </br><b>linux /boot/vmlinuz-4.19.0-10-amd64</b></li>
  <li>We need to set Root Partition. For that, Assign path of sdb1 to <b>[ root ]</b> keyword</li>
  <li>Declare the version of <b>Initial Ram Disk</b> with initrd keyword
  </br><b>initrd /boot/initrd-4.19.0-10-amd64</b></li>
</ul>
<p>Above all this, the code is in the following:</p>
<pre>
set default=0
set timeout=0
menuentry "Conqueror" {
  linux /boot/vmlinuz-4.19.0-10-amd64 root=/dev/sdb1 ro
  initrd /boot/initrd-4.19.0-10-amd64
}
</pre>


  
