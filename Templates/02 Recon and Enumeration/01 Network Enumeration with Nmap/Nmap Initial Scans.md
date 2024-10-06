## Initial Nmap Scan

### TCP
#### Step 1
```bash
nmap -p- -Pn -vv <% tp.frontmatter["RHOSTS"] %> -oN <% tp.frontmatter["RHOSTS"] %>-ports
```

#### Step 2

```bash
ports=$(grep '^[0-9]' <% tp.frontmatter["RHOSTS"] %>-ports | cut -d '/' -f 1 | tr '\n' ',' | sed s/,$//)
```

#### Step 3
```bash
nmap -A -Pn -p $ports -vv <% tp.frontmatter["RHOSTS"] %> -oA <% tp.frontmatter["RHOSTS"] %>-aggressive-scan 
```

### UDP

```shell
sudo nmap -sU -Pn -vv <% tp.frontmatter["RHOSTS"] %>
```
