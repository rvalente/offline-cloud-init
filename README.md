# offline-cloud-init

Create ISO for cloud-init testing with Virtualbox

## Requirements

On macOS you need to install cdrtools

```
brew install cdrtools
```

## Usage

```
tee meta-data <<EOF
instance-id: iid-01234567889abcdef
local-hostname: HOSTNAME
EOF

tee user-data <<EOF
#cloud-config
ssh_authorized_keys: YOUR_PUB_KEY
EOF

make
```
