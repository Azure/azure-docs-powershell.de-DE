---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004589"
---
# New-AzDeploymentManagerServiceTopology

## Synopsis
Erstellt eine Dienst Topologie.

## Syntax

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzDeploymentManagerServiceTopology** erstellt eine Dienst Topologie.

Sie können das zurückgegebene ServiceTopology-Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerServiceTopology-Cmdlets Änderungen an der Topologie vornehmen.
Das zurückgegebene Objekt 

Das zurückgegebene Objekt verfügt über ein Feld "resourcecode", auf das in einer Rollout Ressource verwiesen werden kann, um anzugeben, dass die in dieser Dienst Topologie deklarierten Dienste im Rollout bereitgestellt werden.

## Beispiele

### Beispiel 1
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

Mit diesem Cmdlet wird eine neue Dienst Topologie in der Ressourcengruppe ContosoResourceGroup mit dem Namen ContosoServiceTopology und in Location Central US erstellt. Die Artefakt-Quell-Resource-Funktion gibt an, dass die für die Dienst Einheits Definitionen in dieser Topologie erforderlichen Artefakte aus der angegebenen Artefakt-Quelle gelesen werden müssen.

### Beispiel 2
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

Mit diesem Cmdlet wird eine neue Dienst Topologie in der Ressourcengruppe ContosoResourceGroup mit dem Namen ContosoServiceTopology und in Location Central US erstellt. Das Fehlen eines Artefakt-Quellen Verweises gibt an, dass die für die Dienst Einheits Definitionen in dieser Topologie erforderlichen Artefakte als absolute SAS-URIs in der Diensteinheit bereitgestellt werden.

## Parameter

### -ArtifactSourceId
Der Bezeichner der Artefakt-Quelle, in der die Artefakte, aus denen sich die Topologie befindet, gespeichert werden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Standort
Der Speicherort der Topologie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Topologie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Eine Hashtabelle, die Ressourcenkategorien darstellt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource

## Notizen

## Verwandte Links
