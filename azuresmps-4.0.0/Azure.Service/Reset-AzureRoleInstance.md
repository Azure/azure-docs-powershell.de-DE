---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005686"
---
# Reset-AzureRoleInstance

## Synopsis
Fordert einen Neustart oder eine Neubildung einer einzelnen Rolleninstanz oder aller Rolleninstanzen einer bestimmten Rolle an.

## Syntax

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Reset-AzureRoleInstance** fordert einen Neustart oder ein reimage einer Rolleninstanz an, die in einer Bereitstellung ausgeführt wird.
Dieser Vorgang wird synchron ausgeführt.
Wenn Sie eine Rolleninstanz neu starten, nimmt Azure die Instanz offline, startet das zugrunde liegende Betriebssystem für diese Instanz neu und führt die Instanz wieder online.
Alle Daten, die auf die lokale Festplatte geschrieben werden, bleiben über einen Neustart erhalten.
Alle im Arbeitsspeicher befindlichen Daten gehen verloren.

Das umbilden einer Rolleninstanz führt je nach Art der Rolle zu einem anderen Verhalten.
Bei einer Web-oder Worker-Rolle übernimmt Azure die Rolle offline und schreibt eine Neuinstallation des Azure Guest-Betriebssystems auf den virtuellen Computer, wenn die Rolle neu erstellt wird.
Die Rolle wird dann wieder online geschaltet.
Bei einer VM-Rolle übernimmt Azure beim erneuten abbilden der Rolle die Rolle offline, wendet das von Ihnen bereitgestellte benutzerdefinierte Bild erneut an und bringt die Rolle wieder online.

Azure versucht, beim erneuten abbilden der Rolle Daten in allen lokalen Speicherressourcen zu verwalten. bei einem vorübergehenden Hardwarefehler kann die lokale Speicherressource jedoch verloren gehen.
Wenn für Ihre Anwendung die Beibehaltung von Daten erforderlich ist, empfiehlt es sich, in eine dauerhafte Datenquelle zu schreiben, beispielsweise ein Azure-Laufwerk.
Alle Daten, die in ein lokales Verzeichnis geschrieben werden, die nicht von der lokalen Speicherressource definiert sind, gehen beim erneuten abbilden der Rolle verloren.

## Beispiele

### Beispiel 1: Starten einer Rolleninstanz
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Mit diesem Befehl wird die Rolleninstanz mit dem Namen MyWebRole_IN_0 in der Staging-Bereitstellung des MySvc01-Diensts neu gestartet.

### Beispiel 2: umbilden einer Rolleninstanz
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Mit diesem Befehl werden die Rolleninstanzen in der Staging-Bereitstellung des MySvc01-Cloud-Diensts erneut abbildet.

### Beispiel 3: umbilden aller Rolleninstanzen
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Mit diesem Befehl werden alle Rolleninstanzen in der Produktionsbereitstellung des MySvc01-Diensts erneut abbildet.

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

### -InstanceName
Gibt den Namen der Rolleninstanz an, die neu abbilden oder neu gestartet werden soll.

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

### -Reboot
Gibt an, dass dieses Cmdlet die angegebene Rolleninstanz neu startet oder, falls keine angegeben ist, alle Rolleninstanzen.
Sie müssen entweder einen *Neustart* -oder einen *reimage* -Parameter angeben, aber nicht beide.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Reimage
Gibt an, dass dieses Cmdlet die angegebene Rolleninstanz oder, falls keine angegeben ist, alle Rolleninstanzen umbildet.
Sie müssen entweder einen *Neustart* -oder einen *reimage* -Parameter angeben, aber nicht beide.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen des Diensts an.

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

### -Slot
Gibt die Bereitstellungsumgebung an, in der die Rolleninstanzen ausgeführt werden.
Gültige Werte sind: Production und Staging.
Sie können entweder den Parameter *deploymentname* oder *Slot* angeben, aber nicht beide.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Satz-AzureRole](./Set-AzureRole.md)


