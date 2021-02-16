---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163004"
---
# New-AzStorageAccount

## SYNOPSIS
Erstellt ein Speicherkonto.

## SYNTAX

### AzureActiveDirectoryDomainServicesForFile (Standard)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzStorageAccount"** erstellt ein Azure Storage-Konto.

## BEISPIELE

### Beispiel 1: Erstellen eines Speicherkontos
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen "MyResourceGroup" erstellt.

### Beispiel 2: Erstellen eines Blob Storage-Kontos mit BlobStorage Kind und hot AccessTier
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Mit diesem Befehl wird ein Blob Storage-Konto erstellt, das blobStorage Kind und hot AccessTier verwendet.

### Beispiel 3: Erstellen Sie ein Speicherkonto mit Kind StorageV2, und generieren und weisen Sie eine Identität für Azure KeyVault zu.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Mit diesem Befehl wird ein Speicherkonto mit Kind StorageV2 erstellt.  Außerdem wird eine Identität generiert und zugewiesen, die zum Verwalten von Kontoschlüsseln über Azure KeyVault verwendet werden kann.

### Beispiel 4: Erstellen eines Speicherkontos mit NetworkRuleSet aus JSON
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Mit diesem Befehl wird ein Speicherkonto erstellt, das über die Eigenschaft "NetworkRuleSet" von JSON verfügt.

### Beispiel 5: Erstellen eines Speicherkontos mit aktivierten hierarchischem Namespace
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Mit diesem Befehl wird ein Speicherkonto mit aktivierten hierarchischem Namespace erstellt.

### Beispiel 6: Erstellen Sie ein Speicherkonto mit Azure Files AAD DS Authentication, und aktivieren Sie die große Dateifreigabe.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Mit diesem Befehl wird ein Speicherkonto mit Azure Files AAD DS Authentication erstellt und große Dateifreigaben aktiviert.

### Beispiel 7: Erstellen eines Speicherkontos mit aktivierter Active Directory-Domänendienstauthentifizierung.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Mit diesem Befehl wird ein Speicherkonto erstellt, für das die Active Directory-Domänendienstauthentifizierung aktiviert werden kann.

### Beispiel 8: Erstellen eines Speicherkontos mit "Warteschlange" und "Tabellendienst" verwenden den Verschlüsselungsschlüssel mit Kontobereich und "Infrastrukturverschlüsselung erforderlich".
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

Dieser Befehl erstellt ein Speicherkonto mit Verschlüsselungsschlüssel mit Kontobereich und Tabellendienst und erfordert Infrastrukturverschlüsselung. Warteschlange und Tabelle verwenden also denselben Verschlüsselungsschlüssel mit blob- und file-Dienst, und der Dienst wenden eine sekundäre Verschlüsselungsebene mit plattformver verwalteten Schlüsseln für ruhede Daten an.
Holen Sie sich dann die Eigenschaften des Speicherkontos, zeigen Sie den Verschlüsselungsschlüsseltyp von Warteschlangen- und Tabellendienst sowie den Wert der Kryption "RequireInfrastructureEncryption" an.

### Beispiel 9: Erstellen des Kontos "MinimumTlsVersion" und "AllowBlobPublicAccess"
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

Der Befehl "Konto erstellen" mit "MinimumTlsVersion" und "AllowBlobPublicAccess" und zeigt dann die zwei Eigenschaften des erstellten Kontos an. 

### Beispiel 10: Erstellen eines Speicherkontos mit Einstellung "RoutingPreference"
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

Mit diesem Befehl wird ein Speicherkonto mit der Einstellung "RoutingPreference" erstellt: "PublishMicrosoftEndpoint" und "PublishInternetEndpoint" als "true" und "RoutingChoice" als "MicrosoftRouting".

## PARAMETERS

### -AccessTier
Gibt die Zugriffsebene des Speicherkontos an, das von diesem Cmdlet erstellt wird.
Die zulässigen Werte für diesen Parameter sind: "Hot" und "Cool".
Wenn Sie einen Wert von BlobStorage für den Parameter *"Kind"* angeben, müssen Sie einen Wert für den *Parameter "AccessTier"* angeben. Wenn Sie einen Wert von "Storage" für diesen *Parameter "Kind"* angeben, geben Sie nicht den *"AccessTier"-Parameter* an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryAzureStorageSid
Gibt die Sicherheits-ID (SID) für Azure Storage an. Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
Gibt die Domänen-GUID an. Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
Gibt die primäre Domäne an, für die der AD -DNS-Server autoritativ ist. Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
Gibt die Sicherheits-ID (SID) an. Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
Gibt die active Directory-Gesamtstruktur an, die sie erhalten soll. Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetDomäneName
Gibt den Domänennamen von NetERGEBNISS an. Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBlobPublicAccess
Lassen Sie den öffentlichen Zugriff auf alle BLOBS oder Container im Speicherkonto zu. Die Standarddeutung gilt für diese Eigenschaft.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -AssignIdentity
Generieren und zuweisen Sie eine neue Speicherkontoidentität für dieses Speicherkonto zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.

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

### -CustomDomainName
Gibt den Namen der benutzerdefinierten Domäne des Speicherkontos an.
Der Standardwert ist "Storage".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableActiveDirectoryDomainServicesForFile
Aktivieren Sie azure files Active Directory Domain Service Authentication für das Speicherkonto.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
Aktivieren Sie Azure Files Azure Active Directory Domain Service Authentication für das Speicherkonto.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
Gibt an, ob das Konto "Storage" den hierarchischen Namespace aktiviert.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Gibt an, ob das Speicherkonto nur den HTTPS-Datenverkehr aktiviert.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 TiB-Kapazität unterstützen kann. Sobald das Konto aktiviert ist, kann das Feature nicht mehr deaktiviert werden. Derzeit nur für LRS- und ZRS-Replikationstypen unterstützt, daher sind Kontokonvertierungen in georedundanter Konten nicht möglich. Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047

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

### -EncryptionKeyTypeForQueue
Legen Sie den Verschlüsselungsschlüsseltyp für die Warteschlange ein. Der Standardwert ist "Dienst".
-Konto: Die Warteschlange wird mit dem Verschlüsselungsschlüssel mit Kontobereich verschlüsselt. -Dienst: Die Warteschlange wird immer mit Service-Managed verschlüsselt. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
Legen Sie den Verschlüsselungsschlüsseltyp für "Table" ein. Der Standardwert ist "Dienst".
- Konto: Die Tabelle wird mit dem Verschlüsselungsschlüssel mit Kontobereich verschlüsselt. 
- Dienst: Die Tabelle wird immer mit Service-Managed verschlüsselt. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Gibt die Art des Speicherkontos an, das von diesem Cmdlet erstellt wird.
Die zulässigen Werte für diesen Parameter sind:
- Speicher. Allgemeines Speicherkonto, das die Speicherung von Blobs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.
- StorageV2. Allgemeine Version 2 (GPv2) Speicherkonto, das Blobs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Daten tiering unterstützt.
- BlobStorage. Blob Storage account which supports storage of Blobs only.
- BlockBlobStorage. Block Blob Storage account which supports storage of Block Blobs only.
- FileStorage. Dateispeicherkonto, das nur das Speichern von Dateien unterstützt.
Der Standardwert ist "StorageV2".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Gibt den Speicherort des zu erstellenden Speicherkontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
Die mindestens zulässige TLS-Version für Speicheranforderungen. Die Standarddeutung für diese Eigenschaft ist TLS 1.0.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Speicherkontos an, das erstellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
NetworkRuleSet dient zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften wie Dienste, die die Regeln umgehen dürfen, und zum Behandeln von Anforderungen, die keine der definierten Regeln erfüllen.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishInternetEndpoint
Gibt an, ob Internetroutingspeicherendpunkte veröffentlicht werden sollen

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishMicrosoftEndpoint
Gibt an, ob Microsoft-Routing-Speicherendpunkte veröffentlicht werden sollen.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Speicherkonto hinzugefügt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoutingChoice
Die Routingauswahl definiert die Art des vom Benutzer gewählten Netzwerkroutings. Mögliche Werte sind: "MicrosoftRouting", "InternetRouting".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
Gibt den Namen der SKU des Speicherkontos an, das von diesem Cmdlet erstellt wird.
Die zulässigen Werte für diesen Parameter sind:
- Standard_LRS. Lokal redundanter Speicher.
- Standard_ZRS. Zone-redundant storage.
- Standard_GRS. Georedundanter Speicher.
- Standard_RAGRS. Georedundanter Speicher mit Lesezugriff.
- Premium_LRS. Premium für lokal redundanten Speicher.
- Premium_ZRS. Premium zone-redundant storage.
- Standard_GZRS – Georedundanter zonenredundanter Speicher.
- Standard_RAGZRS – Georedundanter zonenredundanter Speicher mit Lesezugriff.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist. Beispiel: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Gibt an, ob die indirekte #A0 aktiviert werden soll.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

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

## AUSGABEN

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
