---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006162"
---
# Set-AzureIPForwarding

## Synopsis
Aktiviert oder deaktiviert die IP-Weiterleitung.

## Syntax

### EnableIaaSIPForwardingParamSet
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### DisableIaaSIPForwardingParamSet
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnableSlotIPForwardingParamSet
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### DisableSlotIPForwardingParamSet
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureIPForwarding** " aktiviert oder deaktiviert die IP-Weiterleitung für einen virtuellen Computer, für eine Plattform als Dienst (PaaS)-Rolle oder einen Netzwerkadapter, der zu einer virtuellen Maschine oder PaaS-Rolle gehört.

## Beispiele

### Beispiel 1: Aktivieren der IP-Weiterleitung für einen virtuellen Computer
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.
Das aktuelle Cmdlet aktiviert die IP-Weiterleitung für diesen virtuellen Computer.

### Beispiel 2: Deaktivieren der IP-Weiterleitung für einen virtuellen Computer
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.
Das aktuelle Cmdlet deaktiviert die IP-Weiterleitung für diesen virtuellen Computer.

## Parameter

### -Deaktivieren Sie
Gibt an, dass dieses Cmdlet die IP-Weiterleitung deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Gibt an, dass dieses Cmdlet IP-Weiterleitung aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterfaceName
Gibt den Namen des Netzwerkadapters an, auf dem dieses Cmdlet IP-Weiterleitung festlegt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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
Gibt den Namen einer PaaS-Rolle an, auf der dieses Cmdlet IP-Weiterleitung festlegt.

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
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
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt einen PaaS-Steckplatz an.
Die PaaS-Rolle, für die dieses Cmdlet die Weiterleitung festlegt, hat den Slot, den dieser Parameter angibt.
Gültige Werte sind:

- Produktions
- Inszenierung

Der Standardwert ist Production.

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, auf dem dieses Cmdlet IP-Weiterleitung festlegt.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
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

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzureIPForwarding](./Get-AzureIPForwarding.md)
