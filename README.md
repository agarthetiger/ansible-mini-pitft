# mini-pitft

Configure a Raspberry Pi for an adafruit mini-pitft display running RaspbianOS. This role automates the process outlined [here](https://learn.adafruit.com/adafruit-mini-pitft-135x240-color-tft-add-on-for-raspberry-pi/python-setup) to setup python support for a mini pi-tft display. 

Important to note two key points up front, taken from the guide above.

Firstly, this is not a kernel driver that will let you have the console appear on the TFT. However, this is handy when you can't install an fbtft driver, and want to use the TFT purely from 'user Python' code!

Secondly, you can only use this technique with Linux/computer devices that have hardware SPI support, and not all single board computers have an SPI device so check before continuing.

This has been written for use with a Raspberry Pi Zero running [pi-hole](https://pi-hole.net/) with a [mini-pitft display](https://learn.adafruit.com/pi-hole-ad-blocker-with-pi-zero-w/install-mini-pitft) for the stats.

I've not attempted to optimise this role so the tasks in tasks/main.yml follow the manual steps in the guide above. Hopefully anyone new to Ansible will be able to read and understand what this Role is doing if they choose to look at the source on GitHub, which I always recommend doing.

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

As there are no variables for this role running this role is about as easy as it gets. 

```yaml
    - hosts: servers
      roles:
         - agarthetiger.ansible-mini-pitft
```

## License

MIT

## Author Information

Andrew Garner (@agarthetiger)
