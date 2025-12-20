**Tip**: if encountering image pull issues on the workers change the dns resolve

```bash
# Remove the existing link
sudo rm /etc/resolv.conf

# Create a new file with a working nameserver
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf

# restart worker
sudo systemctl restart k3s-agent
```

Then just redeploy 