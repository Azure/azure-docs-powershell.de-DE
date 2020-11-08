---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006638"
---
# Set-AzureAclConfig

## Synopsis
Ändert ein ACL-Konfigurationsobjekt.

## Syntax

### AddRule
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### RemoveRule
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Setrule
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzureAclConfig** " ändert ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) aus einer vorhandenen Azure Virtual Machine-Konfiguration.

## Beispiele

### Beispiel 1: Hinzufügen einer Regel zu einer neuen ACL-Konfiguration
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

Der erste Befehl erstellt eine ACL-Konfiguration und speichert Sie dann in der $ACL-Variablen.

Mit dem zweiten Befehl wird der in $ACL gespeicherten Konfiguration eine neue Regel hinzugefügt.
Der Befehl gibt eine Aktion, ein Subnetz, eine Reihenfolge und eine Beschreibung für die Regel an.

### Beispiel 2: Ändern einer Regel in einer ACL-Konfiguration
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Cmdlet " **Get-AzureAclConfig** ".
Dieses Cmdlet ruft die ACL-Konfiguration für den Endpunkt mit dem Namen Web ab.
Der Befehl speichert das ACL-Konfigurationsobjekt in der $ACL-Variablen.

Der zweite Befehl ändert die Regel, die die ID 0 hat.
Der Befehl ändert die Reihenfolge und die Beschreibung der Regel.

Der endgültige Befehl legt das ACL-Konfigurationsobjekt für diesen virtuellen Computer mithilfe des Cmdlets " **Set-AzureEndpoint** " fest.
Der Befehl aktualisiert auch diesen virtuellen Computer.

### Beispiel 3: Entfernen einer Regel aus einer ACL-Konfiguration
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

Der erste Befehl speichert ein ACL-Konfigurationsobjekt in der $ACL-Variablen.
Dies entspricht dem vorherigen Beispiel.

Der zweite Befehl entfernt die Regel, die die ID 0 hat, aus der ACL-Konfiguration in $ACL.

Der endgültige Befehl legt das ACL-Konfigurationsobjekt für den virtuellen Computer fest und aktualisiert diesen virtuellen Computer.
Dies entspricht dem vorherigen Beispiel.

## Parameter

### -ACL
Gibt ein ACL-Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Aktion
Gibt die Aktion für die Regel an, die von diesem Cmdlet hinzugefügt oder geändert wird.
Gültige Werte sind: zulassen und verweigern.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRule
Gibt an, dass dieses Cmdlet der ACL-Konfiguration eine Regel hinzufügt.

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beschreibung
Gibt eine Beschreibung für die Regel an, die von diesem Cmdlet hinzugefügt oder geändert wird.

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestellung
Gibt die Verarbeitungsreihenfolge für die Regel an, die von diesem Cmdlet hinzugefügt oder geändert wird.

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteSubnet
Gibt das Remote-Subnetz für die Regel an, die dieses Cmdlet hinzufügt oder ändert.
Gibt eine Adresse im CIDR-Format (classlos InterDomain Routing) an.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRule
Gibt an, dass dieses Cmdlet eine Regel aus der ACL-Konfiguration entfernt.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lineal
Gibt die ID der Regel an, die dieses Cmdlet für die ACL-Konfiguration entfernt oder ändert.

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Setrule
Gibt an, dass mit diesem Cmdlet eine Regel in der ACL-Konfiguration geändert wird.

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[Get-AzureVM](./Get-AzureVM.md)

[Neu – AzureAclConfig](./New-AzureAclConfig.md)

[Remove-AzureAclConfig](./Remove-AzureAclConfig.md)

[Satz-AzureEndpoint](./Set-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


