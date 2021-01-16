---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468244"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
Holen Sie sich die unterstützten Servervariablen sowie die verfügbaren Anforderungs- und Antwortheader.

## SYNTAX

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzApplicationGatewayAvailableServerVariableAndHeader"** ruft die unterstützten Servervariablen sowie die verfügbaren Anforderungs- und Antwortheader ab. Parameter können verwendet werden, um die Variablen oder Headerlisten zu erhalten.

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

Diese Befehle geben alle verfügbaren Anforderungsheader zurück.

### Beispiel 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Diese Befehle geben alle verfügbaren Antwortheader zurück.

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

### -RequestHeader
Verfügbare Anforderungsheader des Anwendungsgateways.

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
Verfügbare Antwortheader des Anwendungsgateways.

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
Verfügbare Servervariablen des Anwendungsgateways.

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

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## HINWEISE
**List-AzApplicationGatewayAvailableServerVariableAndHeader** ist ein Alias für das **Cmdlet "Get-AzApplicationGatewayAvailableServerVariableAndHeader".**

## LINKS ZU VERWANDTEN THEMEN
