---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 5ede64a5efaa5e44b5de5551bde4d17730b910b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996688"
---
# <span data-ttu-id="4d2cc-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d2cc-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="4d2cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d2cc-103">Legt Eigenschaften für eine Azure-Umgebung fest.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="4d2cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d2cc-104">SYNTAX</span></span>

### <span data-ttu-id="4d2cc-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d2cc-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d2cc-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d2cc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d2cc-107">DESCRIPTION</span></span>
<span data-ttu-id="4d2cc-108">Das Set-AzEnvironment-Cmdlet legt Endpunkte und Metadaten für die Verbindung mit einer Instanz von Azure fest.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="4d2cc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d2cc-109">EXAMPLES</span></span>

### <span data-ttu-id="4d2cc-110">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="4d2cc-110">Example 1: Creating and modifying a new environment</span></span>
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
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
```

<span data-ttu-id="4d2cc-111">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispiel Endpunkten mithilfe von Add-AzEnvironment, und dann ändern wir den Wert der Attribute ActiveDirectoryEndpoint und GraphEndpoint der erstellten Umgebung mit dem Cmdlet-Cmdlet-Satz-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="4d2cc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d2cc-112">PARAMETERS</span></span>

### <span data-ttu-id="4d2cc-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4d2cc-114">Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="4d2cc-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2cc-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4d2cc-116">Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="4d2cc-117">-Mandant</span><span class="sxs-lookup"><span data-stu-id="4d2cc-117">-AdTenant</span></span>
<span data-ttu-id="4d2cc-118">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="4d2cc-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-119">-ARMEndpoint</span></span>
<span data-ttu-id="4d2cc-120">Der Azure Resource Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="4d2cc-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2cc-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="4d2cc-122">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="4d2cc-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="4d2cc-124">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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
### <span data-ttu-id="4d2cc-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2cc-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="4d2cc-126">Der Ressourcenbezeichner des Azure-Bestätigungs Diensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4d2cc-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="4d2cc-128">DNS-Suffix des Azure-Bestätigungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="4d2cc-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="4d2cc-130">DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste</span><span class="sxs-lookup"><span data-stu-id="4d2cc-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="4d2cc-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="4d2cc-132">DNS-Suffix des Azure Data Lake Store-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="4d2cc-133">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="4d2cc-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="4d2cc-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="4d2cc-135">DNS-Suffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="4d2cc-136">Beispiel ist Vault-int.Azure-int.net</span><span class="sxs-lookup"><span data-stu-id="4d2cc-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="4d2cc-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2cc-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="4d2cc-138">Ressourcenbezeichner des Azure Key Vault-Datendiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4d2cc-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="4d2cc-140">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4d2cc-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2cc-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="4d2cc-142">Das Publikum für Tokens, die sich mit der Azure Log Analytics-API authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4d2cc-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d2cc-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="4d2cc-144">Der Ressourcenbezeichner des Azure-Batch Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="4d2cc-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="4d2cc-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="4d2cc-145">-DataLakeAudience</span></span>
<span data-ttu-id="4d2cc-146">Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="4d2cc-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d2cc-147">-DefaultProfile</span></span>
<span data-ttu-id="4d2cc-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-148">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d2cc-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4d2cc-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="4d2cc-150">Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="4d2cc-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-151">-GalleryEndpoint</span></span>
<span data-ttu-id="4d2cc-152">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="4d2cc-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="4d2cc-153">-GraphAudience</span></span>
<span data-ttu-id="4d2cc-154">Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="4d2cc-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-155">-GraphEndpoint</span></span>
<span data-ttu-id="4d2cc-156">Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="4d2cc-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="4d2cc-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="4d2cc-158">Gibt die URL für das Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="4d2cc-159">-Name</span><span class="sxs-lookup"><span data-stu-id="4d2cc-159">-Name</span></span>
<span data-ttu-id="4d2cc-160">Gibt den Namen der zu ändernden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-160">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="4d2cc-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4d2cc-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4d2cc-162">Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="4d2cc-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4d2cc-164">Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="4d2cc-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="4d2cc-165">-Scope</span></span>
<span data-ttu-id="4d2cc-166">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4d2cc-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-167">-ServiceEndpoint</span></span>
<span data-ttu-id="4d2cc-168">Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="4d2cc-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="4d2cc-170">Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="4d2cc-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d2cc-171">-StorageEndpoint</span></span>
<span data-ttu-id="4d2cc-172">Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="4d2cc-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4d2cc-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="4d2cc-174">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="4d2cc-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d2cc-175">-Confirm</span></span>
<span data-ttu-id="4d2cc-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d2cc-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d2cc-177">-WhatIf</span></span>
<span data-ttu-id="4d2cc-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d2cc-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d2cc-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d2cc-180">CommonParameters</span></span>
<span data-ttu-id="4d2cc-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d2cc-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d2cc-182">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d2cc-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d2cc-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d2cc-183">INPUTS</span></span>

### <span data-ttu-id="4d2cc-184">System. String</span><span class="sxs-lookup"><span data-stu-id="4d2cc-184">System.String</span></span>

### <span data-ttu-id="4d2cc-185">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4d2cc-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d2cc-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d2cc-186">OUTPUTS</span></span>

### <span data-ttu-id="4d2cc-187">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d2cc-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="4d2cc-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d2cc-188">NOTES</span></span>

## <span data-ttu-id="4d2cc-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d2cc-189">RELATED LINKS</span></span>

[<span data-ttu-id="4d2cc-190">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d2cc-190">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="4d2cc-191">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d2cc-191">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="4d2cc-192">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d2cc-192">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

