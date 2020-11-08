---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006410"
---
# New-AzureStorageAccount

## Synopsis
Erstellt ein neues Speicherkonto in einem Azure-Abonnement.

## Syntax

### ParameterSetAffinityGroup (Standard)
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### ParameterSetLocation
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageAccount** erstellt ein Konto, das Zugriff auf Azure Storage Services bietet.
Ein Speicherkonto ist eine weltweit einmalige Ressource im Speichersystem.
Das Konto ist der übergeordnete Namespace für die BLOB-, Warteschlangen-und Tabellen Dienste.

## Beispiele

### Beispiel 1: Erstellen eines speicherkontos für eine angegebene affinitätsgruppe
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

Mit diesem Befehl wird ein Speicherkonto für eine angegebene affinitätsgruppe erstellt.

### Beispiel 2: Erstellen eines speicherkontos an einem angegebenen Speicherort
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

Mit diesem Befehl wird ein Speicherkonto an einem angegebenen Speicherort erstellt.

## Parameter

### -Affinitygroup
Gibt den Namen einer vorhandenen affinitätsgruppe im aktuellen Abonnement an.
Sie können entweder den Parameter *Location* oder *affinitygroup* angeben, aber nicht beide.

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Beschreibung
Gibt eine Beschreibung für das Speicherkonto an.
Die Beschreibung kann bis zu 1024 Zeichen lang sein.

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
Gibt eine Bezeichnung für das Speicherkonto an.
Die Beschriftung kann bis zu 100 Zeichen lang sein.

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

### -Standort
Gibt den Speicherort des Azure-Datencenters an, in dem das Speicherkonto erstellt wird.
Sie können entweder den Parameter *Location* oder *affinitygroup* , aber nicht beides einbeziehen.

```yaml
Type: String
Parameter Sets: ParameterSetLocation
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

### -StorageAccountName
Gibt einen Namen für das Speicherkonto an.
Der Name des speicherkontos muss für Azure eindeutig sein und muss zwischen 3 und 24 Zeichen lang sein und nur Kleinbuchstaben und Zahlen verwenden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Typ
Gibt den Typ des speicherkontos an.
Gültige Werte sind:

- Standard_LRS
- Standard_ZRS
- Standard_GRS
- Standard_RAGRS
- Premium_LRS

Wenn dieser Parameter nicht angegeben wird, lautet der Standardwert Standard_GRS.

Standard_ZRS oder Premium_LRS Konten können nicht in andere Kontotypen geändert werden und umgekehrt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Satz-AzureStorageAccount](./Set-AzureStorageAccount.md)


