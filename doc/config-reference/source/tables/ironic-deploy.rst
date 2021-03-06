..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _ironic-deploy:

.. list-table:: Description of deploy configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[deploy]**
     -
   * - ``continue_if_disk_secure_erase_fails`` = ``False``
     - (Boolean) Defines what to do if an ATA secure erase operation fails during cleaning in the Ironic Python Agent. If False, the cleaning operation will fail and the node will be put in ``clean failed`` state. If True, shred will be invoked and cleaning will continue.
   * - ``default_boot_option`` = ``None``
     - (String) Default boot option to use when no boot option is requested in node's driver_info. Currently the default is "netboot", but it will be changed to "local" in the future. It is recommended to set an explicit value for this option.
   * - ``erase_devices_metadata_priority`` = ``None``
     - (Integer) Priority to run in-band clean step that erases metadata from devices, via the Ironic Python Agent ramdisk. If unset, will use the priority set in the ramdisk (defaults to 99 for the GenericHardwareManager). If set to 0, will not run during cleaning.
   * - ``erase_devices_priority`` = ``None``
     - (Integer) Priority to run in-band erase devices via the Ironic Python Agent ramdisk. If unset, will use the priority set in the ramdisk (defaults to 10 for the GenericHardwareManager). If set to 0, will not run during cleaning.
   * - ``http_root`` = ``/httpboot``
     - (String) ironic-conductor node's HTTP root path.
   * - ``http_url`` = ``None``
     - (String) ironic-conductor node's HTTP server URL. Example: http://192.1.2.3:8080
   * - ``power_off_after_deploy_failure`` = ``True``
     - (Boolean) Whether to power off a node after deploy failure. Defaults to True.
   * - ``shred_final_overwrite_with_zeros`` = ``True``
     - (Boolean) Whether to write zeros to a node's block devices after writing random data. This will write zeros to the device even when deploy.shred_random_overwrite_iterations is 0. This option is only used if a device could not be ATA Secure Erased. Defaults to True.
   * - ``shred_random_overwrite_iterations`` = ``1``
     - (Integer) During shred, overwrite all block devices N times with random data. This is only used if a device could not be ATA Secure Erased. Defaults to 1.
