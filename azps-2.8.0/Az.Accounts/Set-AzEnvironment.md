---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658426"
---
# <span data-ttu-id="04047-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="04047-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="04047-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04047-102">SYNOPSIS</span></span>
<span data-ttu-id="04047-103">Legt Eigenschaften für eine Azure-Umgebung fest.</span><span class="sxs-lookup"><span data-stu-id="04047-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="04047-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04047-104">SYNTAX</span></span>

### <span data-ttu-id="04047-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="04047-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04047-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04047-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04047-107">DESCRIPTION</span></span>
<span data-ttu-id="04047-108">Das Set-AzEnvironment-Cmdlet legt Endpunkte und Metadaten für die Verbindung mit einer Instanz von Azure fest.</span><span class="sxs-lookup"><span data-stu-id="04047-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="04047-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04047-109">EXAMPLES</span></span>

### <span data-ttu-id="04047-110">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="04047-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

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
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
```

<span data-ttu-id="04047-111">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispiel Endpunkten mithilfe von Add-AzEnvironment, und dann ändern wir den Wert der Attribute ActiveDirectoryEndpoint und GraphEndpoint der erstellten Umgebung mit dem Cmdlet-Cmdlet-Satz-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="04047-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="04047-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="04047-112">PARAMETERS</span></span>

### <span data-ttu-id="04047-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="04047-114">Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="04047-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="04047-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="04047-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="04047-116">Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="04047-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="04047-117">-Mandant</span><span class="sxs-lookup"><span data-stu-id="04047-117">-AdTenant</span></span>
<span data-ttu-id="04047-118">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="04047-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="04047-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-119">-ARMEndpoint</span></span>
<span data-ttu-id="04047-120">Der Azure Resource Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="04047-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="04047-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="04047-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="04047-122">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="04047-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="04047-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="04047-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="04047-124">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04047-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="04047-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="04047-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="04047-126">DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste</span><span class="sxs-lookup"><span data-stu-id="04047-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="04047-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="04047-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="04047-128">DNS-Suffix des Azure Data Lake Store-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="04047-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="04047-129">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="04047-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="04047-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="04047-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="04047-131">DNS-Suffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="04047-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="04047-132">Beispiel ist Vault-int.Azure-int.net</span><span class="sxs-lookup"><span data-stu-id="04047-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="04047-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="04047-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="04047-134">Ressourcenbezeichner des Azure Key Vault-Datendiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="04047-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04047-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="04047-136">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04047-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04047-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="04047-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="04047-138">Das Publikum für Tokens, die sich mit der Azure Log Analytics-API authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="04047-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04047-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="04047-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="04047-140">Der Ressourcenbezeichner des Azure-Batch Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="04047-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04047-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="04047-141">-DataLakeAudience</span></span>
<span data-ttu-id="04047-142">Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="04047-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="04047-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04047-143">-DefaultProfile</span></span>
<span data-ttu-id="04047-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04047-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04047-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="04047-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="04047-146">Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="04047-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="04047-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-147">-GalleryEndpoint</span></span>
<span data-ttu-id="04047-148">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="04047-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="04047-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="04047-149">-GraphAudience</span></span>
<span data-ttu-id="04047-150">Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="04047-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="04047-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-151">-GraphEndpoint</span></span>
<span data-ttu-id="04047-152">Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.</span><span class="sxs-lookup"><span data-stu-id="04047-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="04047-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="04047-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="04047-154">Gibt die URL für das Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="04047-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="04047-155">-Name</span><span class="sxs-lookup"><span data-stu-id="04047-155">-Name</span></span>
<span data-ttu-id="04047-156">Gibt den Namen der zu ändernden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="04047-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="04047-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="04047-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="04047-158">Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="04047-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="04047-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="04047-160">Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="04047-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="04047-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="04047-161">-Scope</span></span>
<span data-ttu-id="04047-162">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="04047-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="04047-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-163">-ServiceEndpoint</span></span>
<span data-ttu-id="04047-164">Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="04047-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="04047-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="04047-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="04047-166">Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="04047-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="04047-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="04047-167">-StorageEndpoint</span></span>
<span data-ttu-id="04047-168">Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.</span><span class="sxs-lookup"><span data-stu-id="04047-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="04047-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="04047-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="04047-170">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="04047-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="04047-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04047-171">-Confirm</span></span>
<span data-ttu-id="04047-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04047-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04047-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04047-173">-WhatIf</span></span>
<span data-ttu-id="04047-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04047-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04047-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04047-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04047-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04047-176">CommonParameters</span></span>
<span data-ttu-id="04047-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04047-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04047-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04047-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04047-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04047-179">INPUTS</span></span>

### <span data-ttu-id="04047-180">System. String</span><span class="sxs-lookup"><span data-stu-id="04047-180">System.String</span></span>

### <span data-ttu-id="04047-181">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="04047-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="04047-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04047-182">OUTPUTS</span></span>

### <span data-ttu-id="04047-183">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="04047-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="04047-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="04047-184">NOTES</span></span>

## <span data-ttu-id="04047-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04047-185">RELATED LINKS</span></span>

[<span data-ttu-id="04047-186">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="04047-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="04047-187">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="04047-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="04047-188">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="04047-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

