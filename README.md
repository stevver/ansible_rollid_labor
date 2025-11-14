# Ansible Role: Nginx

Paigaldab Nginx web serveri. Toetab mitut keskkonda (dev, staging, prod).

## Muutujad

Kohustuslikud (määra playbook'is):
- `nginx_environment`: näiteks `"production"`
- `site_title`: näiteks `"My Site"`
- `site_color`: näiteks `"#00AA00"`

Valikulised:
- `nginx_workers`: töötajate arv (default: CPU arv)
- `nginx_port`: vaikimisi 80
- `nginx_hostname`: vaikimisi `"localhost"`

## Näited

Development:

```yaml
- role: nginx
  vars:
    nginx_environment: "development"
    nginx_workers: 1

Production:

```yaml
- role: nginx
  vars:
    nginx_environment: "production"
    nginx_workers: 4

## Test

ansible-playbook -i inventory dev.yml
ansible-playbook -i inventory prod.yml

## Author

Stever
