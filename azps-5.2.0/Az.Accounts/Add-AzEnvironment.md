---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 92a8c816f1c5a76b0f3725b70a627b798b9de2b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292307"
---
# <span data-ttu-id="414f0-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="414f0-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="414f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="414f0-102">SYNOPSIS</span></span>
<span data-ttu-id="414f0-103">Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="414f0-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="414f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="414f0-104">SYNTAX</span></span>

### <span data-ttu-id="414f0-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="414f0-105">Name (Default)</span></span>
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

### <span data-ttu-id="414f0-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-106">ARMEndpoint</span></span>
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

### <span data-ttu-id="414f0-107">Ermittlung</span><span class="sxs-lookup"><span data-stu-id="414f0-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="414f0-108">DESCRIPTION</span></span>
<span data-ttu-id="414f0-109">Das Add-AzEnvironment cmdlet fügt Endpunkte und Metadaten hinzu, damit Azure Resource -Manager-Cmdlets eine Verbindung mit einer neuen Instanz von Azure Resource Manager herstellen können.</span><span class="sxs-lookup"><span data-stu-id="414f0-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="414f0-110">Die integrierten Umgebungen AzureCloud und AzureChinaCloud sind für vorhandene öffentliche Instanzen von Azure Resource Manager bestimmt.</span><span class="sxs-lookup"><span data-stu-id="414f0-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="414f0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="414f0-111">EXAMPLES</span></span>

### <span data-ttu-id="414f0-112">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="414f0-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="414f0-113">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispielendpunkten mit Add-AzEnvironment und ändern dann den Wert der ActiveDirectoryEndpoint- und GraphEndpoint-Attribute der erstellten Umgebung mithilfe des Cmdlets "Set-AzEnvironment".</span><span class="sxs-lookup"><span data-stu-id="414f0-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="414f0-114">Beispiel 2: Ermitteln einer neuen Umgebung über den URI</span><span class="sxs-lookup"><span data-stu-id="414f0-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="414f0-115">In diesem Beispiel ermitteln wir eine neue Azure-Umgebung über den `https://configuredmetadata.net` URI.</span><span class="sxs-lookup"><span data-stu-id="414f0-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="414f0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="414f0-116">PARAMETERS</span></span>

### <span data-ttu-id="414f0-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="414f0-118">Gibt die Basisbehörde für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="414f0-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="414f0-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="414f0-120">Gibt die Benutzergruppe für Token an, mit der Anforderungen an Azure Resource Manager- oder Service Management (RDFE)-Endpunkte authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="414f0-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="414f0-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="414f0-121">-AdTenant</span></span>
<span data-ttu-id="414f0-122">Gibt den Standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="414f0-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="414f0-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-123">-ARMEndpoint</span></span>
<span data-ttu-id="414f0-124">Der Azure Resource Manager-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="414f0-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="414f0-125">-AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="414f0-125">-AutoDiscover</span></span>
<span data-ttu-id="414f0-126">Ermittelt Umgebungen über den standardmäßigen oder konfigurierten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="414f0-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="414f0-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="414f0-128">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="414f0-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="414f0-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="414f0-130">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="414f0-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="414f0-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="414f0-132">Die Ressourcen-ID des Azure-Nachweisdiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="414f0-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="414f0-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="414f0-134">Dns-Suffix des Azure-Nachweisdiensts.</span><span class="sxs-lookup"><span data-stu-id="414f0-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="414f0-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="414f0-136">Dns Suffix des Auftrags- und Katalogdiensts von Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="414f0-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="414f0-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="414f0-138">Dns-Suffix von Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="414f0-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="414f0-139">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="414f0-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="414f0-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="414f0-141">Dns-Suffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="414f0-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="414f0-142">Beispiel: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="414f0-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="414f0-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="414f0-144">Ressourcen-ID des Azure Key Vault-Datendiensts, der empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="414f0-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="414f0-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="414f0-146">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="414f0-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="414f0-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="414f0-148">Die Zielgruppe für Token, die sich mit der Azure Log Analytics-API authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="414f0-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="414f0-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="414f0-150">Die Ressourcen-ID der Azure Synapse Analytics, die der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="414f0-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="414f0-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="414f0-152">Dns-Suffix von Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="414f0-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="414f0-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="414f0-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="414f0-154">Die Ressourcen-ID des Azure Batch-Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="414f0-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="414f0-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="414f0-156">Suffix der Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="414f0-156">Suffix of Azure Container Registry.</span></span>

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

### <span data-ttu-id="414f0-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="414f0-157">-DataLakeAudience</span></span>
<span data-ttu-id="414f0-158">Die Zielgruppe für Token, die sich mit dem Ad Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="414f0-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="414f0-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414f0-159">-DefaultProfile</span></span>
<span data-ttu-id="414f0-160">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="414f0-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="414f0-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="414f0-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="414f0-162">Gibt an, dass die lokale Active Directory Federation Services (ADFS)-Authentifizierung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="414f0-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="414f0-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-163">-GalleryEndpoint</span></span>
<span data-ttu-id="414f0-164">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="414f0-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="414f0-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="414f0-165">-GraphAudience</span></span>
<span data-ttu-id="414f0-166">Die Zielgruppe für Token, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="414f0-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="414f0-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-167">-GraphEndpoint</span></span>
<span data-ttu-id="414f0-168">Gibt die URL für Graph(Active Directory-Metadaten)-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="414f0-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="414f0-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="414f0-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="414f0-170">Gibt die URL für das Verwaltungsportal an.</span><span class="sxs-lookup"><span data-stu-id="414f0-170">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="414f0-171">-Name</span><span class="sxs-lookup"><span data-stu-id="414f0-171">-Name</span></span>
<span data-ttu-id="414f0-172">Gibt den Namen der hinzuzufügenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="414f0-172">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="414f0-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="414f0-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="414f0-174">Gibt die URL an, über die .publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="414f0-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="414f0-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="414f0-176">Gibt die URL für Azure Resource Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="414f0-176">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="414f0-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="414f0-177">-Scope</span></span>
<span data-ttu-id="414f0-178">Bestimmt den Umfang der Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="414f0-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="414f0-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-179">-ServiceEndpoint</span></span>
<span data-ttu-id="414f0-180">Gibt den Endpunkt für Dienstverwaltungsanforderungen (Service Management, RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="414f0-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="414f0-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="414f0-182">Gibt das Domänensuffix für Azure SQL Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="414f0-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="414f0-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="414f0-183">-StorageEndpoint</span></span>
<span data-ttu-id="414f0-184">Gibt den Endpunkt für den Speicherzugriff (BLOB, Tabelle, Warteschlange und Datei) an.</span><span class="sxs-lookup"><span data-stu-id="414f0-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="414f0-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="414f0-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="414f0-186">Gibt das Domänensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="414f0-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="414f0-187">-URI</span><span class="sxs-lookup"><span data-stu-id="414f0-187">-Uri</span></span>
<span data-ttu-id="414f0-188">Gibt den URI der Internetressource an, um Umgebungen zu abrufen.</span><span class="sxs-lookup"><span data-stu-id="414f0-188">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="414f0-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="414f0-189">-Confirm</span></span>
<span data-ttu-id="414f0-190">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="414f0-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414f0-191">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="414f0-191">-WhatIf</span></span>
<span data-ttu-id="414f0-192">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="414f0-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="414f0-193">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="414f0-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414f0-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414f0-194">CommonParameters</span></span>
<span data-ttu-id="414f0-195">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="414f0-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414f0-196">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="414f0-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414f0-197">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="414f0-197">INPUTS</span></span>

### <span data-ttu-id="414f0-198">System.String</span><span class="sxs-lookup"><span data-stu-id="414f0-198">System.String</span></span>

### <span data-ttu-id="414f0-199">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="414f0-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="414f0-200">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="414f0-200">OUTPUTS</span></span>

### <span data-ttu-id="414f0-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="414f0-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="414f0-202">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="414f0-202">NOTES</span></span>

## <span data-ttu-id="414f0-203">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="414f0-203">RELATED LINKS</span></span>

[<span data-ttu-id="414f0-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="414f0-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="414f0-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="414f0-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="414f0-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="414f0-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

