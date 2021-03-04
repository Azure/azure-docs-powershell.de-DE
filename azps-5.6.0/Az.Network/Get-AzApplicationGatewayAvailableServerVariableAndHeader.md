---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931808"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
Holen Sie sich die unterstützten Servervariablen sowie verfügbare Anforderungs- und Antwortheader.

## SYNTAX

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzApplicationGatewayAvailableServerVariableAndHeader-Cmdlet** ruft die unterstützten Servervariablen sowie verfügbare Anforderungs- und Antwortheader ab. Parameter können verwendet werden, um die Variablen- oder Kopfzeilenlisten zu erhalten.

## BEISPIELE

### Beispiel 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

Diese Befehle geben alle verfügbaren Servervariablen zurück.

### Beispiel 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

Diese Befehle geben alle verfügbaren Anforderungsüberschriften zurück.

### Beispiel 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Diese Befehle geben alle verfügbaren Antwortkopfzeilen zurück.

### Beispiel 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

Diese Befehle geben alle verfügbaren Servervariablen, Anforderungs- und Antwortheader zurück.

### Beispiel 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

Diese Befehle geben alle verfügbaren Servervariablen, Anforderungs- und Antwortheader zurück.

## PARAMETER

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

### -RequestHeader
Verfügbare Anforderungsheader für das Anwendungsgateway.

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

### -ResponseHeader
Verfügbare Antwortheader für das Anwendungsgateway.

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

### -ServerVariable
Verfügbare Servervariablen für das Anwendungsgateway.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## NOTIZEN
**List-AzApplicationGatewayAvailableServerVariableAndHeader** ist ein Alias für das **Get-AzApplicationGatewayAvailableServerVariableAndHeader-Cmdlet.**

## VERWANDTE LINKS
