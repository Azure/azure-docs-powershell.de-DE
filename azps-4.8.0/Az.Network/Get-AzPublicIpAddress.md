---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 9df5cdd2a601977b453cb8242a9241cede3d4539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165248"
---
# Get-AzPublicIpAddress

## Synopsis
Ruft eine öffentliche IP-Adresse ab.

## Syntax

### NoExpandStandAloneIp (Standard)
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ExpandStandAloneIp
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NoExpandScaleSetIp
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExpandScaleSetIp
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzPublicIPAddress** " ruft mindestens eine öffentliche IP-Adresse in einer Ressourcengruppe ab.

## Beispiele

### Beispiel 1: Abrufen einer öffentlichen IP-Ressource
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

Dieser Befehl ruft eine öffentliche IP-Adressen Ressource mit dem Namen myPublicIp in der Ressourcengruppe myRg.

### Beispiel 2: Abrufen öffentlicher IP-Ressourcen mithilfe von Filtern
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

Dieser Befehl ruft alle öffentlichen IP-Adressen Ressourcen ab, deren Name mit myPublicIp beginnt.

## Parameter

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

### -ExpandResource
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpConfigurationName
IP-Konfigurations Name der Netzwerkschnittstelle.

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der öffentlichen IP-Adresse an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -NetworkInterfaceName
Name der Netzwerkschnittstelle der virtuellen Maschine

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -VirtualMachineIndex
Virtueller Computer-Index.

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetName
Name des Skalierungs Satzes für virtuelle Maschinen

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

## Notizen

## Verwandte Links

[Neu – AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Satz-AzPublicIpAddress](./Set-AzPublicIpAddress.md)


