# Add domain to hosts file

```shell
echo '<% tp.frontmatter["RHOSTS"] %> <% tp.frontmatter["VHOST"] %>' | sudo tee -a /etc/hosts
```