---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165428"
---
# Get-AzSynapseRoleDefinition

## Synopsis
Ruft eine Synapse-Analyse Rollendefinition ab.

## Syntax

### GetByWorkspaceNameAndIdParameterSet (Standard)
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByWorkspaceNameAndNameParameterSet
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByWorkspaceObjectAndIdParameterSet
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByWorkspaceObjectAndNameParameterSet
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSynapseRoleDefinition** " Ruft eine Azure Synapse-Analyse Rollen Definition ab.
Wenn Sie keinen Rollennamen oder keine Rollen-ID angeben, ruft dieses Cmdlet alle Rollendefinitionen ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

Dieser Befehl ruft alle Rollendefinitionen unter einem Arbeitsbereich ab.

### Beispiel 2
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

Dieser Befehl ruft die Rollendefinition unter Workspace ContosoWorkspace mit dem Namen ContosoRole.

### Beispiel 3
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

Dieser Befehl ruft alle Rollendefinitionen unter einem Arbeitsbereich durch Pipeline ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Die ID der Rolle, die dem Prinzipal zugewiesen ist.

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Rolle, die dem Prinzipal zugewiesen ist.

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Name des Synapse-Arbeitsbereichs

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workspaceobject
Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace

## Ausgaben

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseRole

## Notizen

## Verwandte Links
