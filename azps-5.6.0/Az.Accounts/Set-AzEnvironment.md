---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926171"
---
# <span data-ttu-id="c1d2f-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c1d2f-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="c1d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d2f-103">Legt Eigenschaften für eine Azure-Umgebung fest.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="c1d2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1d2f-104">SYNTAX</span></span>

### <span data-ttu-id="c1d2f-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1d2f-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1d2f-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1d2f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1d2f-107">DESCRIPTION</span></span>
<span data-ttu-id="c1d2f-108">Das Set-AzEnvironment-Cmdlet legt Endpunkte und Metadaten für die Verbindung mit einer Instanz von Azure fest.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="c1d2f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1d2f-109">EXAMPLES</span></span>

### <span data-ttu-id="c1d2f-110">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="c1d2f-110">Example 1: Creating and modifying a new environment</span></span>
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
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="c1d2f-111">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispielendpunkten mit Add-AzEnvironment, und dann ändern wir den Wert der ActiveDirectoryEndpoint- und GraphEndpoint-Attribute der erstellten Umgebung mithilfe des Cmdlets Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="c1d2f-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1d2f-112">PARAMETERS</span></span>

### <span data-ttu-id="c1d2f-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c1d2f-114">Gibt die Basisbehörde für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="c1d2f-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-116">Gibt die Benutzergruppe für Token an, die Anforderungen an Azure Resource Manager- oder RdFE-Endpunkte (Service Management) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="c1d2f-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c1d2f-117">-AdTenant</span></span>
<span data-ttu-id="c1d2f-118">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="c1d2f-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-119">-ARMEndpoint</span></span>
<span data-ttu-id="c1d2f-120">Der Azure Resource Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="c1d2f-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-122">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="c1d2f-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="c1d2f-124">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c1d2f-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-126">Der Ressourcenbezeichner des Azure Attestation-Diensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2f-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="c1d2f-128">Dnssuffix des Azure Attestation-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2f-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="c1d2f-130">Dns suffix of Azure Data Lake Analytics job and catalog services</span><span class="sxs-lookup"><span data-stu-id="c1d2f-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="c1d2f-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="c1d2f-132">Dnssuffix von Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="c1d2f-133">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="c1d2f-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="c1d2f-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="c1d2f-135">Dnssuffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="c1d2f-136">Beispiel: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="c1d2f-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="c1d2f-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-138">Ressourcenbezeichner des Azure Key Vault-Datendiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="c1d2f-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="c1d2f-140">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c1d2f-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-142">Die Zielgruppe für Token, die mit der Azure Log Analytics-API authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c1d2f-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-144">Der Ressourcenbezeichner der Azure Synapse Analytics, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2f-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="c1d2f-146">Dnssuffix von Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2f-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d2f-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="c1d2f-148">Der Ressourcenbezeichner des Azure Batch-Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="c1d2f-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="c1d2f-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="c1d2f-150">Suffix der Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-150">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2f-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="c1d2f-151">-DataLakeAudience</span></span>
<span data-ttu-id="c1d2f-152">Die Zielgruppe für Token, die mit dem AD Data Lake-Dienstendpunkt authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="c1d2f-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2f-153">-DefaultProfile</span></span>
<span data-ttu-id="c1d2f-154">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d2f-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c1d2f-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="c1d2f-156">Gibt an, dass die lokale Active Directory Federation Services (ADFS)-Authentifizierung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="c1d2f-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-157">-GalleryEndpoint</span></span>
<span data-ttu-id="c1d2f-158">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="c1d2f-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="c1d2f-159">-GraphAudience</span></span>
<span data-ttu-id="c1d2f-160">Die Zielgruppe für Token, die mit dem AD Graph-Endpunkt authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="c1d2f-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-161">-GraphEndpoint</span></span>
<span data-ttu-id="c1d2f-162">Gibt die URL für Graph(Active Directory-Metadaten)-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="c1d2f-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="c1d2f-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="c1d2f-164">Gibt die URL für das Verwaltungsportal an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="c1d2f-165">-Name</span><span class="sxs-lookup"><span data-stu-id="c1d2f-165">-Name</span></span>
<span data-ttu-id="c1d2f-166">Gibt den Namen der zu ändernden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-166">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="c1d2f-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c1d2f-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c1d2f-168">Gibt die URL an, aus der .publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="c1d2f-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c1d2f-170">Gibt die URL für Azure Resource Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="c1d2f-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="c1d2f-171">-Scope</span></span>
<span data-ttu-id="c1d2f-172">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c1d2f-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-173">-ServiceEndpoint</span></span>
<span data-ttu-id="c1d2f-174">Gibt den Endpunkt für Dienstverwaltungsanforderungen (Service Management, RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="c1d2f-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="c1d2f-176">Gibt das Domänennamensuffix für Azure SQL Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="c1d2f-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1d2f-177">-StorageEndpoint</span></span>
<span data-ttu-id="c1d2f-178">Gibt den Endpunkt für den Speicherzugriff (Blob, Tabelle, Warteschlange und Datei) an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="c1d2f-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c1d2f-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="c1d2f-180">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="c1d2f-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1d2f-181">-Confirm</span></span>
<span data-ttu-id="c1d2f-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d2f-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d2f-183">-WhatIf</span></span>
<span data-ttu-id="c1d2f-184">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1d2f-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d2f-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d2f-186">CommonParameters</span></span>
<span data-ttu-id="c1d2f-187">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d2f-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d2f-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1d2f-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d2f-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1d2f-189">INPUTS</span></span>

### <span data-ttu-id="c1d2f-190">System.String</span><span class="sxs-lookup"><span data-stu-id="c1d2f-190">System.String</span></span>

### <span data-ttu-id="c1d2f-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1d2f-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1d2f-192">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1d2f-192">OUTPUTS</span></span>

### <span data-ttu-id="c1d2f-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c1d2f-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c1d2f-194">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c1d2f-194">NOTES</span></span>

## <span data-ttu-id="c1d2f-195">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c1d2f-195">RELATED LINKS</span></span>

[<span data-ttu-id="c1d2f-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c1d2f-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="c1d2f-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c1d2f-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="c1d2f-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c1d2f-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

