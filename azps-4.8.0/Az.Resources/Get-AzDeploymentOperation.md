---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 6a6d4022988c9164412f498ac2b92effd31e6a47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165682"
---
# Get-AzDeploymentOperation

## Synopsis
Abrufen des Bereitstellungsvorgangs

## Syntax

### GetByDeploymentName (Standard)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.
Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.
Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.

Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzDeployment** übermitteln.
Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.
Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzDeployment und Debuggen von Arm-Vorlagen Bereitstellungen

## Beispiele

### Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Ruft den Bereitstellungsvorgang mit dem Namen "Test" im aktuellen Abonnement Bereich ab.

### Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Mit diesem Befehl wird die Bereitstellung "Test" im aktuellen Abonnement Bereich abgerufen und die Bereitstellungsvorgänge abgerufen.

## Parameter

### -ApiVersion
Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.
Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.

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

### -Deploymentname
Der Bereitstellungsname.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Vorgangs-Nr
Die ID des Bereitstellungsvorgangs.

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
