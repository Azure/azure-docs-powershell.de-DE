---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846780"
---
# Get-AzManagementGroupDeploymentOperation

## Synopsis
Abrufen des Bereitstellungsvorgangs für die Verwaltungsgruppen Bereitstellung

## Syntax

### GetByDeploymentName (Standard)
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzManagementGroupDeploymentOperation** " listet alle Vorgänge auf, die Teil der Bereitstellung einer Verwaltungsgruppe waren, um Ihnen zu helfen, Informationen zu den genauen Vorgängen zu finden, die für eine bestimmte Bereitstellung fehlschlugen.
Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.

## Beispiele

### Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" in der Verwaltungsgruppe "myMG" ab.

### Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

Dieser Befehl ruft die Bereitstellung "Deploy01" in der Verwaltungsgruppe "myMG" ab und erhält dessen Bereitstellungsvorgänge.

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

### -Deploymentname
Der Bereitstellungsname.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Deploymentobject
Das Bereitstellungsobjekt.

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ManagementGroupId
Die Verwaltungsgruppen-ID.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vorgangs-Nr
Die ID des Bereitstellungsvorgangs.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
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

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## Ausgaben

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## Notizen

## Verwandte Links
