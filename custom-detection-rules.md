## Custom Wazuh Detection Rules

This document contains the custom detection rules developed during the Wazuh SIEM Lab project. These rules demonstrate basic detection engineering techniques by identifying common attack patterns observed during testing.

Current Rules

- Multiple Failed Login Attempts (Brute Force)
- Suspicious PowerShell Process Execution


Append to:
/var/ossec/etc/rules/local_rules.xml


## Rule 1 – Multiple Failed Login Attempts

### Objective

Detect possible brute-force attacks by monitoring repeated authentication failures from the same account.

### Detection Logic

- Trigger after 5 failed logins
- Time window: 5 minutes
- Maps to MITRE ATT&CK T1110

### Rule

<group name="custom,authentication">

  <rule id="100100" level="10" frequency="5" timeframe="300">

    <if_matched_sid>5710</if_matched_sid>

    <same_field>srcuser</same_field>

    <description>
Possible Brute Force Attack - 5 failed logins within 5 minutes.
    </description>

    <mitre>
      <id>T1110</id>
    </mitre>

    <group>
authentication,bruteforce,
    </group>

  </rule>

</group>


## Rule 2 — Suspicious PowerShell Launching CMD

### Objective

Generate an alert whenever PowerShell launches cmd.exe.

### Detection Logic

- PowerShell launches cmd.exe
- Suspicious Process Creation

### Rule

<group name="custom,process">

<rule id="100101" level="12">

<if_group>sysmon_event1</if_group>

<field name="win.eventdata.parentImage">powershell.exe</field>

<field name="win.eventdata.image">cmd.exe</field>

<description>

PowerShell spawned cmd.exe.

Possible suspicious process chain.

</description>

<mitre>

<id>T1059</id>

</mitre>

<group>

process_creation,powershell,

</group>

</rule>

</group>


## Limitations

These rules were created for a virtual SOC lab and serve as proof-of-concept detections. Additional tuning may be required before deployment in production environments to reduce false positives and adapt to organization-specific baselines.
