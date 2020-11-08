---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: ba5a398e21543bc4b19c09309884ceb11fed3197
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173975"
---
# <span data-ttu-id="37169-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="37169-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="37169-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37169-102">SYNOPSIS</span></span>
<span data-ttu-id="37169-103">Fügt Endpunkte und Metadaten für eine Instanz von Azure Resource Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="37169-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="37169-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37169-104">SYNTAX</span></span>

### <span data-ttu-id="37169-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="37169-105">Name (Default)</span></span>
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
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37169-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37169-107">Entdeckung</span><span class="sxs-lookup"><span data-stu-id="37169-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37169-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37169-108">DESCRIPTION</span></span>
<span data-ttu-id="37169-109">Das Add-AzEnvironment-Cmdlet fügt Endpunkte und Metadaten hinzu, damit Azure Resource Manager-Cmdlets eine Verbindung mit einer neuen Instanz des Azure Resource Manager herstellen können.</span><span class="sxs-lookup"><span data-stu-id="37169-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="37169-110">Die integrierten Umgebungen AzureCloud und AzureChinaCloud Zielen auf vorhandene öffentliche Instanzen des Azure Resource Manager ab.</span><span class="sxs-lookup"><span data-stu-id="37169-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="37169-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37169-111">EXAMPLES</span></span>

### <span data-ttu-id="37169-112">Beispiel 1: Erstellen und Ändern einer neuen Umgebung</span><span class="sxs-lookup"><span data-stu-id="37169-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="37169-113">In diesem Beispiel erstellen wir eine neue Azure-Umgebung mit Beispiel Endpunkten mithilfe von Add-AzEnvironment, und dann ändern wir den Wert der Attribute ActiveDirectoryEndpoint und GraphEndpoint der erstellten Umgebung mit dem Cmdlet-Cmdlet-Satz-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="37169-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="37169-114">Beispiel 2: Entdecken einer neuen Umgebung über URI</span><span class="sxs-lookup"><span data-stu-id="37169-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="37169-115">In diesem Beispiel entdecken wir eine neue Azure-Umgebung aus dem https://configuredmetadata.net URI.</span><span class="sxs-lookup"><span data-stu-id="37169-115">In this example, we are discovering a new Azure environment from the https://configuredmetadata.net Uri.</span></span>

## <span data-ttu-id="37169-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="37169-116">PARAMETERS</span></span>

### <span data-ttu-id="37169-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="37169-118">Gibt die Basis Autorität für die Azure Active Directory-Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="37169-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="37169-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="37169-120">Gibt das Publikum für Token an, die Anforderungen an Azure Resource Manager-oder Service Management-Endpunkte (RDFE) authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="37169-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="37169-121">-Mandant</span><span class="sxs-lookup"><span data-stu-id="37169-121">-AdTenant</span></span>
<span data-ttu-id="37169-122">Gibt den standardmäßigen Active Directory-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="37169-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="37169-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-123">-ARMEndpoint</span></span>
<span data-ttu-id="37169-124">Der Azure Resource Manager-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="37169-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="37169-125">-AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="37169-125">-AutoDiscover</span></span>
<span data-ttu-id="37169-126">Erkennt Umgebungen über den standardmäßigen oder konfigurierten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="37169-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="37169-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="37169-128">Der Ressourcenbezeichner der Azure Analysis Services-Ressource.</span><span class="sxs-lookup"><span data-stu-id="37169-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="37169-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="37169-130">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37169-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="37169-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="37169-132">Der Ressourcenbezeichner des Azure-Bestätigungs Diensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="37169-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="37169-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="37169-134">DNS-Suffix des Azure-Bestätigungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="37169-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="37169-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="37169-136">DNS-Suffix der Azure Data Lake Analytics-Auftrags-und Katalogdienste</span><span class="sxs-lookup"><span data-stu-id="37169-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="37169-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="37169-138">DNS-Suffix des Azure Data Lake Store-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="37169-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="37169-139">Beispiel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="37169-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="37169-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="37169-141">DNS-Suffix des Azure Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="37169-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="37169-142">Beispiel ist Vault-int.Azure-int.net</span><span class="sxs-lookup"><span data-stu-id="37169-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="37169-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="37169-144">Ressourcenbezeichner des Azure Key Vault-Datendiensts, der der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="37169-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="37169-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="37169-146">Der Endpunkt, der bei der Kommunikation mit der Azure Log Analytics-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37169-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="37169-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="37169-148">Das Publikum für Tokens, die sich mit der Azure Log Analytics-API authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="37169-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="37169-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="37169-150">Der Ressourcenbezeichner der Azure Synapse-Analyse, die der Empfänger des angeforderten Tokens ist.</span><span class="sxs-lookup"><span data-stu-id="37169-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="37169-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="37169-152">DNS-Suffix der Azure Synapse-Analyse.</span><span class="sxs-lookup"><span data-stu-id="37169-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="37169-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37169-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="37169-154">Der Ressourcenbezeichner des Azure-Batch Diensts, der der Empfänger des angeforderten Tokens ist</span><span class="sxs-lookup"><span data-stu-id="37169-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="37169-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="37169-155">-DataLakeAudience</span></span>
<span data-ttu-id="37169-156">Das Publikum für Tokens, die sich mit dem AD Data Lake Services-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="37169-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="37169-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37169-157">-DefaultProfile</span></span>
<span data-ttu-id="37169-158">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="37169-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37169-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="37169-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="37169-160">Gibt an, dass die lokale Authentifizierung (Active Directory Federation Services, ADFS) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="37169-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="37169-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-161">-GalleryEndpoint</span></span>
<span data-ttu-id="37169-162">Gibt den Endpunkt für den Azure Resource Manager-Katalog mit Bereitstellungsvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="37169-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="37169-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="37169-163">-GraphAudience</span></span>
<span data-ttu-id="37169-164">Das Publikum für Tokens, die sich mit dem AD Graph-Endpunkt authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="37169-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="37169-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-165">-GraphEndpoint</span></span>
<span data-ttu-id="37169-166">Gibt die URL für Graph-Anforderungen (Active Directory-Metadaten) an.</span><span class="sxs-lookup"><span data-stu-id="37169-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="37169-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="37169-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="37169-168">Gibt die URL für das Verwaltungs Portal an.</span><span class="sxs-lookup"><span data-stu-id="37169-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="37169-169">-Name</span><span class="sxs-lookup"><span data-stu-id="37169-169">-Name</span></span>
<span data-ttu-id="37169-170">Gibt den Namen der Umgebung an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37169-170">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="37169-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="37169-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="37169-172">Gibt die URL an, aus der publishsettings-Dateien heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="37169-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="37169-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="37169-174">Gibt die URL für Azure-Ressourcen-Manager-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="37169-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="37169-175">-Scope</span><span class="sxs-lookup"><span data-stu-id="37169-175">-Scope</span></span>
<span data-ttu-id="37169-176">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="37169-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="37169-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-177">-ServiceEndpoint</span></span>
<span data-ttu-id="37169-178">Gibt den Endpunkt für Service Management-Anforderungen (RDFE) an.</span><span class="sxs-lookup"><span data-stu-id="37169-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="37169-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="37169-180">Gibt das Domänennamensuffix für Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="37169-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="37169-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="37169-181">-StorageEndpoint</span></span>
<span data-ttu-id="37169-182">Gibt den Endpunkt für den Speicher (BLOB-, Tabellen-, Warteschlangen-und Dateizugriff) an.</span><span class="sxs-lookup"><span data-stu-id="37169-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="37169-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="37169-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="37169-184">Gibt das Domänennamensuffix für Azure Traffic Manager-Dienste an.</span><span class="sxs-lookup"><span data-stu-id="37169-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="37169-185">-URI</span><span class="sxs-lookup"><span data-stu-id="37169-185">-Uri</span></span>
<span data-ttu-id="37169-186">Gibt den URI der Internetressource an, um Umgebungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="37169-186">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="37169-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37169-187">-Confirm</span></span>
<span data-ttu-id="37169-188">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37169-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37169-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37169-189">-WhatIf</span></span>
<span data-ttu-id="37169-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37169-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37169-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37169-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37169-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37169-192">CommonParameters</span></span>
<span data-ttu-id="37169-193">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37169-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37169-194">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37169-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37169-195">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37169-195">INPUTS</span></span>

### <span data-ttu-id="37169-196">System. String</span><span class="sxs-lookup"><span data-stu-id="37169-196">System.String</span></span>

### <span data-ttu-id="37169-197">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="37169-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37169-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37169-198">OUTPUTS</span></span>

### <span data-ttu-id="37169-199">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="37169-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="37169-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="37169-200">NOTES</span></span>

## <span data-ttu-id="37169-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37169-201">RELATED LINKS</span></span>

[<span data-ttu-id="37169-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="37169-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="37169-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="37169-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="37169-204">Satz-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="37169-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

