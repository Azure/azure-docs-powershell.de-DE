---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 2ff0f9f03524368e01b6edbcad5b8db8fef4fb21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949195"
---
# <span data-ttu-id="46dad-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="46dad-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="46dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46dad-102">SYNOPSIS</span></span>
<span data-ttu-id="46dad-103">Aktualisiert einen vorhandenen Fhir-Dienst im GesundheitswesenApis.</span><span class="sxs-lookup"><span data-stu-id="46dad-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="46dad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46dad-104">SYNTAX</span></span>

### <span data-ttu-id="46dad-105">ServiceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="46dad-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46dad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46dad-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46dad-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46dad-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46dad-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46dad-108">DESCRIPTION</span></span>
<span data-ttu-id="46dad-109">Aktualisiert einen vorhandenen Fhir-Dienst im GesundheitswesenApis.</span><span class="sxs-lookup"><span data-stu-id="46dad-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="46dad-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46dad-110">EXAMPLES</span></span>

### <span data-ttu-id="46dad-111">Beispiel 1: Aktualisiert den vorhandenen Healthcareapis-Dienst mit dem Namen MyService in der Ressourcengruppe MyResourceGroup mit dem cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="46dad-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : 
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="46dad-112">Beispiel 2: Aktualisiert den vorhandenen Healthcareapis-Dienst mit dem Namen MyService in der Ressourcengruppe MyResourceGroup mit dem cosmosdb OfferThroughput = 500 und key vault key uri "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/".</span><span class="sxs-lookup"><span data-stu-id="46dad-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="46dad-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46dad-113">PARAMETERS</span></span>

### <span data-ttu-id="46dad-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="46dad-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="46dad-115">Liste der Access-Richtlinienobjekt-IDs.</span><span class="sxs-lookup"><span data-stu-id="46dad-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="46dad-116">-AllowCorsCredential</span></span>
<span data-ttu-id="46dad-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="46dad-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46dad-118">-AsJob</span></span>
<span data-ttu-id="46dad-119">Führen Sie das Cmdlet als Auftrag im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="46dad-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-120">-Audience</span><span class="sxs-lookup"><span data-stu-id="46dad-120">-Audience</span></span>
<span data-ttu-id="46dad-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="46dad-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-122">-Autorität</span><span class="sxs-lookup"><span data-stu-id="46dad-122">-Authority</span></span>
<span data-ttu-id="46dad-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="46dad-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="46dad-124">-CorsHeader</span></span>
<span data-ttu-id="46dad-125">HealthcareApis FhirService List of Cors Headers.</span><span class="sxs-lookup"><span data-stu-id="46dad-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="46dad-126">Geben Sie HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="46dad-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="46dad-127">Verwenden Sie " \* " für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="46dad-127">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="46dad-128">-CorsMaxAge</span></span>
<span data-ttu-id="46dad-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="46dad-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="46dad-130">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="46dad-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="46dad-131">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="46dad-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="46dad-132">-CorsMethod</span></span>
<span data-ttu-id="46dad-133">HealthcareApis FhirService List of Cors Methods.</span><span class="sxs-lookup"><span data-stu-id="46dad-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="46dad-134">-CorsOrigin</span></span>
<span data-ttu-id="46dad-135">HealthcareApis FhirService List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="46dad-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="46dad-136">Geben Sie URLs von Ursprungswebsites an, die auf diese API zugreifen können, oder verwenden Sie " \* ", um den Zugriff von einer beliebigen Website aus zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="46dad-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-137">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="46dad-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="46dad-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="46dad-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="46dad-139">Der URI des vom Kunden verwalteten Schlüssels für die Sicherungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="46dad-139">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-140">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="46dad-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="46dad-141">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="46dad-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46dad-142">-DefaultProfile</span></span>
<span data-ttu-id="46dad-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46dad-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46dad-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="46dad-144">-DisableCorsCredential</span></span>
<span data-ttu-id="46dad-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span><span class="sxs-lookup"><span data-stu-id="46dad-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="46dad-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="46dad-147">Deaktivieren Sie verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="46dad-147">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="46dad-148">-DisableSmartProxy</span></span>
<span data-ttu-id="46dad-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="46dad-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="46dad-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="46dad-151">Aktivieren sie verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="46dad-151">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="46dad-152">-EnableSmartProxy</span></span>
<span data-ttu-id="46dad-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="46dad-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="46dad-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="46dad-155">HealthcareApis Fhir Service Export Storage Account Name.</span><span class="sxs-lookup"><span data-stu-id="46dad-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46dad-156">-InputObject</span></span>
<span data-ttu-id="46dad-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="46dad-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-158">-Name</span><span class="sxs-lookup"><span data-stu-id="46dad-158">-Name</span></span>
<span data-ttu-id="46dad-159">Name des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="46dad-159">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="46dad-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="46dad-161">Der Netzwerkzugriffstyp für den Dienst "Fhir".</span><span class="sxs-lookup"><span data-stu-id="46dad-161">The network access type for Fhir service.</span></span> <span data-ttu-id="46dad-162">Häufig `Enabled` oder `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="46dad-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46dad-163">-ResourceGroupName</span></span>
<span data-ttu-id="46dad-164">Name der HealthcareApis Service Resource Group.</span><span class="sxs-lookup"><span data-stu-id="46dad-164">HealthcareApis Service Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46dad-165">-ResourceId</span></span>
<span data-ttu-id="46dad-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="46dad-166">HealthcareApis Fhir Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="46dad-167">-Tag</span></span>
<span data-ttu-id="46dad-168">HealthcareApis Fhir Service Account Tags.</span><span class="sxs-lookup"><span data-stu-id="46dad-168">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46dad-169">-Confirm</span></span>
<span data-ttu-id="46dad-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46dad-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46dad-171">-WhatIf</span></span>
<span data-ttu-id="46dad-172">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46dad-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46dad-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46dad-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46dad-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46dad-174">CommonParameters</span></span>
<span data-ttu-id="46dad-175">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46dad-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46dad-176">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46dad-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46dad-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46dad-177">INPUTS</span></span>

### <span data-ttu-id="46dad-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="46dad-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="46dad-179">System.String</span><span class="sxs-lookup"><span data-stu-id="46dad-179">System.String</span></span>

## <span data-ttu-id="46dad-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46dad-180">OUTPUTS</span></span>

### <span data-ttu-id="46dad-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="46dad-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="46dad-182">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46dad-182">NOTES</span></span>

## <span data-ttu-id="46dad-183">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46dad-183">RELATED LINKS</span></span>
