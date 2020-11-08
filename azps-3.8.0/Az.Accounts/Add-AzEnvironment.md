---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: c1df1917a4133cf43f7cf0db89f1d59ad2c9c151
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003248"
---
# <span data-ttu-id="e8db5-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8db5-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="e8db5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8db5-102">SYNOPSIS</span></span>
<span data-ttu-id="e8db5-103">Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8db5-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="e8db5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8db5-104">SYNTAX</span></span>

### <span data-ttu-id="e8db5-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8db5-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8db5-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8db5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8db5-107">DESCRIPTION</span></span>
<span data-ttu-id="e8db5-108">Das Add-AzEnvironment-Cmdlet fügt Endpunkte und Metadaten hinzu, damit Azure Resource Manager-Cmdlets eine Verbindung mit einer neuen Instanz des Azure Resource Manager herstellen können.</span><span class="sxs-lookup"><span data-stu-id="e8db5-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="e8db5-109">Die integrierten Umgebungen AzureCloud und AzureChinaCloud Zielen auf vorhandene öffentliche Instanzen des Azure Resource Manager ab.</span><span class="sxs-lookup"><span data-stu-id="e8db5-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="e8db5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8db5-110">EXAMPLES</span></span>

### <span data-ttu-id="e8db5-111">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="e8db5-111">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
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
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="e8db5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8db5-112">PARAMETERS</span></span>

### <span data-ttu-id="e8db5-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="e8db5-114">Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="e8db5-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e8db5-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="e8db5-116">Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e8db5-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="e8db5-117">-Mandant</span><span class="sxs-lookup"><span data-stu-id="e8db5-117">-AdTenant</span></span>
<span data-ttu-id="e8db5-118">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="e8db5-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-119">-ARMEndpoint</span></span>
<span data-ttu-id="e8db5-120">Der Azure Resource Manager-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e8db5-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="e8db5-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e8db5-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="e8db5-122">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e8db5-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="e8db5-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="e8db5-124">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8db5-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="e8db5-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e8db5-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="e8db5-126">Der Ressourcenbezeichner des Azure-Bestätigungs Diensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="e8db5-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="e8db5-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="e8db5-128">DNS-Suffix des Azure-Bestätigungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="e8db5-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="e8db5-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="e8db5-130">DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste</span><span class="sxs-lookup"><span data-stu-id="e8db5-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="e8db5-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="e8db5-132">DNS-Suffix des Azure Data Lake Store-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="e8db5-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="e8db5-133">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="e8db5-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="e8db5-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="e8db5-135">DNS-Suffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="e8db5-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="e8db5-136">Beispiel ist Vault-int.Azure-int.net</span><span class="sxs-lookup"><span data-stu-id="e8db5-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="e8db5-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e8db5-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="e8db5-138">Ressourcenbezeichner des Azure Key Vault-Datendiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="e8db5-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="e8db5-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="e8db5-140">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8db5-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="e8db5-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e8db5-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="e8db5-142">Das Publikum für Tokens, die sich mit der Azure Log Analytics-API authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e8db5-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="e8db5-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e8db5-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="e8db5-144">Der Ressourcenbezeichner des Azure-Batch Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="e8db5-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="e8db5-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="e8db5-145">-DataLakeAudience</span></span>
<span data-ttu-id="e8db5-146">Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e8db5-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="e8db5-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8db5-147">-DefaultProfile</span></span>
<span data-ttu-id="e8db5-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="e8db5-148">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8db5-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="e8db5-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="e8db5-150">Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e8db5-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="e8db5-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-151">-GalleryEndpoint</span></span>
<span data-ttu-id="e8db5-152">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="e8db5-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="e8db5-153">-GraphAudience</span></span>
<span data-ttu-id="e8db5-154">Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e8db5-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="e8db5-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-155">-GraphEndpoint</span></span>
<span data-ttu-id="e8db5-156">Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="e8db5-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="e8db5-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="e8db5-158">Gibt die URL für das Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="e8db5-159">-Name</span><span class="sxs-lookup"><span data-stu-id="e8db5-159">-Name</span></span>
<span data-ttu-id="e8db5-160">Gibt den Namen der Umgebung an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8db5-160">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="e8db5-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="e8db5-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="e8db5-162">Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="e8db5-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="e8db5-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="e8db5-164">Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="e8db5-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="e8db5-165">-Scope</span></span>
<span data-ttu-id="e8db5-166">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="e8db5-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e8db5-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-167">-ServiceEndpoint</span></span>
<span data-ttu-id="e8db5-168">Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="e8db5-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="e8db5-170">Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="e8db5-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8db5-171">-StorageEndpoint</span></span>
<span data-ttu-id="e8db5-172">Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="e8db5-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e8db5-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="e8db5-174">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="e8db5-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="e8db5-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8db5-175">-Confirm</span></span>
<span data-ttu-id="e8db5-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8db5-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8db5-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8db5-177">-WhatIf</span></span>
<span data-ttu-id="e8db5-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8db5-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8db5-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8db5-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8db5-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8db5-180">CommonParameters</span></span>
<span data-ttu-id="e8db5-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8db5-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8db5-182">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8db5-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8db5-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8db5-183">INPUTS</span></span>

### <span data-ttu-id="e8db5-184">System. String</span><span class="sxs-lookup"><span data-stu-id="e8db5-184">System.String</span></span>

### <span data-ttu-id="e8db5-185">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e8db5-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8db5-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8db5-186">OUTPUTS</span></span>

### <span data-ttu-id="e8db5-187">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8db5-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e8db5-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8db5-188">NOTES</span></span>

## <span data-ttu-id="e8db5-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8db5-189">RELATED LINKS</span></span>

[<span data-ttu-id="e8db5-190">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8db5-190">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="e8db5-191">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8db5-191">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="e8db5-192">Satz-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8db5-192">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

