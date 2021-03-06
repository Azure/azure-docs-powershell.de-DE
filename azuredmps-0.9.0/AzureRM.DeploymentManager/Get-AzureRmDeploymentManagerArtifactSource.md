---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661988"
---
# Get-AzureRmDeploymentManagerArtifactSource

## Synopsis
Ruft eine Artefakt-Quelle ab.

## Syntax

### Interaktiv (Standard)
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDeploymentManagerArtifactSource** " Ruft eine Artefakt-Quelle ab und gibt ein Objekt zurück, das diese Artefakt-Quelle darstellt.
Geben Sie die Artefakt-Quelle anhand des Namens und des Ressourcengruppen namens an. Alternativ können Sie das ArtifactSource-Objekt oder die resourcecode-Objekt bereitstellen.

Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerArtifactSource-Cmdlets Änderungen an der Artefakt-Quelle übernehmen.

## Beispiele

### Beispiel 1: Abrufen einer Artefakt-Quelle
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

Dieser Befehl ruft eine Artefakt-Quelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.

### Beispiel 2: Abrufen einer Artefakt-Quelle mit dem Ressourcenbezeichner
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

Dieser Befehl ruft eine Artefakt-Quelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.

### Beispiel 3: Abrufen einer Artefakt-Quelle mit einem von New-AzureRmDeploymentManagerArtifactSource zurückgegebenen Objekt
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

Dieser Befehl ruft eine Artefakt-Quelle ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.

## Parameter

### -ArtifactSource
Artefakt-Quellobjekt.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Artefakt-Quelle.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Der Ressourcenbezeichner.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource

## Notizen

## Verwandte Links

[Neu – AzureRmDeploymentManagerArtifactSource](./New-AzureRmDeploymentManagerArtifactSource.md)

[Remove-AzureRmDeploymentManagerArtifactSource](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[Satz-AzureRmDeploymentManagerArtifactSource](./Set-AzureRmDeploymentManagerArtifactSource.md)