# TB-9707F proprietary blobs

Blob list for the Lenovo Legion Y700 (TB-9707F, SM8250-AC / kona), kept in the
vendor tree so that `extract-files.py` and the generated blob makefiles live
next to the blobs they describe.

## Stock images used

| Property | Value |
| --- | --- |
| Device | Lenovo TB-9707F (`TB-9707F_PRC`), model `Lenovo TB-9707F` |
| Fingerprint | `Lenovo/TB-9707F_PRC/TB-9707F:13/TKQ1.221013.002/15.0.342_231018:user/release-keys` |
| Build ID | `TKQ1.221013.002` |
| Incremental | `15.0.342_231018` (`ro.product`/`ro.system_ext`: `TB-9707F_CN_OPEN_USER_Q00024.0_T_ZUI_15.0.342_ST_231018`) |
| Build date | `Wed Oct 18 08:43:25 CST 2023` (vendor/odm: `09:17:46 CST 2023`) |
| ZUI version | `15.0` (`ro.vendor.com.zui.version`) |
| system_ext / product | Android 13, SDK 33 |
| vendor / odm | Android 11, SDK 30, `ro.product.first_api_level=30` (VNDK 30) |
| vendor security patch | `2023-06-01` |

Extracted partitions: `vendor`, `odm`, `system_ext`, `product`. The `system`
partition is not part of the extracted stock trees, so every `system/...` base
entry is reported as missing below.

## Counts

| Group | Count |
| --- | --- |
| Base entries kept from `device/xiaomi/sm8250-common` | 585 |
| Base entries missing from the stock images | 74 |
| TB-9707F delta entries | 412 |
| Total blobs required by `proprietary-files.txt` | 997 |

### Delta groups

| Section | Entries |
| --- | --- |
| Lenovo hardware HAL | 39 |
| Vibrator (Qualcomm + AAC RichTap) | 18 |
| Haptic firmware (Awinic AW8697 / RichTap RTP) | 268 |
| Audio (Cirrus Logic CS35L45 speaker protection) | 18 |
| Display and touch panel (Novatek NT36523) | 5 |
| WLAN (QCA6390) | 2 |
| Dolby (DAX3 / DMS / Dolby C2) | 18 |
| Camera (ArcSoft Pandora algorithms) | 44 |
| **Total** | **412** |

## Missing base entries

The paths below are listed in the Xiaomi sm8250-common blob list but do not
exist anywhere in the extracted stock trees. They are preserved in
`proprietary-files.txt` as single-line `# missing: <path>` comments so the
filter step stays auditable.

```
vendor/lib/rfsa/adsp/capi_v2_aptX_CLHDAD_Speech_Decoder.so
system/media/audio/ui/popup_cangmen_down.ogg
system/media/audio/ui/popup_cangmen_up.ogg
system/media/audio/ui/popup_chilun_down.ogg
system/media/audio/ui/popup_chilun_up.ogg
system/media/audio/ui/popup_jijia_down.ogg
system/media/audio/ui/popup_jijia_up.ogg
system/media/audio/ui/popup_mofa_down.ogg
system/media/audio/ui/popup_mofa_up.ogg
system/media/audio/ui/popup_muqin_down.ogg
system/media/audio/ui/popup_muqin_up.ogg
system/media/audio/ui/popup_yingyan_down.ogg
system/media/audio/ui/popup_yingyan_up.ogg
vendor/lib64/libcdsprpc_system.so
vendor/lib64/vendor.qti.hardware.data.iwlan@1.0.so
vendor/lib64/libgame_enhance.so
system/framework/tcmclient.jar
vendor/bin/loc_launcher
vendor/bin/xtra-daemon
vendor/bin/xtwifi-client
vendor/lib64/libgdtap.so
vendor/lib64/libizat_client_api.so
vendor/lib64/liblbs_core.so
vendor/etc/izat.conf
system_ext/lib64/vendor.qti.ImsRtpService-V1-ndk.so
system_ext/priv-app/ims/ims.apk
vendor/etc/init/android.hardware.keymaster@4.0-service-qti.rc
vendor/bin/nv_mac
system_ext/app/PowerOffAlarm/PowerOffAlarm.apk
system/etc/permissions/privapp-permissions-qti.xml
system/etc/sysconfig/qti_whitelist.xml
system_ext/app/QtiTelephonyService/QtiTelephonyService.apk
system_ext/etc/permissions/qcrilhook.xml
system_ext/framework/qcrilhook.jar
system_ext/priv-app/qcrilmsgtunnel/qcrilmsgtunnel.apk
vendor/bin/ATFWD-daemon
vendor/bin/hw/qcrild
vendor/etc/init/qcrild.rc
vendor/etc/seccomp_policy/atfwd@2.0.policy
vendor/lib64/deviceInfoServiceModule.so
vendor/lib64/libhydra_common.so
vendor/lib64/libmodemapi.so
vendor/lib64/libqcrilFramework.so
vendor/lib64/libril-qc-hal-qmi.so
vendor/lib64/libril-qc-logger.so
vendor/lib64/libril-qc-ltedirectdisc.so
vendor/lib64/libril-qc-radioconfig.so
vendor/lib64/librilqmiservices.so
vendor/lib64/libsettings.so
vendor/lib64/qcrild_librilutils.so
vendor/lib64/qtibus.so
vendor/lib64/qtimutex.so
vendor/radio/qcril_database/qcril.db
vendor/radio/qcril_database/upgrade/0_initial.sql
vendor/radio/qcril_database/upgrade/10_version_update_ecc_table.sql
vendor/radio/qcril_database/upgrade/1_version_intro.sql
vendor/radio/qcril_database/upgrade/2_version_add_wps_config.sql
vendor/radio/qcril_database/upgrade/3_version_update_wps_config.sql
vendor/radio/qcril_database/upgrade/4_version_update_ecc_table.sql
vendor/radio/qcril_database/upgrade/5_version_update_ecc_table.sql
vendor/radio/qcril_database/upgrade/6_version_update_ecc_table.sql
vendor/radio/qcril_database/upgrade/7_version_update_ecc_table.sql
vendor/radio/qcril_database/upgrade/8_version_update_ecc_table.sql
vendor/radio/qcril_database/upgrade/9_version_update_ecc_table.sql
vendor/bin/hw/vendor.qti.secure_element@1.2-service
vendor/etc/init/vendor.qti.secure_element@1.2-service.rc
vendor/lib64/android.hardware.secure_element@1.0-impl.so
vendor/lib64/jcos_nq_client.so
vendor/lib64/ls_nq_client.so
vendor/lib64/se_nq_extn_client.so
vendor/bin/mi_thermald
vendor/etc/init/init.mi_thermald.rc
system/framework/WfdCommon.jar
system_ext/lib64/vendor.qti.hardware.wifidisplaysession_aidl-V2-ndk.so
```
