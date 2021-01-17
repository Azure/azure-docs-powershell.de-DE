---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303312"
---
# Set-AzStorageContainerAcl

## SYNOPSIS
Legt die Berechtigung für den öffentlichen Zugriff auf einen Speichercontainer fest.

## SYNTAX

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzStorageContainerAcl"** legt die Berechtigung für den öffentlichen Zugriff auf den angegebenen Speichercontainer in Azure fest.

## BEISPIELE

### Beispiel 1: Festlegen des Azure -Speichercontainer-ACL nach Name
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

Mit diesem Befehl wird ein Container erstellt, der keinen öffentlichen Zugriff hat.

### Beispiel 2: Festlegen des Azure -Speichercontainer-ACL mithilfe der Pipeline
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

Dieser Befehl ruft alle Speichercontainer ab, deren Name mit dem Container beginnt, und übergibt dann das Ergebnis an die Pipeline, um die Berechtigung für alle Container für den BLOB-Zugriff zu festlegen.

## PARAMETERS

### -ClientTimeoutPerRequest
Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.
Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.
Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Gibt die maximalen gleichzeitigen Netzwerkanrufe an.
Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.
Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.
Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.
Der Standardwert ist 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Gibt den Azure -Speicherkontext an.
Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Containernamen an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig generiert dieses Cmdlet keine Ausgabe.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Permission
Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.
Standardmäßig kann nur der Besitzer des Speicherkontos auf den Container und alle darin gespeicherten BLOBS zugreifen.
Wenn Sie anonymen Benutzern Leseberechtigungen für einen Container und dessen Blobs erteilen möchten, können Sie die Containerberechtigungen zum Aktivieren des öffentlichen Zugriffs festlegen.
Anonyme Benutzer können Blobs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.
Die zulässigen Werte für diesen Parameter sind: --Container.
Bietet vollständigen Lesezugriff auf einen Container und dessen Blobs.
Clients können Blobs im Container über anonyme Anforderung aufzählen, jedoch keine Container im Speicherkonto aufzählen. --Blob.
Bietet Lesezugriff auf BLOB-Daten in einem Container über eine anonyme Anforderung, bietet aber keinen Zugriff auf Containerdaten.
Clients können blobs im Container nicht mithilfe einer anonymen Anforderung aufzählen. --Off.
Beschränkt den Zugriff auf den Besitzer des Speicherkontos.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.
Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.
Serverseitiges Zeit out für jede Anforderung.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[New-AzStorageContainer](./New-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)


