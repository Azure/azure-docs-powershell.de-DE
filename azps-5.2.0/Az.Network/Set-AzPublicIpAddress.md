---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364005"
---
# Set-AzPublicIpAddress

## SYNOPSIS
Aktualisiert eine öffentliche IP-Adresse.

## SYNTAX

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzPublicIpAddress"** aktualisiert eine öffentliche IP-Adresse.

## BEISPIELE

### 1: Ändern der Zuweisungsmethode einer öffentlichen IP-Adresse
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe ab, $rgName.
Der zweite Befehl legt die Zuweisungsmethode des öffentlichen IP-Adressobjekts auf "Static" fest.
Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt und ändert die Zuordnungsmethode in "Statisch". Eine öffentliche IP-Adresse wird sofort zugewiesen.

### 2: Hinzufügen einer DNS-Domänenbezeichnung einer öffentlichen IP-Adresse
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe ab, $rgName.
Mit dem zweiten Befehl wird die Eigenschaft "DomainNameLabel" auf das erforderliche DNS-Präfix festgelegt.
Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt. DomainNameLabel & Fqdn werden wie erwartet geändert.
    
### 3: Ändern der Bezeichnung einer öffentlichen IP-Adresse für die DNS-Domäne
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe ab, $rgName.
Mit dem zweiten Befehl wird die Eigenschaft "DomainNameLabel" auf das erforderliche DNS-Präfix festgelegt.
Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt. DomainNameLabel & Fqdn werden wie erwartet geändert.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -PublicIpAddress
Gibt ein öffentliches IP-Adressobjekt an, das den Zustand darstellt, in dem die öffentliche IP-Adresse festgelegt werden soll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


