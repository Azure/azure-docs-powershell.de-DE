---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: c39b61ab51296231b0952d1f12bd18e6d3aa13d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504802"
---
# <span data-ttu-id="be5b1-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="be5b1-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="be5b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="be5b1-103">Legt Eigenschaften für eine Azure-Umgebung fest.</span><span class="sxs-lookup"><span data-stu-id="be5b1-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be5b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be5b1-104">SYNTAX</span></span>

### <span data-ttu-id="be5b1-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="be5b1-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be5b1-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be5b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be5b1-107">DESCRIPTION</span></span>
<span data-ttu-id="be5b1-108">Das Set-AzureRMEnvironment-Cmdlet legt Endpunkte und Metadaten für die Verbindung mit einer Instanz von Azure fest.</span><span class="sxs-lookup"><span data-stu-id="be5b1-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="be5b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be5b1-109">EXAMPLES</span></span>

### <span data-ttu-id="be5b1-110">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="be5b1-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="be5b1-111">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispiel Endpunkten mithilfe von Add-AzureRmEnvironment, und dann ändern wir den Wert der Attribute ActiveDirectoryEndpoint und GraphEndpoint der erstellten Umgebung mit dem Cmdlet-Cmdlet-Satz-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="be5b1-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="be5b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="be5b1-112">PARAMETERS</span></span>

### <span data-ttu-id="be5b1-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="be5b1-114">Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="be5b1-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="be5b1-116">Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="be5b1-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-117">-Mandant</span><span class="sxs-lookup"><span data-stu-id="be5b1-117">-AdTenant</span></span>
<span data-ttu-id="be5b1-118">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-118">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-119">-ARMEndpoint</span></span>
<span data-ttu-id="be5b1-120">Der Azure Resource Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="be5b1-120">The Azure Resource Manager endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="be5b1-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="be5b1-122">DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste</span><span class="sxs-lookup"><span data-stu-id="be5b1-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="be5b1-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="be5b1-124">DNS-Suffix des Azure Data Lake Store-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="be5b1-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="be5b1-125">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="be5b1-125">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="be5b1-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="be5b1-127">Gibt das Domänennamensuffix für Key Vault-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-127">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="be5b1-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="be5b1-129">Gibt die Zielgruppe für Zugriffstoken an, die Anforderungen für Key Vault-Dienste autorisieren.</span><span class="sxs-lookup"><span data-stu-id="be5b1-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="be5b1-130">-DataLakeAudience</span></span>
<span data-ttu-id="be5b1-131">Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="be5b1-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5b1-132">-DefaultProfile</span></span>
<span data-ttu-id="be5b1-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be5b1-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="be5b1-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="be5b1-135">Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="be5b1-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-136">-GalleryEndpoint</span></span>
<span data-ttu-id="be5b1-137">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="be5b1-138">-GraphAudience</span></span>
<span data-ttu-id="be5b1-139">Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="be5b1-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-140">-GraphEndpoint</span></span>
<span data-ttu-id="be5b1-141">Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="be5b1-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="be5b1-143">Gibt die URL für das Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-143">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-144">-Name</span><span class="sxs-lookup"><span data-stu-id="be5b1-144">-Name</span></span>
<span data-ttu-id="be5b1-145">Gibt den Namen der zu ändernden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-145">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="be5b1-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="be5b1-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="be5b1-147">Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="be5b1-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="be5b1-149">Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-149">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-150">-Scope</span><span class="sxs-lookup"><span data-stu-id="be5b1-150">-Scope</span></span>
<span data-ttu-id="be5b1-151">Bestimmt den Bereich von Kontextänderungen, beispielsweise wheher Änderungen gelten nur für den cusrrent-Prozess oder für alle von diesem Benutzer gestarteten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="be5b1-151">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-152">-ServiceEndpoint</span></span>
<span data-ttu-id="be5b1-153">Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="be5b1-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="be5b1-155">Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="be5b1-156">-StorageEndpoint</span></span>
<span data-ttu-id="be5b1-157">Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="be5b1-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="be5b1-159">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="be5b1-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be5b1-160">-Confirm</span></span>
<span data-ttu-id="be5b1-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be5b1-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be5b1-162">-WhatIf</span></span>
<span data-ttu-id="be5b1-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be5b1-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be5b1-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be5b1-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5b1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5b1-165">CommonParameters</span></span>
<span data-ttu-id="be5b1-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5b1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5b1-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5b1-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5b1-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be5b1-168">INPUTS</span></span>

## <span data-ttu-id="be5b1-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be5b1-169">OUTPUTS</span></span>

### <span data-ttu-id="be5b1-170">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="be5b1-170">PSAzureEnvironment</span></span>

## <span data-ttu-id="be5b1-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="be5b1-171">NOTES</span></span>

## <span data-ttu-id="be5b1-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be5b1-172">RELATED LINKS</span></span>

[<span data-ttu-id="be5b1-173">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="be5b1-173">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="be5b1-174">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="be5b1-174">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="be5b1-175">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="be5b1-175">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

