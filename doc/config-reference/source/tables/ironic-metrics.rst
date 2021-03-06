..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _ironic-metrics:

.. list-table:: Description of metrics configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[metrics]**
     -
   * - ``agent_backend`` = ``noop``
     - (String) Backend for the agent ramdisk to use for metrics. Default possible backends are "noop" and "statsd".
   * - ``agent_global_prefix`` = ``None``
     - (String) Prefix all metric names sent by the agent ramdisk with this value. The format of metric names is [global_prefix.][uuid.][host_name.]prefix.metric_name.
   * - ``agent_prepend_host`` = ``False``
     - (Boolean) Prepend the hostname to all metric names sent by the agent ramdisk. The format of metric names is [global_prefix.][uuid.][host_name.]prefix.metric_name.
   * - ``agent_prepend_host_reverse`` = ``True``
     - (Boolean) Split the prepended host value by "." and reverse it for metrics sent by the agent ramdisk (to better match the reverse hierarchical form of domain names).
   * - ``agent_prepend_uuid`` = ``False``
     - (Boolean) Prepend the node's Ironic uuid to all metric names sent by the agent ramdisk. The format of metric names is [global_prefix.][uuid.][host_name.]prefix.metric_name.
   * - ``backend`` = ``noop``
     - (String) Backend to use for the metrics system.
   * - ``global_prefix`` = ``None``
     - (String) Prefix all metric names with this value. By default, there is no global prefix. The format of metric names is [global_prefix.][host_name.]prefix.metric_name.
   * - ``prepend_host`` = ``False``
     - (Boolean) Prepend the hostname to all metric names. The format of metric names is [global_prefix.][host_name.]prefix.metric_name.
   * - ``prepend_host_reverse`` = ``True``
     - (Boolean) Split the prepended host value by "." and reverse it (to better match the reverse hierarchical form of domain names).
