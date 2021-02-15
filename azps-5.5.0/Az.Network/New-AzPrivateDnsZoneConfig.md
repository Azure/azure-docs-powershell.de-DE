---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151641"
---
# New-AzPrivateDnsZoneConfig

## SYNOPSIS
Erstellt die KONFIGURATION der DNS-Zone der Gruppe der privaten DNS-Zone.

## SYNTAX

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Mit **dem Cmdlet "New-AzPrivateDnsZoneConfig"** können Sie ein neues Konfigurationsobjekt für die DNS-Zone erstellen, das für die Gruppe "DNS-Zone" festgelegt wird.

## BEISPIELE

### Erstellt eine Konfiguration der DNS-Zone.
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

Im vorstehenden Beispiel wird die DNS-Zone und dann die Konfiguration der DNS-Zone erstellt. `New-AzPrivateDnsZone` Das Cmdlet az.privateDns zeigt sich als Beweis.

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

### -Name
Der Name der Ressource, die innerhalb einer Ressourcengruppe eindeutig ist.
Dieser Name kann für den Zugriff auf die Ressource verwendet werden.

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

### -PrivateDnsZoneId
Die Ressourcen-ID der privaten DNS-Zone.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
