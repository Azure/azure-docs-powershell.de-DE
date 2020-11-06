---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 65ba11bcbe26ce91ce4c9ff2f84dc0cff30e125c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477513"
---
# Get-AzureStorageShare

## Synopsis
Ruft eine Liste der Dateifreigaben ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### MatchingPrefix (Standard)
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Spezifische
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageShare** " Ruft eine Liste der Dateifreigaben für ein Speicherkonto ab.

## Beispiele

### Beispiel 1: Abrufen einer Dateifreigabe
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

Dieser Befehl ruft die Dateifreigabe mit dem Namen ContosoShare06 ab.

### Beispiel 2: Abrufen aller Dateifreigaben, die mit einer Zeichenfolge beginnen
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

Dieser Befehl ruft alle Dateifreigaben ab, deren Namen mit Contoso beginnen.

### Beispiel 3: Abrufen aller Dateifreigaben in einem angegebenen Kontext
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

Der erste Befehl verwendet das Cmdlet **New-AzureStorageContext** , um einen Kontext mithilfe des *lokalen* Parameters zu erstellen, und speichert dann dieses Kontextobjekt in der $Context Variablen.

Der zweite Befehl ruft die Dateifreigaben für das Kontextobjekt ab, das in $context gespeichert ist.

## Parameter

### -ClientTimeoutPerRequest
Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.
Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.
Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.
Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.
Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.
Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.
Der Standardwert ist 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Dateifreigabe an.
Dieses Cmdlet ruft die Dateifreigabe ab, die dieser Parameter angibt, oder Nothing, wenn Sie den Namen einer Dateifreigabe angeben, die nicht vorhanden ist.

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
Gibt das Präfix für Dateifreigaben an.
Dieses Cmdlet ruft Dateifreigaben ab, die dem Präfix entsprechen, das dieser Parameter angibt, oder keine Dateifreigaben, wenn keine Dateifreigaben dem angegebenen Präfix entsprechen.

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.

```yaml
Type: Int32
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

### IStorageContext

Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureStorageShare](./New-AzureStorageShare.md)

[Remove-AzureStorageShare](./Remove-AzureStorageShare.md)
