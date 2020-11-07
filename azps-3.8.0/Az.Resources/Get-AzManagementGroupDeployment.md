---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6a18c886ddddc30c82746ebe76d83d9477399755
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846783"
---
# Get-AzManagementGroupDeployment

## Synopsis
Abrufen der Bereitstellung in einer Mangement-Gruppe

## Syntax

### GetByDeploymentName (Standard)
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzManagementGroupDeployment** " Ruft die Bereitstellungen in der a-Verwaltungsgruppe ab.
Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.
Standardmäßig ruft **Get-AzManagementGroupDeployment** alle Bereitstellungen in der Verwaltungsgruppe ab.

## Beispiele

### Beispiel 1: Abrufen aller Bereitstellungen in einer Verwaltungsgruppe
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

Dieser Befehl ruft alle Bereitstellungen in der Verwaltungsgruppe "myMG" ab.

### Beispiel 2: Abrufen einer Bereitstellung nach Name
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

Dieser Befehl ruft die "Deploy01"-Bereitstellung in der Verwaltungsgruppe "myMG" ab.
Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzManagementGroupDeployment** erstellen.
Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.

### Beispiel 3: Abrufen einer Bereitstellung nach ID
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

Dieser Befehl ruft die "Deploy01"-Bereitstellung in der Verwaltungsgruppe "myMG" ab.

## Parameter

### -ApiVersion
Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.
Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Die vollqualifizierte Ressourcen-ID der Bereitstellung.
Beispiel:/Providers/Microsoft.Management/managementGroups/{managementGroupId}/Providers/Microsoft.Resources/Deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
Die Verwaltungsgruppen-ID.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Bereitstellung.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## Notizen

## Verwandte Links
