# Create the linux boot image

## Download binary images for RoadRunner SOM

<figure markdown>
  ![Debian microsd](https://www.acmesystems.it/www/download_roadrunner/debian_microsd.jpg){ align=left, width="300" }
  ![RoadRunner](https://www.acmesystems.it/photos/products_640/ROADRUNNER-Q16.jpg){ width="300" }
  <figcaption>Image caption</figcaption>
</figure>

### Kernel Linux 5.15.68 - Debian Bullseye 11.5 - At91boostrap 4.0.4

[Download](https://www.acmesystems.it/download/microsd/roadrunner-30nov2022/debian-bullseye-roadrunner.img.xz)

> MD5SUM: 6f30451497fd9230f5263311009805c9

It is possible to generate a bootable microSD from this image using [Balena Etcher](https://www.balena.io/etcher/) on any platform.

At prompt via debug port interface or via lan using SSH the login data are:

```yaml
login: acme
Password: acmesystems
```

!!! note

    To extend the rootfs partition to fill the whole microSD size type:

    ```console
    sudo ./extend_rootfs.sh
    ```

    The password for the root user is not defined. To set it log in as acme user and type:

    ```console
    sudo passwd
    ```

## Compiling AT91bootstrap 4.0.4
