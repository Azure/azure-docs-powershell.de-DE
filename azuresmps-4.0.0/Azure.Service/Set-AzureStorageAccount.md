---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006056"
---
# Set-AzureStorageAccount

## Synopsis
Aktualisiert die Eigenschaften eines speicherkontos in einem Azure-Abonnement.

## Syntax

### AccountType (Standard)
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GeoReplicationEnabled
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureStorageAccount** " aktualisiert die Eigenschaften eines Azure Storage-Kontos im aktuellen Abonnement.
Eigenschaften, die festgesetzt werden können, sind: **Label** , **Description** , **Type** und **GeoReplicationEnabled**.

## Beispiele

### Beispiel 1: Aktualisieren der Bezeichnung für ein Speicherkonto
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

Mit diesem Befehl werden die Eigenschaften **Label** und **Description** für das Speicherkonto mit dem Namen ContosoStorage01 aktualisiert.

### Beispiel 2: Aktivieren der Geo-Replikation für ein Speicherkonto
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

Mit diesem Befehl wird die **GeoReplicationEnabled** -Eigenschaft auf $false für das Speicherkonto mit dem Namen ContosoStorage01 festgelegt.

### Beispiel 3: Deaktivieren der Geo-Replikation für ein Speicherkonto
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

Mit diesem Befehl wird die **GeoReplicationEnabled** -Eigenschaft auf $true für das Speicherkonto mit dem Namen ContosoStorage01 festgelegt.

## Parameter

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoReplicationEnabled
Gibt an, ob das Speicherkonto mit aktivierter Geo-Replikation erstellt wird.

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
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
Gibt eine Bezeichnung für das Speicherkonto an.
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
Gibt den Namen des speicherkontos an, das von diesem Cmdlet geändert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

Der Effekt der Angabe des *GeoReplicationEnabled* -Parameters entspricht dem angeben Standard_GRS im *Type* -Parameter.

Standard_ZRS oder Premium_LRS Konten können nicht in andere Kontotypen geändert werden und umgekehrt.

```yaml
Type: String
Parameter Sets: AccountType
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

[Neu – AzureStorageAccount](./New-AzureStorageAccount.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)


