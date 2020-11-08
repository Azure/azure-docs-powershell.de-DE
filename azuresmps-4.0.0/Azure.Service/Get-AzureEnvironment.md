---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006558"
---
# Get-AzureEnvironment

## Synopsis
Ruft Azure-Umgebungen ab

## Syntax

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureEnvironment** " Ruft die Azure-Umgebungen ab, die für Windows PowerShell verfügbar sind.

Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.
Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.
Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Das Cmdlet " **Get-AzureEnvironment** " ruft Umgebungen aus ihrer Abonnement Datendatei ab, nicht aus Azure.
Wenn die Abonnement Datendatei veraltet ist, führen Sie das Cmdlet **Add-AzureAccount** oder **Import-PublishSettingsFile** aus, um die Datei zu aktualisieren.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Abrufen aller Umgebungen
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Dieser Befehl ruft alle Umgebungen ab, die für Windows PowerShell verfügbar sind.

### Beispiel 2: Abrufen einer Umgebung anhand des Namens
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

In diesem Beispiel wird die AzureCloud-Umgebung abgerufen.

### Beispiel 3: Abrufen aller Eigenschaften aller Umgebungen
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Dieser Befehl ruft alle Eigenschaften aller Umgebungen ab.

Der Befehl verwendet das Cmdlet " **Get-AzureEnvironment** ", um alle Azure-Umgebungen für dieses Konto abzurufen.
Anschließend wird mit dem Cmdlet " **ForEach-Object** " ein Befehl " **Get-AzureEnvironment** " mit dem **Name** -Parameter für jede Umgebung ausgeführt.
Der Wert des **Name** -Parameters ist die **environmentname** -Eigenschaft jeder Umgebung.

Ohne Parameter ruft **Get-AzureEnvironment** nur ausgewählte Eigenschaften einer Umgebung ab.

## Parameter

### -Name
Ruft nur die angegebene Umgebung ab.
Geben Sie den Namen der Umgebung ein.
Bei dem Parameterwert wird die Groß-/Kleinschreibung beachtet.
Platzhalterzeichen sind nicht zulässig.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### System. Management. Automation. PSCustomObject
Standardmäßig gibt **Get-AzureEnvironment** ein benutzerdefiniertes Objekt zurück.

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment
Wenn Sie **Get-AzureEnvironment** mit dem Parameter **Name** ausführen, wird ein  **WindowsAzureEnvironment** -Objekt zurückgegeben.

## Notizen

## Verwandte Links

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Importieren-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Satz-AzureEnvironment](./Set-AzureEnvironment.md)


