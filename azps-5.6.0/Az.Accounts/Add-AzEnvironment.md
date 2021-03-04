---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 62e642208e11ece3aeaab009920a5c30b53c0636
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938403"
---
# <span data-ttu-id="f6cf8-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f6cf8-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="f6cf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cf8-103">Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="f6cf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6cf8-104">SYNTAX</span></span>

### <span data-ttu-id="f6cf8-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6cf8-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6cf8-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6cf8-107">Discovery</span><span class="sxs-lookup"><span data-stu-id="f6cf8-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6cf8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6cf8-108">DESCRIPTION</span></span>
<span data-ttu-id="f6cf8-109">Das Add-AzEnvironment-Cmdlet fügt Endpunkte und Metadaten hinzu, damit Azure Resource Manager-Cmdlets eine Verbindung mit einer neuen Instanz von Azure Resource Manager herstellen können.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f6cf8-110">Die integrierten Umgebungen AzureCloud und AzureChinaCloud zielen auf vorhandene öffentliche Instanzen von Azure Resource Manager ab.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f6cf8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6cf8-111">EXAMPLES</span></span>

### <span data-ttu-id="f6cf8-112">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="f6cf8-112">Example 1: Creating and modifying a new environment</span></span>
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
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="f6cf8-113">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispielendpunkten mit Add-AzEnvironment, und dann ändern wir den Wert der ActiveDirectoryEndpoint- und GraphEndpoint-Attribute der erstellten Umgebung mithilfe des Cmdlets Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="f6cf8-114">Beispiel 2: Entdecken einer neuen Umgebung über Uri</span><span class="sxs-lookup"><span data-stu-id="f6cf8-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="f6cf8-115">In diesem Beispiel entdecken wir eine neue Azure-Umgebung aus dem `https://configuredmetadata.net` Uri.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="f6cf8-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6cf8-116">PARAMETERS</span></span>

### <span data-ttu-id="f6cf8-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f6cf8-118">Gibt die Basisbehörde für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f6cf8-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-120">Gibt die Benutzergruppe für Token an, die Anforderungen an Azure Resource Manager- oder RdFE-Endpunkte (Service Management) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f6cf8-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f6cf8-121">-AdTenant</span></span>
<span data-ttu-id="f6cf8-122">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f6cf8-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-123">-ARMEndpoint</span></span>
<span data-ttu-id="f6cf8-124">Der Azure Resource Manager-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="f6cf8-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="f6cf8-125">-AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="f6cf8-125">-AutoDiscover</span></span>
<span data-ttu-id="f6cf8-126">Ermittelt Umgebungen über den standardmäßigen oder konfigurierten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-128">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="f6cf8-130">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-132">Der Ressourcenbezeichner des Azure Attestation-Diensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="f6cf8-134">Dnssuffix des Azure Attestation-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f6cf8-136">Dns suffix of Azure Data Lake Analytics job and catalog services</span><span class="sxs-lookup"><span data-stu-id="f6cf8-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f6cf8-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f6cf8-138">Dnssuffix von Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="f6cf8-139">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f6cf8-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f6cf8-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f6cf8-141">Dnssuffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="f6cf8-142">Beispiel: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="f6cf8-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-144">Ressourcenbezeichner des Azure Key Vault-Datendiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="f6cf8-146">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-148">Die Zielgruppe für Token, die mit der Azure Log Analytics-API authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-150">Der Ressourcenbezeichner der Azure Synapse Analytics, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="f6cf8-152">Dnssuffix von Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f6cf8-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="f6cf8-154">Der Ressourcenbezeichner des Azure Batch-Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="f6cf8-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="f6cf8-156">Suffix der Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-156">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f6cf8-157">-DataLakeAudience</span></span>
<span data-ttu-id="f6cf8-158">Die Zielgruppe für Token, die mit dem AD Data Lake-Dienstendpunkt authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6cf8-159">-DefaultProfile</span></span>
<span data-ttu-id="f6cf8-160">Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f6cf8-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6cf8-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f6cf8-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f6cf8-162">Gibt an, dass die lokale Active Directory Federation Services (ADFS)-Authentifizierung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f6cf8-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-163">-GalleryEndpoint</span></span>
<span data-ttu-id="f6cf8-164">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f6cf8-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f6cf8-165">-GraphAudience</span></span>
<span data-ttu-id="f6cf8-166">Die Zielgruppe für Token, die mit dem AD Graph-Endpunkt authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f6cf8-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-167">-GraphEndpoint</span></span>
<span data-ttu-id="f6cf8-168">Gibt die URL für Graph(Active Directory-Metadaten)-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f6cf8-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f6cf8-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="f6cf8-170">Gibt die URL für das Verwaltungsportal an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-170">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f6cf8-171">-Name</span><span class="sxs-lookup"><span data-stu-id="f6cf8-171">-Name</span></span>
<span data-ttu-id="f6cf8-172">Gibt den Namen der hinzuzufügenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-172">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f6cf8-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f6cf8-174">Gibt die URL an, aus der .publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f6cf8-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f6cf8-176">Gibt die URL für Azure Resource Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-176">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f6cf8-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="f6cf8-177">-Scope</span></span>
<span data-ttu-id="f6cf8-178">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f6cf8-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-179">-ServiceEndpoint</span></span>
<span data-ttu-id="f6cf8-180">Gibt den Endpunkt für Dienstverwaltungsanforderungen (Service Management, RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f6cf8-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f6cf8-182">Gibt das Domänennamensuffix für Azure SQL Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f6cf8-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6cf8-183">-StorageEndpoint</span></span>
<span data-ttu-id="f6cf8-184">Gibt den Endpunkt für den Speicherzugriff (Blob, Tabelle, Warteschlange und Datei) an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f6cf8-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f6cf8-186">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f6cf8-187">-URI</span><span class="sxs-lookup"><span data-stu-id="f6cf8-187">-Uri</span></span>
<span data-ttu-id="f6cf8-188">Gibt den URI der Internetressource zum Abrufen von Umgebungen an.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-188">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6cf8-189">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6cf8-189">-Confirm</span></span>
<span data-ttu-id="f6cf8-190">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6cf8-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6cf8-191">-WhatIf</span></span>
<span data-ttu-id="f6cf8-192">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6cf8-193">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6cf8-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cf8-194">CommonParameters</span></span>
<span data-ttu-id="f6cf8-195">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6cf8-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cf8-196">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6cf8-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cf8-197">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6cf8-197">INPUTS</span></span>

### <span data-ttu-id="f6cf8-198">System.String</span><span class="sxs-lookup"><span data-stu-id="f6cf8-198">System.String</span></span>

### <span data-ttu-id="f6cf8-199">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6cf8-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f6cf8-200">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6cf8-200">OUTPUTS</span></span>

### <span data-ttu-id="f6cf8-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f6cf8-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f6cf8-202">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6cf8-202">NOTES</span></span>

## <span data-ttu-id="f6cf8-203">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6cf8-203">RELATED LINKS</span></span>

[<span data-ttu-id="f6cf8-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f6cf8-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="f6cf8-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f6cf8-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="f6cf8-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f6cf8-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

