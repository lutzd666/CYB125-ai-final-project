# Windows Configuration Snapshot Collector

## CYB125 AI Final Project

**Student name:** David Lutz
**Date:** May 7, 2026

---

## About this Project

The function of this script is to gather, format, and snapshot important data from the current Windows system configuration. The snapshot is then output as a JSON file by the script to be used and stored for later usage. This script is intended to be used by those who want to quickly gather the important configuration information from their Windows system to check if they meet a specific criteria to ensure security. It's used to be able to easily gather a Windows configuration from a device in a format where it can easily be compared to another system in the same format.



---

## Approach

The three sources of data that will be collected to obtain the important information necessary for the Windows configuration summary is the Windows Registry, Performance counters, and Various Command-line utilities. Using the winreg Python module, the entire Windows Registry can be accessed and used within the script to format the information we need about the systems OS and applications that run on it. By using the typeperf command, we can sample the Performance counters from the Windows system to gather the details on how the system is performing under these configurations. There will also be use of Command-line utilities like subprocesses.run, subprocesses.popen, stdout, and more to access the Windows device through the script and format the information gathered into the program properly.



---

## Data Dictionary

# Windows Configuration Snapshot Collector

## CYB125 AI Final Project

**Student name:** David Lutz
**Date:** May 7, 2026

---

## About this Project

The function of this script is to gather, format, and snapshot important data from the current Windows system configuration. The snapshot is then output as a JSON file by the script to be used and stored for later usage. This script is intended to be used by those who want to quickly gather the important configuration information from their Windows system to check if they meet a specific criteria to ensure security. It's used to be able to easily gather a Windows configuration from a device in a format where it can easily be compared to another system in the same format.



---

## Approach

The three sources of data that will be collected to obtain the important information necessary for the Windows configuration summary is the Windows Registry, Performance counters, and Various Command-line utilities. Using the winreg Python module, the entire Windows Registry can be accessed and used within the script to format the information we need about the systems OS and applications that run on it. By using the typeperf command, we can sample the Performance counters from the Windows system to gather the details on how the system is performing under these configurations. There will also be use of Command-line utilities like subprocesses.run, subprocesses.popen, stdout, and more to access the Windows device through the script and format the information gathered into the program properly.



---

## Data Dictionary

{
  "snapshot_metadata": {
    "schema_version": ,
    "timestamp_utc": ,
    "hostname": ,
    "generated_by_user": ,
    "elevated": ,
    "script_version": ,
    "python_version": ,
    "collection_duration_seconds": ,
    "collection_warnings": []
  },
  "system_identity": {
    "computer_name": ,
    "os_name": ,
    "os_build": ,
    "os_edition": ,
    "registered_owner": ,
    "registered_organization": ,
    "product_id": ,
    "os_version": ,
    "install_date_utc": ,
    "last_boot_utc": ,
    "uptime_seconds": ,
    "time_zone": ,
    "domain_or_workgroup": ,
    "is_domain_joined": 
  },
  "hardware_profile": {
    "cpu": {
      "name": ,
      "manufacturer": ,
      "max_clock_mhz": ,
      "architecture": ,
      "logical_processors": ,
      "physical_cores": 
    },
    "memory": {
      "total_physical_bytes":
    },
    "bios": {
      "manufacturer": ,
      "version": ,
      "release_date": 
    },
    "system": {
      "manufacturer": ,
      "model": 
    },
    "logical_disks": [
      {
        "drive_letter": ,
        "filesystem": ,
        "total_size_bytes": ,
        "free_space_bytes": 
      },
      {
        "drive_letter": ,
        "filesystem": ,
        "total_size_bytes": ,
        "free_space_bytes": 
      }
    ]
  },
  "network_configuration": {
    "primary_dns_suffix": ,
    "adapters": [
      {
        "name": ,
        "description": ,
        "mac_address": ,
        "dhcp_enabled": ,
        "ipv4_addresses": [
        ],
        "ipv4_subnet_mask": ,
        "default_gateway": ,
        "dns_servers": [
          
        ]
      }
    ]
  },
  "listening_ports": [
    {
      "protocol": ,
      "local_address": ,
      "local_port": ,
      "state": ,
      "owning_pid": ,
      "owning_process_name": 
    }
  ],
  "local_user_accounts": {
    "current_user": ,
    "users": [
      {
        "username": ,
        "full_name": ,
        "sid": ,
        "disabled": ,
        "password_required": ,
        "password_changeable": ,
        "password_expires": ,
        "last_logon_utc": 
      }
    ],
    "administrators_group_members": [
    ]
  },
  "password_policy": {
    "minimum_password_length": ,
    "minimum_password_age_days": ,
    "maximum_password_age_days": ,
    "password_history_length": ,
    "lockout_threshold": ,
    "lockout_duration_minutes": ,
    "lockout_observation_window_minutes": ,
    "force_logoff_after_minutes": 
  },
  "auto_start_services": [
    {
      "name": ,
      "display_name": ,
      "state": ,
      "start_type": ,
      "executable_path": ,
      "log_on_as": 
    }
  ],
  "running_processes": [
    {
      "pid": ,
      "parent_pid": ,
      "name": ,
      "executable_path": ,
      "command_line": 
    }
  ],
  "installed_software": [
    {
      "display_name": ,
      "display_version": ,
      "publisher": ,
      "install_date": ,
      "registry_hive": ,
      "is_64_bit": 
    }
  ],
  "installed_hotfixes": [
    {
      "hotfix_id": ,
      "description": ,
      "installed_on": ,
      "installed_by": 
    }
  ],
  "persistence_locations": {
    "hklm_run": [
      {
        "name": ,
        "value": 
      },
      {
        "name": ,
        "value": 
      }
    ],
    "hkcu_run": [
      {
        "name": ,
        "value": 
      }
    ],
    "hklm_run_once": [],
    "hkcu_run_once": [
      {
        "name": ,
        "value": 
      }
    ],
    "all_users_startup_folder": {
      "path": ,
      "files": [
        "desktop.ini"
      ]
    },
    "current_user_startup_folder": {
      "path": ,
      "files": [
        
      ]
    }
  },
  "scheduled_tasks": [
    {
      "task_name": ,
      "status": ,
      "next_run_time": ",
      "last_run_time": ,
      "last_result": ,
      "author": ,
      "task_to_run": 
    }
  ],
  "security_posture": {
    "firewall": {
      "domain_profile": {
        "state": ,
        "default_inbound_action": ,
        "default_outbound_action": ,
        "logging_dropped_connections": 
      },
      "private_profile": {
        "state": ,
        "default_inbound_action": ,
        "default_outbound_action": ,
        "logging_dropped_connections": 
      },
      "public_profile": {
        "state": ,
        "default_inbound_action": ,
        "default_outbound_action": ,
        "logging_dropped_connections": 
      }
    },
    "windows_defender": {
      "antivirus_enabled": ,
      "real_time_protection_enabled": ,
      "antivirus_signature_age_days": ,
      "antivirus_signature_version": 
    },
    "uac": {
      "enabled": ,
      "consent_prompt_behavior_admin": ,
      "prompt_on_secure_desktop": 
    },
    "bitlocker": {
      "system_drive_protection_status": ,
      "encryption_method": ,
      "encryption_percentage": 
    }
  },
  "performance_snapshot": {
    "sample_timestamp_utc": ,
    "cpu_total_percent": ,
    "memory": {
      "available_bytes": 
    },
    "disk_system_volume": {
      "reads_per_sec": ,
      "writes_per_sec": 
    },
    "process_count": 
  },
  "network_shares": [
    {
      "share_name": ,
      "local_path": ,
      "description": ,
      "is_administrative":
    }
  ]
}



---

## Configuration Areas

- 1. snapshot_metadata
snapshot metadata captures the script data itself to ensure the baseline is up to date.

- 2. system_identity
system identity holds information on the device name, OS specs, and registration to ensure compared systems running the same.

- 3. hardware_profile
hardware profile collects the physical components of the device to ensure there are no compatibility issues.

- 4. network_configuration
network configuration collects network configs and can be important if you need dhcp enabled or connect to the same dns server.

- 5. listening_ports
listening ports are collected data on ports that are open, this can be important because of the risk some ports have when they are open.

- 6. local_user_accounts
local_user_accounts collects all users on the device, its important because unwanted users may be on the system.

- 7. password_policy
password policy collects the set rules that are created for the devices passwords, its important because weak passwords create vulnerabilities in the system.

- 8. auto_start_services
auto start services are important for recognizing unauthorized services running on startup.

- 9. running_processes
running processes is important for identifying services that are accessing parts of the system they shouldn't be.

- 10. installed_software
installed software is important for removing and restricting uneccessary software on the device.

- 11. install_hotfixes
install hotfixes are important for recording what hotfix was implemented last and by who.

- 12. persistence_locations
persistence locations are important for discovering anomolies within startup.

- 13. scheduled_tasks
scheduled tasks are important for ensuring reoccuring tasks are accomplished as scheduled.

- 14. security_posture
security posture is important for ensuring the upkeep of important security standards.

- 15. performance_snapshot
performance snapshots are necessary for monitoring and maintaining a steady performance within a system.

- 16. network_shares
network shares are important to document to ensure there are no unauthorized devices accessing another divices files.



---

## Strategy

I plan to use AI in a tutor sense where it can demonstrate and explain the steps given when I'm lost and don't understand the code being written. I intend to have it explain on each step I don't understand. For example, what does this statement do? How else can this be implemented? Can this be more efficient? I can verify the code by using my own knowledge, look at error codes/troubleshoot, and check the slides for reference. I intend to rely on AI for helping me refine my understanding for subprocesses and how to better and more efficiently implement them



---

The project is structured around eight milestones, each one designed to produce a working
JSON file with an additional section implemented. The milestone structure isn't just a grading
convenience, it's a deliberate AI-collaboration pattern.
When students use AI well, they treat it like a pair programmer: they bring it small, well-scoped
problems, ask it to explain things rather than just produce things, and verify its answers against
an authoritative source (the textbook, the official Python docs, or their own running code). The
output is code they understand and could rewrite from scratch.
The eight-milestone structure exists to force the second pattern. Each milestone is small
enough that you can hold the whole thing in your head. Each milestone has a specific Python
concept attached to it, so you know what you're supposed to be learning. Each milestone has a
suggested AI prompt that asks for explanation, not code.
Your goal is not to finish the project as fast as possible. Your goal is to finish the project
understanding what you built. Those are different goals. The milestone structure pushes you
toward the second one. 