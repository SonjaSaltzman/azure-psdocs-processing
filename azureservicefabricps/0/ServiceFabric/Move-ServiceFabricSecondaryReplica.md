---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: DBE2A1B4-438C-4E66-9D50-2DBC6333338C
online version:
schema: 2.0.0
updated_at: 05/03/2017 06:05 AM
ms.date: 05/03/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Move-ServiceFabricSecondaryReplica.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Move-ServiceFabricSecondaryReplica.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/40385fc07259a8f5f0d2cec04a231e9cd42fcff3
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
ms.service: service-fabric
---

# Move-ServiceFabricSecondaryReplica

## SYNOPSIS
Moves the Service Fabric secondary replica of a stateful service.

## SYNTAX

### PartitionId
```
Move-ServiceFabricSecondaryReplica [-CurrentSecondaryNodeName <String>] [-NewSecondaryNodeName <String>]
 [-IgnoreConstraints <Boolean>] -PartitionId <Guid> -ServiceName <Uri> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNameRandomPartition
```
Move-ServiceFabricSecondaryReplica [-CurrentSecondaryNodeName <String>] [-NewSecondaryNodeName <String>]
 [-IgnoreConstraints <Boolean>] -ServiceName <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingleton
```
Move-ServiceFabricSecondaryReplica [-CurrentSecondaryNodeName <String>] [-NewSecondaryNodeName <String>]
 [-IgnoreConstraints <Boolean>] -ServiceName <Uri> [-PartitionKindSingleton] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionNamed
```
Move-ServiceFabricSecondaryReplica [-CurrentSecondaryNodeName <String>] [-NewSecondaryNodeName <String>]
 [-IgnoreConstraints <Boolean>] -ServiceName <Uri> [-PartitionKindNamed] -PartitionKey <String>
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionUniformedInt
```
Move-ServiceFabricSecondaryReplica [-CurrentSecondaryNodeName <String>] [-NewSecondaryNodeName <String>]
 [-IgnoreConstraints <Boolean>] -ServiceName <Uri> [-PartitionKindUniformInt64] -PartitionKey <String>
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Move-ServiceFabricSecondaryReplica** cmdlet moves the Service Fabric stateful service active secondary replica from the current active secondary node to a specified node location.
You can also perform this operation on system services.
You cannot use this cmdlet for stateless services.

The **Move-ServiceFabricSecondaryReplica** cmdlet moves the secondary replica to a new Service Fabric node location after the command is accepted.
However, the load balancer may move the secondary replica again based on load balancer constraints or on the load balancer balancing algorithm.

To use this cmdlet, you must be a member of the Administrators group.

Before using this cmdlet, connect to the Service Fabric cluster.

## EXAMPLES

### Example 1: Move the secondary replica of a stateful service by node name
```
PS C:\> Move-ServiceFabricSecondaryReplica -CurrentSecondaryNodeName "N0020" -NewSecondaryNodeName "N0010" -PartitionId 93838f53-f1d9-4b99-8492-b802ee807d03 -ServiceName fabric:/SampleApp/SampleService
```

This command moves the specified secondary replica from node N0020 to node N0010 for the specified partition that belongs to the service named fabric:/SampleApp/SampleService.

### Example 2: Move a random secondary replica of a stateful service by service name to a new node
```
PS C:\> Move-ServiceFabricSecondaryReplica -ServiceName fabric:/myApp/MyPersistedService
```

This command moves a random secondary replica to a new node.
A random partition is selected for the specified service.

## PARAMETERS

### -CurrentSecondaryNodeName
Specifies the current node name for the secondary node.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreConstraints
Indicates whether the cmdlet ignores constraints.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NewSecondaryNodeName
Specifies the new node name for the secondary node.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionId
Specifies the ID of the partition for which the replica is moved.

```yaml
Type: Guid
Parameter Sets: PartitionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKey
Specifies the key of the partition for which the replica is moved.

```yaml
Type: String
Parameter Sets: ServiceNamePartitionNamed, ServiceNamePartitionUniformedInt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKindNamed
Indicates that this cmdlet moves a named partition service.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionNamed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKindSingleton
Indicates that this cmdlet moves a singleton partitioned service.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionSingleton
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKindUniformInt64
Indicates that this cmdlet moves a UniformInt64 partitioned service.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionUniformedInt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifies the service name of the replica to move.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeoutSec
Specifies the time-out period, in seconds, for the operation.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Guid
Represents the ID of a Service Fabric partition.

### System.Uri
Represents the name of a Service Fabric service.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Testability.MoveSecondaryResult** object that represents the operation result.

## NOTES

## RELATED LINKS

[Move-ServiceFabricPrimaryReplica](./Move-ServiceFabricPrimaryReplica.md)
