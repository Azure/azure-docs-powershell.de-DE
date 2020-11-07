---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 1eafc934777809d7fd4041496b004ea682e97910
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843467"
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

### Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Ruft den Bereitstellungsvorgang mit dem Namen "Test" im aktuellen Abonnement Bereich ab.

### Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Mit diesem Befehl wird die Bereitstellung "Test" im aktuellen Abonnement Bereich abgerufen und die Bereitstellungsvorgänge abgerufen.

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
Aliases: AzContext, AzureCredential

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String
System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## Ausgaben

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## Notizen

## Verwandte Links
