---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005936"
---
# Add-AzureEnvironment

## Synopsis
Erstellt eine Azure-Umgebung.

## Syntax

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureEnvironment** erstellt eine neue benutzerdefinierte Azure-Konto Umgebung und speichert Sie in Ihrem Roaming-Benutzerprofil.
Das Cmdlet gibt ein Objekt zurück, das die neue Umgebung darstellt.
Nach Abschluss des Befehls können Sie die Umgebung in Windows PowerShell verwenden.

Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.
Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.
Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Nur der **Name** -Parameter dieses Cmdlets ist obligatorisch.
Wenn Sie einen Parameter nicht angeben, ist sein Wert NULL ($null), und der Dienst, der diesen Endpunkt verwendet, funktioniert möglicherweise nicht ordnungsgemäß.
Wenn Sie den Wert einer Umgebungseigenschaft hinzufügen oder ändern möchten, verwenden Sie das Cmdlet " **Satz-AzureEnvironment** ".

Hinweis: das Ändern Ihrer Umgebung kann dazu führen, dass Ihr Konto fehlschlägt.
In der Regel werden Umgebungen nur zum Testen oder zur Problembehandlung hinzugefügt.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Hinzufügen einer Azure-Umgebung
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

Mit diesem Befehl wird die ContosoEnv Azure-Umgebung erstellt.

## Parameter

### -ActiveDirectoryEndpoint
Gibt den Endpunkt für die Azure Active Directory-Authentifizierung in der neuen Umgebung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveDirectoryServiceEndpointResourceId
Gibt die Ressourcen-ID einer Verwaltungs-API an, deren Zugriff von Azure Active Directory verwaltet wird.

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

### -Mandant
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

### -AzureKeyVaultDnsSuffix
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

### -AzureKeyVaultServiceEndpointResourceId
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

### -EnableAdfsAuthentication
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
Gibt den Endpunkt für den Azure Resource Manager-Katalog an, in dem Ressourcengruppen-Katalogvorlagen gespeichert sind.
Weitere Informationen zu Azure-Ressourcengruppen und Katalogvorlagen finden Sie im Hilfethema zu Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl
Gibt die URL des Azure-Verwaltungsportals in der neuen Umgebung an.

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

### -Name
Gibt einen Namen für die Umgebung an.
Dieser Parameter ist erforderlich.
Verwenden Sie nicht die Namen der Standardumgebungen AzureCloud und AzureChinaCloud.

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

### -PublishSettingsFileUrl
Gibt die URL der Datei für die Veröffentlichungseinstellungen für Ihr Konto an.
Eine Azure Publish Settings-Datei ist eine XML-Datei, die Informationen zu Ihrem Konto und ein Verwaltungszertifikat enthält, mit dem Windows PowerShell sich in Ihrem Namen bei Ihrem Azure-Konto anmelden kann.

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

### -ResourceManagerEndpoint
Gibt den Endpunkt für Azure Resource Manager-Daten an, einschließlich Daten zu Ressourcengruppen, die dem Konto zugeordnet sind.
Weitere Informationen zum Azure Resource Manager finden Sie unter [Azure Resource Manager-Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) und [Verwenden von Windows PowerShell mit Ressourcen-Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Gibt die URL des Azure-Dienstendpunkts an.
Der Azure-Dienstendpunkt bestimmt, ob Ihre Anwendung von der globalen Azure-Plattform, Azure, die von 21Vianet in China betrieben wird, oder von einer privaten Azure-Installation verwaltet wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
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

### -StorageEndpoint
Gibt den Standardendpunkt von Speicherdiensten in der neuen Umgebung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment

## Notizen

## Verwandte Links

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Satz-AzureEnvironment](./Set-AzureEnvironment.md)


