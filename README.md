# hosts_parser
Made the ability to parse a string of hosts easier.
#### Key Features:
* **Easy**: Designed with simplicity in mind. Uses modern design principle making the code DRY and Extensible.
* **Great Developer Experience**: Being fully typed makes it great for editor support. Want to make your own Action Runner workflow? Just combine or inherit from the pre built components to match your use case.
* **There is More!!!**:
    * [host_reader](https://github.com/tybruno/hosts_reader): retreive a list of host from a file or string.
    * [commands_reader](https://github.com/tybruno/commands_reader): retreive a list of commands from a file or string.
    * [parser](https://github.com/tybruno/parsers): Generic Parsers and Abstract classes. This project extends parsers.
## Installation
`pip install "git+git@github.com:tybruno/hosts_parser.git#egg=hosts_parser`
## Usage
### Example 1
```python
from hosts_parser import HostsParser

hosts_str = "host1, host2, host3"

parse_hosts = HostsParser()

hosts = parse_hosts(hosts_str)

print(list(hosts)) # ['host1', 'host2', 'host3']
```
### Example 2

```python
from hosts_parser import HostsParser

hosts_str = """hosts1
host2
host3
"""

parse_hosts = HostsParser()

hosts = parse_hosts(hosts_str)

print(list(hosts)) # ['host1', 'host2', 'host3']
```
