---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ef4f5128e92a319cb2b8ca021fc9b86f484d9b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662221"
---
# Add-AzureRmEnvironment

## Synopsis
Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Name (Standard)
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ARMEndpoint
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Add-AzureRmEnvironment-Cmdlet fügt Endpunkte und Metadaten hinzu, damit Azure Resource Manager-Cmdlets eine Verbindung mit einer neuen Instanz des Azure Resource Manager herstellen können.
Die integrierten Umgebungen AzureCloud und AzureChinaCloud Zielen auf vorhandene öffentliche Instanzen des Azure Resource Manager ab.

## Beispiele

### Beispiel 1: Erstellen und Ändern einer neuen Umgebung
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispiel Endpunkten mithilfe von Add-AzureRmEnvironment, und dann ändern wir den Wert der Attribute ActiveDirectoryEndpoint und GraphEndpoint der erstellten Umgebung mit dem Cmdlet-Cmdlet-Satz-AzureRmEnvironment.

## Parameter

### -ActiveDirectoryEndpoint
Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveDirectoryServiceEndpointResourceId
Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Mandant
Gibt den standardmäßigen Active Directory-Mandanten an.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ARMEndpoint
Der Azure Resource Manager-Endpunkt

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix
DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureDataLakeStoreFileSystemEndpointSuffix
DNS-Suffix des Azure Data Lake Store-Dateisystems.
Beispiel: azuredatalake.net

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureKeyVaultDnsSuffix
Gibt das Domänennamensuffix für Key Vault-Dienste an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureKeyVaultServiceEndpointResourceId
Gibt die Zielgruppe für Zugriffstoken an, die Anforderungen für Key Vault-Dienste autorisieren.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataLakeAudience
Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die credeetnails, Mandanten und Abonnements, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAdfsAuthentication
Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphAudience
Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl
Gibt die URL für das Verwaltungs Portal an.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Umgebung an, die hinzugefügt werden soll.

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

### -PublishSettingsFileUrl
Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceManagerEndpoint
Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceEndpoint
Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpoint
Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BatchEndpointResourceId
Der Ressourcenbezeichner des Azure-Batch Diensts, der der Empfänger des angeforderten Tokens ist

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureOperationalInsightsEndpoint
Gibt den Endpunkt für den Zugriff auf die Operation Insight-Abfrage an. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureOperationalInsightsEndpointResourceId
Gibt die Zielgruppe für Zugriffstoken an, die Anforderungen für Operational Insights-Dienste autorisieren.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### PSAzureEnvironment
Dieses Cmdlet gibt den Satz von Endpunkten und Metadaten zurück, die für die Kommunikation mit einer Instanz von Azure erforderlich sind.

## Notizen

## Verwandte Links

[Get-AzureRMEnvironment](./Get-AzureRMEnvironment.md)

[Remove-AzureRMEnvironment](./Remove-AzureRMEnvironment.md)

[Satz-AzureRMEnvironment](./Set-AzureRMEnvironment.md)

