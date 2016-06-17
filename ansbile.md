# 1. ansbile 学习总结

## 1.1 安装

###
	$sudo easy_install pip
	$sudo pip install ansible

##1.2 默认配置
### ansbile.cfg

###
	[defaults]
	hosts=inventory.pro_diwh
	remote_user = david
	host_key_checking = False  # 不检查密码或者 export ANSIBLE_HOST_KEY_CHECKING=False

	remote_port = 16688
###


## 1.3 Inventory

###
    $more inventory.pro_diwh
    en0 ansible_host=139.196.231.46 ansible_port=16688 ansible_user=david
    en1 ansible_host=139.196.231.45  # 使用ansible.cfg中的默认值
    
    [nodes]
    en0
    en1
    
###

## 1.4 常见Ad-Hoc命令
###
	ansible all -m ping -u david --become-user root
	
	ansible all -m setup  # 收集servers facts
	
	ansible all -m command -a "/bin/echo hello"  --forks 10 # 启动10个进程处理  
	ansible all -a "/bin/echo hello" # command is default module，可以省略 -m
	
	ansible en1 -m shell -a 'echo $TERM' 
	
	ansible en1 -m copy -a "src=/etc/hosts dest=/tmp/hosts"
	
	ansible en1 -m file -a "dest=/srv/foo/b.txt mode=600 owner=mdehaan group=mdehaan"
	ansible en1 -m file -a "dest=/path/c mode=755 owner=a group=a state=directory" # mkdir -p 
	ansible en1 -m file -a "dest=/path/to/c state=absent" # delete file
	
	ansible en1 -m yum -a "name=acme state=present"
	ansible en1 -m yum -a "name=acme state=absent"
	
	ansible all -m user -a "name=foo password=<crypted password here>" # set foo password
	ansible all -m user -a "name=foo state=absent"  # delete user foo
	
	 ansible en1 -m git -a "repo=git://foo.example.org/repo.git dest=/srv/myapp version=HEAD"
	 
	 ansible en1 -m service -a "name=httpd state=started"
	 ansible en1 -m service -a "name=httpd state=restarted"
	 ansible en1 -m service -a "name=httpd state=stopped"
	
	ansible-doc -l   # 查看安装module列表  
	ansible-doc yum  # 查看module yum的帮助文档
###

###see: 
1. [Ad_hoc cmd](http://docs.ansible.com/ansible/intro_adhoc.html) <br>
2. [Module list](http://docs.ansible.com/ansible/modules.html)   [Module Index](http://docs.ansible.com/ansible/modules_by_category.html) <br>  
3. [Core module](https://github.com/ansible/ansible-modules-core)
4. [Extra module](https://github.com/ansible/ansible-modules-extras)

## 出错处理
###
	- name: this will not be counted as a failure
  	  command: /bin/false
  	  ignore_errors: yes
###

## 安装网桥相关工具
###
	# yum install bridge-utils
	# service docker stop
	# ip link set dev docker0 down
	# brctl delbr docker0