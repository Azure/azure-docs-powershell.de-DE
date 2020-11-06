---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475638"
---
# New-AzureStorageContainer

## Synopsis
Erstellt einen Azure-Speichercontainer.

## Syntax

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageContainer** erstellt einen Azure-Speichercontainer.

## Beispiele

### Beispiel 1: Erstellen eines Azure-Speichercontainers
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

Mit diesem Befehl wird ein Speichercontainer erstellt.

### Beispiel 2: Erstellen mehrerer Azure-Speichercontainer
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

In diesem Beispiel werden mehrere Speichercontainer erstellt.
Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.

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
Gibt einen Kontext für den neuen Container an.

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
Gibt einen Namen für den neuen Container an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Berechtigung
Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.
Standardmäßig kann der Container und alle darin enthaltenen BLOBs nur vom Besitzer des speicherkontos aufgerufen werden.
Um anonymen Benutzern Leseberechtigungen für einen Container und dessen BLOBs zu erteilen, können Sie die Container Berechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.
Anonyme Benutzer können BLOBs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Container.
Bietet vollständigen Lesezugriff auf einen Container und seine BLOBs.
Clients können BLOBs im Container mithilfe einer anonymen Anforderung auflisten, aber keine Container im Speicherkonto auflisten. 
- BLOB.
Bietet Lesezugriff auf BLOB-Daten in einem Container durch anonyme Anforderung, bietet jedoch keinen Zugriff auf Containerdaten.
Clients können keine BLOBs im Container mithilfe einer anonymen Anforderung auflisten. 
- Aus.
Dadurch wird der Zugriff auf den Besitzer des speicherkontos eingeschränkt.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.
Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.

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

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)

[Satz-AzureStorageContainerAcl](./Set-AzureStorageContainerAcl.md)


