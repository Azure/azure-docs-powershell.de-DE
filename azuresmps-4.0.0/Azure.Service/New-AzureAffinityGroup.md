---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006433"
---
# New-AzureAffinityGroup

## Synopsis
Erstellt eine affinitätsgruppe im aktuellen Abonnement.

## Syntax

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureAffinityGroup** erstellt eine Azure-affinitätsgruppe im aktuellen Azure-Abonnement.

Eine affinitätsgruppe fügt ihre Dienste und ihre Ressourcen in einem Azure Datacenter zusammen.
Die affinitätsgruppe gruppiert Mitglieder zusammen, um eine optimale Leistung zu erzielen.
Definieren von Affinitätsgruppen auf Abonnementebene
Ihre Affinitätsgruppen sind für alle nachfolgenden Cloud-Dienste oder Speicherkonten verfügbar, die Sie erstellen.
Sie können einer affinitätsgruppe nur dann Dienste hinzufügen, wenn Sie Sie erstellen.

## Beispiele

### Beispiel 1: Erstellen einer affinitätsgruppe
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

Mit diesem Befehl wird eine affinitätsgruppe namens South01 in der Region Süd-Zentralamerika erstellt.
Der Befehl gibt eine Bezeichnung und eine Beschreibung an.

## Parameter

### -Beschreibung
Gibt eine Beschreibung für die affinitätsgruppe an.
Die Beschreibung kann bis zu 1024 Zeichen lang sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -Label
Gibt eine Bezeichnung für die affinitätsgruppe an.
Die Beschriftung kann bis zu 100 Zeichen lang sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den geografischen Standort des Azure Datacenter an, in dem dieses Cmdlet die affinitätsgruppe erstellt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die affinitätsgruppe an.
Der Name muss für das Abonnement eindeutig sein.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureAffinityGroup](./Get-AzureAffinityGroup.md)

[Remove-AzureAffinityGroup](./Remove-AzureAffinityGroup.md)

[Satz-AzureAffinityGroup](./Set-AzureAffinityGroup.md)


