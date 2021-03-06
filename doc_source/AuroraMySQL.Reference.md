# Amazon Aurora MySQL Reference<a name="AuroraMySQL.Reference"></a>

## Amazon Aurora MySQL Parameters<a name="AuroraMySQL.Reference.ParameterGroups"></a>

You manage your Amazon Aurora MySQL DB cluster in the same way that you manage other Amazon RDS DB instances, by using parameters in a DB parameter group\. Amazon Aurora differs from other DB engines in that you have a DB cluster that contains multiple DB instances\. As a result, some of the parameters that you use to manage your Aurora MySQL DB cluster apply to the entire cluster, while other parameters apply only to a particular DB instance in the DB cluster\.

Cluster\-level parameters are managed in DB cluster parameter groups\. Instance\-level parameters are managed in DB parameter groups\. Although each DB instance in an Aurora MySQL DB cluster is compatible with the MySQL database engine, some of the MySQL database engine parameters must be applied at the cluster level, and are managed using DB cluster parameter groups\. Cluster\-level parameters are not found in the DB parameter group for an instance in an Aurora DB cluster and are listed later in this topic\.

You can manage both cluster\-level and instance\-level parameters using the AWS Management Console, the AWS CLI, or the Amazon RDS API\. There are separate commands for managing cluster\-level parameters and instance\-level parameters\. For example, you can use the [modify\-db\-cluster\-parameter\-group](http://docs.aws.amazon.com/cli/latest/reference/rds/modify-db-cluster-parameter-group.html) AWS CLI command to manage cluster\-level parameters in a DB cluster parameter group and use the [modify\-db\-parameter\-group](http://docs.aws.amazon.com/cli/latest/reference/rds/modify-db-parameter-group.html) AWS CLI command to manage instance\-level parameters in a DB parameter group for a DB instance in a DB cluster\.

You can view both cluster\-level and instance\-level parameters in the AWS Management Console, or by using the AWS CLI or Amazon RDS API\. For example, you can use the [describe\-db\-cluster\-parameters](http://docs.aws.amazon.com/cli/latest/reference/rds/describe-db-cluster-parameters.html) AWS CLI command to view cluster\-level parameters in a DB cluster parameter group and use the [describe\-db\-parameters](http://docs.aws.amazon.com/cli/latest/reference/rds/describe-db-parameters.html) AWS CLI command to view instance\-level parameters in a DB parameter group for a DB instance in a DB cluster\.

For more information on DB parameter groups, see [Working with DB Parameter Groups](USER_WorkingWithParamGroups.md)\.

### Cluster\-level Parameters<a name="AuroraMySQL.Reference.Parameters.Cluster"></a>

The following table shows all of the parameters that apply to the entire Aurora MySQL DB cluster\. 


| Parameter name | Modifiable | 
| --- | --- | 
|  `aurora_load_from_s3_role`  |  Yes  | 
|  `aurora_select_into_s3_role`  |  Yes  | 
|  `auto_increment_increment`  |  Yes  | 
|  `auto_increment_offset`  |  Yes  | 
|  `aws_default_lambda_role`  |  Yes  | 
|  `aws_default_s3_role`  |  Yes  | 
|  `binlog_checksum`  |  Yes  | 
|  `binlog_format`  |  Yes  | 
|  `binlog_row_image`  |  No  | 
|  `binlog_rows_query_log_events`  |  No  | 
|  `character-set-client-handshake`  |  Yes  | 
|  `character_set_client`  |  Yes  | 
|  `character_set_connection`  |  Yes  | 
|  `character_set_database`  |  Yes  | 
|  `character_set_filesystem`  |  Yes  | 
|  `character_set_results`  |  Yes  | 
|  `collation_connection`  |  Yes  | 
|  `collation_server`  |  Yes  | 
|  `completion_type`  |  Yes  | 
|  `default_storage_engine`  |  No  | 
|  `innodb_autoinc_lock_mode`  |  Yes  | 
|  `innodb_checksum_algorithm`  |  No  | 
|  `innodb_checksums`  |  No  | 
|  `innodb_cmp_per_index_enabled`  |  Yes  | 
|  `innodb_commit_concurrency`  |  Yes  | 
|  `innodb_data_home_dir`  |  No  | 
|  `innodb_doublewrite`  |  No  | 
|  `innodb_file_per_table`  |  Yes  | 
|  `innodb_flush_log_at_trx_commit`  |  Yes  | 
|  `innodb_ft_max_token_size`  |  Yes  | 
|  `innodb_ft_min_token_size`  |  Yes  | 
|  `innodb_ft_num_word_optimize`  |  Yes  | 
|  `innodb_ft_sort_pll_degree`  |  Yes  | 
|  `innodb_online_alter_log_max_size`  |  Yes  | 
|  `innodb_optimize_fulltext_only`  |  Yes  | 
|  `innodb_page_size`  |  No  | 
|  `innodb_purge_batch_size`  |  Yes  | 
|  `innodb_purge_threads`  |  Yes  | 
|  `innodb_rollback_on_timeout`  |  Yes  | 
|  `innodb_rollback_segments`  |  Yes  | 
|  `innodb_spin_wait_delay`  |  Yes  | 
|  `innodb_strict_mode`  |  Yes  | 
|  `innodb_support_xa`  |  Yes  | 
|  `innodb_sync_array_size`  |  Yes  | 
|  `innodb_sync_spin_loops`  |  Yes  | 
|  `innodb_table_locks`  |  Yes  | 
|  `innodb_undo_directory`  |  No  | 
|  `innodb_undo_logs`  |  Yes  | 
|  `innodb_undo_tablespaces`  |  No  | 
|  `lc_time_names`  |  Yes  | 
|  `lower_case_table_names`  |  Yes  | 
|  `master-info-repository`  |  Yes  | 
|  `master_verify_checksum`  |  Yes  | 
|  `server_audit_events`  |  Yes  | 
|  `server_audit_excl_users`  |  Yes  | 
|  `server_audit_incl_users`  |  Yes  | 
|  `server_audit_logging`  |  Yes  | 
|  `server_id`  |  No  | 
|  `skip-character-set-client-handshake`  |  Yes  | 
|  `skip_name_resolve`  |  No  | 
|  `sync_frm`  |  Yes  | 
|  `time_zone`  |  Yes  | 

### Instance\-level Parameters<a name="AuroraMySQL.Reference.Parameters.Instance"></a>

The following table shows all of the parameters that apply to a specific DB instance in an Aurora MySQL DB cluster\. 


| Parameter name | Modifiable | 
| --- | --- | 
| `allow-suspicious-udfs` | No | 
| `aurora_lab_mode` | Yes | 
| `autocommit` | Yes | 
| `automatic_sp_privileges` | Yes | 
| `back_log` | Yes | 
| `basedir` | No | 
| `binlog_cache_size` | Yes | 
| `binlog_max_flush_queue_time` | Yes | 
| `binlog_order_commits` | Yes | 
| `binlog_stmt_cache_size` | Yes | 
| `bulk_insert_buffer_size` | Yes | 
| `concurrent_insert` | Yes | 
| `connect_timeout` | Yes | 
| `core-file` | No | 
| `datadir` | No | 
| `default_time_zone` | No | 
| `default_tmp_storage_engine` | Yes | 
| `default_week_format` | Yes | 
| `delay_key_write` | Yes | 
| `delayed_insert_limit` | Yes | 
| `delayed_insert_timeout` | Yes | 
| `delayed_queue_size` | Yes | 
| `div_precision_increment` | Yes | 
| `end_markers_in_json` | Yes | 
| `enforce_gtid_consistency` | No | 
| `eq_range_index_dive_limit` | Yes | 
| `event_scheduler` | Yes | 
| `explicit_defaults_for_timestamp` | Yes | 
| `flush` | No | 
| `flush_time` | Yes | 
| `ft_boolean_syntax` | No | 
| `ft_max_word_len` | Yes | 
| `ft_min_word_len` | Yes | 
| `ft_query_expansion_limit` | Yes | 
| `ft_stopword_file` | Yes | 
| `general_log` | Yes | 
| `general_log_file` | No | 
| `group_concat_max_len` | Yes | 
| `gtid-mode` | No | 
| `host_cache_size` | Yes | 
| `init_connect` | Yes | 
| `innodb_adaptive_flushing` | Yes | 
| `innodb_adaptive_hash_index` | Yes | 
| `innodb_adaptive_max_sleep_delay` | Yes | 
| `innodb_autoextend_increment` | Yes | 
| `innodb_buffer_pool_dump_at_shutdown` | No | 
| `innodb_buffer_pool_dump_now` | No | 
| `innodb_buffer_pool_filename` | No | 
| `innodb_buffer_pool_load_abort` | No | 
| `innodb_buffer_pool_load_at_startup` | No | 
| `innodb_buffer_pool_load_now` | No | 
| `innodb_buffer_pool_size` | Yes | 
| `innodb_change_buffer_max_size` | No | 
| `innodb_compression_failure_threshold_pct` | Yes | 
| `innodb_compression_level` | Yes | 
| `innodb_compression_pad_pct_max` | Yes | 
| `innodb_concurrency_tickets` | Yes | 
| `innodb_file_format` | Yes | 
| `innodb_flush_log_at_timeout` | No | 
| `innodb_flush_method` | Yes | 
| `innodb_flush_neighbors` | No | 
| `innodb_flushing_avg_loops` | No | 
| `innodb_force_load_corrupted` | No | 
| `innodb_ft_aux_table` | Yes | 
| `innodb_ft_cache_size` | Yes | 
| `innodb_ft_enable_stopword` | Yes | 
| `innodb_ft_server_stopword_table` | Yes | 
| `innodb_ft_user_stopword_table` | Yes | 
| `innodb_io_capacity` | No | 
| `innodb_io_capacity_max` | No | 
| `innodb_large_prefix` | Yes | 
| `innodb_lock_wait_timeout` | Yes | 
| `innodb_log_compressed_pages` | No | 
| `innodb_lru_scan_depth` | Yes | 
| `innodb_max_dirty_pages_pct` | Yes | 
| `innodb_max_purge_lag` | Yes | 
| `innodb_max_purge_lag_delay` | Yes | 
| `innodb_monitor_disable` | Yes | 
| `innodb_monitor_enable` | Yes | 
| `innodb_monitor_reset` | Yes | 
| `innodb_monitor_reset_all` | Yes | 
| `innodb_old_blocks_pct` | Yes | 
| `innodb_old_blocks_time` | Yes | 
| `innodb_open_files` | Yes | 
| `innodb_print_all_deadlocks` | Yes | 
| `innodb_random_read_ahead` | Yes | 
| `innodb_read_ahead_threshold` | Yes | 
| `innodb_read_io_threads` | No | 
| `innodb_read_only` | No | 
| `innodb_replication_delay` | Yes | 
| `innodb_sort_buffer_size` | Yes | 
| `innodb_stats_auto_recalc` | Yes | 
| `innodb_stats_method` | Yes | 
| `innodb_stats_on_metadata` | Yes | 
| `innodb_stats_persistent` | Yes | 
| `innodb_stats_persistent_sample_pages` | Yes | 
| `innodb_stats_transient_sample_pages` | Yes | 
| `innodb_thread_concurrency` | No | 
| `innodb_thread_sleep_delay` | Yes | 
| `innodb_use_native_aio` | No | 
| `innodb_write_io_threads` | No | 
| `interactive_timeout` | Yes | 
| `join_buffer_size` | Yes | 
| `keep_files_on_create` | Yes | 
| `key_buffer_size` | Yes | 
| `key_cache_age_threshold` | Yes | 
| `key_cache_block_size` | Yes | 
| `key_cache_division_limit` | Yes | 
| `local_infile` | Yes | 
| `lock_wait_timeout` | Yes | 
| `log-bin` | No | 
| `log_bin_trust_function_creators` | Yes | 
| `log_bin_use_v1_row_events` | Yes | 
| `log_error` | No | 
| `log_output` | Yes | 
| `log_queries_not_using_indexes` | Yes | 
| `log_slave_updates` | No | 
| `log_throttle_queries_not_using_indexes` | Yes | 
| `log_warnings` | Yes | 
| `long_query_time` | Yes | 
| `low_priority_updates` | Yes | 
| `max_allowed_packet` | Yes | 
| `max_binlog_cache_size` | Yes | 
| `max_binlog_size` | No | 
| `max_binlog_stmt_cache_size` | Yes | 
| `max_connect_errors` | Yes | 
| `max_connections` | Yes | 
| `max_delayed_threads` | Yes | 
| `max_error_count` | Yes | 
| `max_heap_table_size` | Yes | 
| `max_insert_delayed_threads` | Yes | 
| `max_join_size` | Yes | 
| `max_length_for_sort_data` | Yes | 
| `max_prepared_stmt_count` | Yes | 
| `max_seeks_for_key` | Yes | 
| `max_sort_length` | Yes | 
| `max_sp_recursion_depth` | Yes | 
| `max_tmp_tables` | Yes | 
| `max_user_connections` | Yes | 
| `max_write_lock_count` | Yes | 
| `metadata_locks_cache_size` | Yes | 
| `min_examined_row_limit` | Yes | 
| `myisam_data_pointer_size` | Yes | 
| `myisam_max_sort_file_size` | Yes | 
| `myisam_mmap_size` | Yes | 
| `myisam_sort_buffer_size` | Yes | 
| `myisam_stats_method` | Yes | 
| `myisam_use_mmap` | Yes | 
| `net_buffer_length` | Yes | 
| `net_read_timeout` | Yes | 
| `net_retry_count` | Yes | 
| `net_write_timeout` | Yes | 
| `old-style-user-limits` | Yes | 
| `old_passwords` | Yes | 
| `optimizer_prune_level` | Yes | 
| `optimizer_search_depth` | Yes | 
| `optimizer_switch` | Yes | 
| `optimizer_trace` | Yes | 
| `optimizer_trace_features` | Yes | 
| `optimizer_trace_limit` | Yes | 
| `optimizer_trace_max_mem_size` | Yes | 
| `optimizer_trace_offset` | Yes | 
| `performance_schema` | Yes | 
| `pid_file` | No | 
| `plugin_dir` | No | 
| `port` | No | 
| `preload_buffer_size` | Yes | 
| `profiling_history_size` | Yes | 
| `query_alloc_block_size` | Yes | 
| `query_cache_limit` | Yes | 
| `query_cache_min_res_unit` | Yes | 
| `query_cache_size` | Yes | 
| `query_cache_type` | Yes | 
| `query_cache_wlock_invalidate` | Yes | 
| `query_prealloc_size` | Yes | 
| `range_alloc_block_size` | Yes | 
| `read_buffer_size` | Yes | 
| `read_only` | No | 
| `read_rnd_buffer_size` | Yes | 
| `relay-log` | No | 
| `relay_log_info_repository` | Yes | 
| `relay_log_recovery` | No | 
| `safe-user-create` | Yes | 
| `secure_auth` | Yes | 
| `secure_file_priv` | No | 
| `skip-slave-start` | No | 
| `skip_external_locking` | No | 
| `skip_show_database` | Yes | 
| `slave_checkpoint_group` | Yes | 
| `slave_checkpoint_period` | Yes | 
| `slave_parallel_workers` | Yes | 
| `slave_pending_jobs_size_max` | Yes | 
| `slave_sql_verify_checksum` | Yes | 
| `slow_launch_time` | Yes | 
| `slow_query_log` | Yes | 
| `slow_query_log_file` | No | 
| `socket` | No | 
| `sort_buffer_size` | Yes | 
| `sql_mode` | Yes | 
| `sql_select_limit` | Yes | 
| `stored_program_cache` | Yes | 
| `sync_binlog` | No | 
| `sync_master_info` | Yes | 
| `sync_relay_log` | Yes | 
| `sync_relay_log_info` | Yes | 
| `sysdate-is-now` | Yes | 
| `table_cache_element_entry_ttl` | No | 
| `table_definition_cache` | Yes | 
| `table_open_cache` | Yes | 
| `table_open_cache_instances` | Yes | 
| `temp-pool` | Yes | 
| `thread_cache_size` | Yes | 
| `thread_handling` | No | 
| `thread_stack` | Yes | 
| `timed_mutexes` | Yes | 
| `tmp_table_size` | Yes | 
| `tmpdir` | No | 
| `transaction_alloc_block_size` | Yes | 
| `transaction_prealloc_size` | Yes | 
| `tx_isolation` | Yes | 
| `updatable_views_with_limit` | Yes | 
| `validate-password` | No | 
| `validate_password_dictionary_file` | No | 
| `validate_password_length` | No | 
| `validate_password_mixed_case_count` | No | 
| `validate_password_number_count` | No | 
| `validate_password_policy` | No | 
| `validate_password_special_char_count` | No | 
| `wait_timeout` | Yes | 

## Related Topics<a name="AuroraMySQL.Reference.RelatedTopics"></a>
+ [Amazon Aurora on Amazon RDS](CHAP_Aurora.md)