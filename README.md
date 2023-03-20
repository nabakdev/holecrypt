# Simple Dockerized Pi-Hole + DNSCrypt Proxy Setup

Pi-hole is a popular network-level ad-blocking solution that blocks unwanted advertisements and improves internet browsing experience. DNSCrypt is a protocol that encrypts DNS traffic between the client and the server, providing an additional layer of security and privacy.

By combining Pi-hole with DNSCrypt and running them in Docker containers, you can easily set up a secure and efficient ad-blocking and DNS encryption solution for your home network. Docker provides a platform for running applications in isolated containers, which makes installation and configuration of Pi-hole and DNSCrypt easy and straightforward.

With this setup, you can prevent unwanted ads and protect your network from potential malware or phishing attacks that exploit DNS vulnerabilities. Additionally, the encryption of DNS traffic ensures that your online activities are kept private and secure from prying eyes. Overall, this Pi-hole and DNSCrypt setup with Docker provides an efficient, secure, and privacy-focused solution for your home network.

This setup using [pihole-updatelists](https://github.com/jacklul/pihole-updatelists) to manage remote adlists like [firebog](https://v.firebog.net/hosts/lists.php?type=tick) or whitelist like [anudeepND whitelist](https://raw.githubusercontent.com/anudeepND/whitelist/master/domains/whitelist.txt) easily without periodically checking it.

If you are not using remote adlists or whitelist like that, you can replace the pihole image with the official one.

# USAGE

```bash
# clone the repo && cd into `holecrypt`
git clone --depth 1 https://github.com/nabakdev/holecrypt.git holecrypt && cd $_

# copy `.env.example` to `.env`
cp .env.example .env

# start the container until initial launch is complete
sudo docker compose up
# stop container by CTRL+C

# re-start the container to run in background
sudo docker compose up -d
```

### Issues

- [Fix conflict on port 53 on debian based](https://github.com/pi-hole/docker-pi-hole#installing-on-ubuntu-or-fedora)

### Blacklist
- firebog [tick](https://v.firebog.net/hosts/lists.php?type=tick)
- oisd [nsfw](https://nsfw.oisd.nl/), [small](https://small.oisd.nl/), [big](https://big.oisd.nl/)
- 1Hosts [repo](https://github.com/badmojr/1Hosts)
- StevenBlack [repo](https://github.com/StevenBlack/hosts)

