# ApiMachineConfig

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AutoDestroy** | **bool** |  | [optional] [default to null]
**Checks** | [**map[string]ApiMachineCheck**](api.MachineCheck.md) |  | [optional] [default to null]
**DisableMachineAutostart** | **bool** | Deprecated: use Service.Autostart instead | [optional] [default to null]
**Dns** | [***ApiDnsConfig**](api.DNSConfig.md) |  | [optional] [default to null]
**Env** | **map[string]string** | Fields managed from fly.toml If you add anything here, ensure appconfig.Config.ToMachine() is updated | [optional] [default to null]
**Files** | [**[]ApiFile**](api.File.md) |  | [optional] [default to null]
**Guest** | [***ApiMachineGuest**](api.MachineGuest.md) |  | [optional] [default to null]
**HostDedicationId** | **string** |  | [optional] [default to null]
**Image** | **string** | Set by fly deploy or fly machines commands | [optional] [default to null]
**Init** | [***ApiMachineInit**](api.MachineInit.md) |  | [optional] [default to null]
**Metadata** | **map[string]string** |  | [optional] [default to null]
**Metrics** | [***ApiMachineMetrics**](api.MachineMetrics.md) |  | [optional] [default to null]
**Mounts** | [**[]ApiMachineMount**](api.MachineMount.md) |  | [optional] [default to null]
**Processes** | [**[]ApiMachineProcess**](api.MachineProcess.md) |  | [optional] [default to null]
**Restart** | [***ApiMachineRestart**](api.MachineRestart.md) |  | [optional] [default to null]
**Schedule** | **string** | The following fields can only be set or updated by &#x60;fly machines run|update&#x60; commands \&quot;fly deploy\&quot; must preserve them, if you add anything here, ensure it is propagated on deploys | [optional] [default to null]
**Services** | [**[]ApiMachineService**](api.MachineService.md) |  | [optional] [default to null]
**Size** | **string** | Deprecated: use Guest instead | [optional] [default to null]
**Standbys** | **[]string** | Standbys enable a machine to be a standby for another. In the event of a hardware failure, the standby machine will be started. | [optional] [default to null]
**Statics** | [**[]ApiStatic**](api.Static.md) |  | [optional] [default to null]
**StopConfig** | [***ApiStopConfig**](api.StopConfig.md) |  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

