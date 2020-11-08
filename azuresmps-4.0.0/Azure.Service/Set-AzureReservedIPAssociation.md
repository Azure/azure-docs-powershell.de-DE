---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006031"
---
# Set-AzureReservedIPAssociation

## Synopsis
Ordnet eine reservierte IP-Adresse einem vorhandenen virtuellen Computer oder einem cloudbasierten Dienst zu.

## Syntax

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureReservedIPAssociation** " ordnet eine reservierte IP-Adresse der virtuellen IP-Adresse (VIP) eines ausgeführten virtuellen Computers oder Cloud-Diensts zu.
Die reservierte IP-Adresse darf zum Zeitpunkt des Aufrufs dieses Cmdlets nicht verwendet werden und muss sich in der gleichen Region wie der virtuelle Computer oder der Cloud-Dienst befinden.

Der Vorgang dauert etwa 30 Sekunden, nachdem auf den virtuellen Computer oder Dienst über die reservierte IP-Adresse zugegriffen werden kann.

## Beispiele

### Beispiel 1: Einrichten einer reservierten IP-Zuordnung
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

Dieser Befehl weist die reservierte IP-Adresse mit dem Namen ResIp14 dem Dienst PipTestWestEurope zu.
ResIp14 ist eine reservierte IP-Adresse in der Region West Europa.

## Parameter

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

### -ReservedIPName
Gibt den Namen der reservierten IP-Adresse an, die einem virtuellen Computer oder Dienst zugeordnet werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen des Diensts an, der über die Bereitstellung verfügt, mit der die reservierte IP-Adresse verknüpft werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt den Bereitstellungs Steckplatz an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Inszenierung
- Produktions

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualIPName
Gibt den Namen einer vorhandenen VIP-Datei an, die mit einer reservierten IP verknüpft werden soll.
Weitere Informationen finden Sie unter Add-AzureVirtualIP zum Hinzufügen von VIPs zu Ihrem clouddienst.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext

## Notizen

## Verwandte Links

[Remove-AzureReservedIPAssociation](./Remove-AzureReservedIPAssociation.md)


