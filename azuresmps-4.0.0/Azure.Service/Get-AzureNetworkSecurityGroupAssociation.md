---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006788"
---
# Get-AzureNetworkSecurityGroupAssociation

## Synopsis
Ruft eine Netzwerksicherheitsgruppe für einen virtuellen Computer, einen Netzwerkadapter oder eine PaaS-Rolle ab.

## Syntax

### GetNetworkSecurityGroupAssociationForSubnet
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetNetworkSecurityGroupAssociationForIaaSRole
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetNetworkSecurityGroupAssociationForPaaSRole
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureNetworkSecurityGroupAssociation** " Ruft die Netzwerksicherheitsgruppe für einen virtuellen Computer, einen Netzwerkadapter oder eine Plattform als Dienst Rolle (PaaS) ab.

## Beispiele

### Beispiel 1: Abrufen der Netzwerksicherheitsgruppe für einen virtuellen Computer
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft die dem virtuellen Computer zugeordnete Netzwerksicherheitsgruppe ab.

## Parameter

### -Detailliert
Gibt an, dass dieses Cmdlet Details der Netzwerksicherheitsgruppe zurückgibt, die dem virtuellen Computer zugeordnet ist.
Diese Details umfassen Standort und Regeln.

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

### -NetworkInterfaceName
Gibt den Namen des Netzwerkadapters an, für den dieses Cmdlet die Netzwerksicherheitsgruppe abruft.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Gibt den Namen einer PaaS-Rolle an, für die dieses Cmdlet die Netzwerksicherheitsgruppe abruft.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen eines Cloud-Diensts an.
Die PaaS-Rolle gehört zu dem Dienst, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt einen PaaS-Steckplatz an.
Die PaaS-Rolle, für die dieses Cmdlet die Netzwerksicherheitsgruppe erhält, hat den Slot, den dieser Parameter angibt.
Gültige Werte sind: 

- Produktions
- Inszenierung 

Der Standardwert ist Production.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Gibt den Namen eines Subnets an, für das dieses Cmdlet die Netzwerksicherheitsgruppe abruft.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, für das dieses Cmdlet die Netzwerksicherheitsgruppe abruft.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt den virtuellen Computer an, auf den dieses Cmdlet die Netzwerksicherheitsgruppe anwendet.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. Servicemanagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup

## Notizen

## Verwandte Links

[Remove-AzureNetworkSecurityGroupAssociation](./Remove-AzureNetworkSecurityGroupAssociation.md)

[Satz-AzureNetworkSecurityGroupAssociation](./Set-AzureNetworkSecurityGroupAssociation.md)


