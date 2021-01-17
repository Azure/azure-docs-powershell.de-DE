---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459488"
---
# Get-AzDeploymentOperation

## SYNOPSIS
Bereitstellungsvorgang

## SYNTAX

### GetByDeploymentName (Standard)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzDeploymentOperation"** listet alle Vorgänge auf, die Teil einer Bereitstellung waren, um Sie bei der Identifizierung und Bereitstellung genauerer Informationen zu den genauen Vorgängen zu unterstützen, die bei einer bestimmten Bereitstellung fehlgeschlagen sind.
Sie kann auch die Antwort und den Anforderungsinhalt für jeden Bereitstellungsvorgang anzeigen.
Dies sind die gleichen Informationen, die in den Bereitstellungsdetails auf dem Portal bereitgestellt werden.

Um die Anforderung und den Antwortinhalt zu erhalten, aktivieren Sie die Einstellung beim Übermitteln einer Bereitstellung über **"New-AzDeployment".**
Es kann potenziell geheime Daten protokollieren und verfügbar machen, z. B. Kennwörter, die in den Ressourceneigenschafts- oder listKeys-Vorgängen verwendet werden, die beim Abrufen der **Bereitstellungsvorgänge** zurückgegeben werden.
Weitere Informationen zu dieser Einstellung und deren Aktivierung finden Sie unter New-AzDeployment und Debuggen ARM Vorlagenbereitstellungen.

## BEISPIELE

### Beispiel 1: Bereitstellungsvorgänge mit einem Bereitstellungsnamen erhalten
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Ruft den Bereitstellungsvorgang mit dem Namen "test" im aktuellen Abonnementbereich ab.

### Beispiel 2: Erhalten einer Bereitstellung und deren Bereitstellungsvorgänge
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Dieser Befehl ruft den Bereitstellungstest im aktuellen Abonnementbereich ab und ruft dessen Bereitstellungsvorgänge ab.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -DeploymentName
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

### -DeploymentObject
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

### -OperationId
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
Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEploymentOperation

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
