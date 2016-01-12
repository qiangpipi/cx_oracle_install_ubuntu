### cx_oracle_install_ubuntu

**My ENV**
- Fresh Ubuntu 1404 LTS
- Python 2.7
- [Ubuntu official guide for installing oracle client](https://help.ubuntu.com/community/Oracle%20Instant%20Client)
- [Oracle resource] (http://www.oracle.com/technetwork/topics/linuxx86-64soft-092277.html)

**Step by step**

```
sudo apt-get install python-dev
sudo apt-get install alient
sudo apt-get install libaio1
```

Download:
- oracle-instantclientxx.x-basiclite-xx.x.x.x.x-x.x86_64.rpm
- oracle-instantclientxx.x-sqlplus-xx.x.x.x.x-x.x86_64.rpm
- oracle-instantclientxx.x-devel-xx.x.x.x.x-x.x86_64.rpm

```
sudo alient -i oracle-instantclientxx.x-basiclite-xx.x.x.x.x-x.x86_64.rpm
sudo alient -i oracle-instantclientxx.x-sqlplus-xx.x.x.x.x-x.x86_64.rpm
sudo alient -i oracle-instantclientxx.x-devel-xx.x.x.x.x-x.x86_64.rpm
```

Download:
- [cx_oracle source code](https://pypi.python.org/pypi/cx_Oracl)

```
tar -xvf cx_Oracle-x.x.tar.gz -C ~/.
cd ~/cx_Oracle-x.x/
python setup.py build
sudo python setup.py install
echo "export ORACLE_HOME=/usr/lib/oracle/xx.x/client64" >> ~/.bashrc
echo "export PATH=${ORACLE_HOME}/bin:${PATH}" >> ~/.bashrc
echo "export LD_LIBRARY_PATH=${ORACLE_HOME}/lib:${LD_LIBRARY_PATH}" >> ~/.bashrc
source ~/.bashrc
sqlplus username/password@//dbhost:1521/SID
```

**It should work here!!**
