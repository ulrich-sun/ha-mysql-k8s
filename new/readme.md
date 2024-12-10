 kubectl exec --stdin  --tty mysql-0 -- /bin/sh -c "mysql -uroot -proot -e 'SELECT * FROM performance_schema.replication_group_members;'"




 watch kubectl exec --stdin  --tty mysql-0 -- /bin/sh -c "mysql -uroot -proot -e 'SELECT count(*) FROM myDB.test;'"





 kubectl exec --stdin  --tty mysql-1 -- /bin/sh -c "mysql -uroot -proot -e 'SELECT count(*) FROM myDB.test;'"


kubectl exec --stdin --tty mysql-0 -- /bin/sh -c "mysql -uroot -proot -e 'SHOW STATUS LIKE \"group_replication_recovery_progress\";'"
