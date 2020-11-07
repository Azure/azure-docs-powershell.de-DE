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
# <span data-ttu-id="4995b-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="4995b-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="4995b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4995b-102">SYNOPSIS</span></span>
<span data-ttu-id="4995b-103">Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="4995b-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4995b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4995b-104">SYNTAX</span></span>

### <span data-ttu-id="4995b-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="4995b-105">Name (Default)</span></span>
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

### <span data-ttu-id="4995b-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4995b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4995b-107">DESCRIPTION</span></span>
<span data-ttu-id="4995b-108">Das Add-AzureRmEnvironment-Cmdlet fügt Endpunkte und Metadaten hinzu, damit Azure Resource Manager-Cmdlets eine Verbindung mit einer neuen Instanz des Azure Resource Manager herstellen können.</span><span class="sxs-lookup"><span data-stu-id="4995b-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="4995b-109">Die integrierten Umgebungen AzureCloud und AzureChinaCloud Zielen auf vorhandene öffentliche Instanzen des Azure Resource Manager ab.</span><span class="sxs-lookup"><span data-stu-id="4995b-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="4995b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4995b-110">EXAMPLES</span></span>

### <span data-ttu-id="4995b-111">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="4995b-111">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="4995b-112">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispiel Endpunkten mithilfe von Add-AzureRmEnvironment, und dann ändern wir den Wert der Attribute ActiveDirectoryEndpoint und GraphEndpoint der erstellten Umgebung mit dem Cmdlet-Cmdlet-Satz-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="4995b-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="4995b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4995b-113">PARAMETERS</span></span>

### <span data-ttu-id="4995b-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4995b-115">Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="4995b-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="4995b-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4995b-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4995b-117">Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4995b-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="4995b-118">-Mandant</span><span class="sxs-lookup"><span data-stu-id="4995b-118">-AdTenant</span></span>
<span data-ttu-id="4995b-119">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="4995b-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="4995b-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-120">-ARMEndpoint</span></span>
<span data-ttu-id="4995b-121">Der Azure Resource Manager-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="4995b-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="4995b-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4995b-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="4995b-123">DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste</span><span class="sxs-lookup"><span data-stu-id="4995b-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="4995b-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4995b-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="4995b-125">DNS-Suffix des Azure Data Lake Store-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="4995b-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="4995b-126">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="4995b-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="4995b-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4995b-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="4995b-128">Gibt das Domänennamensuffix für Key Vault-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="4995b-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="4995b-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4995b-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="4995b-130">Gibt die Zielgruppe für Zugriffstoken an, die Anforderungen für Key Vault-Dienste autorisieren.</span><span class="sxs-lookup"><span data-stu-id="4995b-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="4995b-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="4995b-131">-DataLakeAudience</span></span>
<span data-ttu-id="4995b-132">Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4995b-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="4995b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4995b-133">-DefaultProfile</span></span>
<span data-ttu-id="4995b-134">Die credeetnails, Mandanten und Abonnements, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4995b-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4995b-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4995b-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="4995b-136">Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="4995b-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="4995b-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-137">-GalleryEndpoint</span></span>
<span data-ttu-id="4995b-138">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="4995b-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="4995b-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="4995b-139">-GraphAudience</span></span>
<span data-ttu-id="4995b-140">Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4995b-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="4995b-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-141">-GraphEndpoint</span></span>
<span data-ttu-id="4995b-142">Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.</span><span class="sxs-lookup"><span data-stu-id="4995b-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="4995b-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="4995b-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="4995b-144">Gibt die URL für das Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="4995b-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="4995b-145">-Name</span><span class="sxs-lookup"><span data-stu-id="4995b-145">-Name</span></span>
<span data-ttu-id="4995b-146">Gibt den Namen der Umgebung an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4995b-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="4995b-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4995b-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4995b-148">Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="4995b-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="4995b-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4995b-150">Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="4995b-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="4995b-151">-Scope</span><span class="sxs-lookup"><span data-stu-id="4995b-151">-Scope</span></span>
<span data-ttu-id="4995b-152">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="4995b-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4995b-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-153">-ServiceEndpoint</span></span>
<span data-ttu-id="4995b-154">Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="4995b-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="4995b-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4995b-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="4995b-156">Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="4995b-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="4995b-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-157">-StorageEndpoint</span></span>
<span data-ttu-id="4995b-158">Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.</span><span class="sxs-lookup"><span data-stu-id="4995b-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="4995b-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4995b-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="4995b-160">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="4995b-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="4995b-161">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4995b-161">-BatchEndpointResourceId</span></span>
<span data-ttu-id="4995b-162">Der Ressourcenbezeichner des Azure-Batch Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="4995b-162">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="4995b-163">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4995b-163">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="4995b-164">Gibt den Endpunkt für den Zugriff auf die Operation Insight-Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="4995b-164">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="4995b-165">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4995b-165">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="4995b-166">Gibt die Zielgruppe für Zugriffstoken an, die Anforderungen für Operational Insights-Dienste autorisieren.</span><span class="sxs-lookup"><span data-stu-id="4995b-166">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="4995b-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4995b-167">-Confirm</span></span>
<span data-ttu-id="4995b-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4995b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4995b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4995b-169">-WhatIf</span></span>
<span data-ttu-id="4995b-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4995b-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4995b-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4995b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4995b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4995b-172">CommonParameters</span></span>
<span data-ttu-id="4995b-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4995b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4995b-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4995b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4995b-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4995b-175">INPUTS</span></span>

### <span data-ttu-id="4995b-176">Keine</span><span class="sxs-lookup"><span data-stu-id="4995b-176">None</span></span>
<span data-ttu-id="4995b-177">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4995b-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4995b-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4995b-178">OUTPUTS</span></span>

### <span data-ttu-id="4995b-179">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4995b-179">PSAzureEnvironment</span></span>
<span data-ttu-id="4995b-180">Dieses Cmdlet gibt den Satz von Endpunkten und Metadaten zurück, die für die Kommunikation mit einer Instanz von Azure erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4995b-180">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="4995b-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="4995b-181">NOTES</span></span>

## <span data-ttu-id="4995b-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4995b-182">RELATED LINKS</span></span>

[<span data-ttu-id="4995b-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="4995b-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="4995b-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="4995b-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="4995b-185">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="4995b-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

