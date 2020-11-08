---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005758"
---
# Get-AzureStorSimpleTask

## Synopsis
Ruft den Status einer Aufgabe auf einem StorSimple-Gerät ab.

## Syntax

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleTask** " Ruft den Status einer Aufgabe ab, die auf einem Azure StorSimple-Gerät asynchron ausgeführt wird.

Beim Verwalten eines StorSimple-Geräts können die meisten Aktionen zum Erstellen, lesen, aktualisieren und löschen asynchron ausgeführt werden.
Windows PowerShell gibt eine **Aufgaben** -Nr zurück.
Verwenden Sie die ID, um den aktuellen Status der Aufgabe abzurufen.

## Beispiele

### Beispiel 1: Abrufen des Status einer Aufgabe
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Dieser Befehl ruft den Status der Aufgabe ab, die die angegebene ID aufweist.
Die Ergebnisse zeigen, dass der Vorgang den Status abgeschlossen und das Ergebnis erfolgreich aufweist.

## Parameter

### -InstanceId
Gibt die ID der Aufgabe an, für die dieses Cmdlet den Status nachverfolgt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### JobStatusInfo
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, das die folgenden Felder enthält: 

- **Fehler**.
**ErrorDetails** , die **Code** und **Nachricht** enthält.
- **Task** -Nr.
**Zeichenfolge**.
Die ID der Aufgabe, für die der Status zurückgegeben wird.
- **TaskSteps**.
**IList \<TaskStep\>**.
Jedes **TaskStep** -Objekt enthält **Details** , **errorCode** , **Nachricht** , **Ergebnis** und **Status**.
- **Ergebnis** aus.
**TaskResult** , das das Gesamtergebnis der Aufgabe enthält.
Gültige Werte sind: fehlgeschlagen, erfolgreich, PartialSuccess, storniert und ungültig.
- **Status** aus.
**Taskstatus** , das den allgemeinen Ausführungsstatus der Aufgabe enthält.
Gültige Werte sind: InProgress, ungültig und abgeschlossen.
- **TaskResult**.
**TaskResult** , ein Wert, der auf Grundlage des **Ergebnisses** und des **Status** berechnet wird.
Gültige Werte sind: fehlgeschlagen, erfolgreich, InProgress, PartialSuccess, storniert und ungültig.

## Notizen

## Verwandte Links

