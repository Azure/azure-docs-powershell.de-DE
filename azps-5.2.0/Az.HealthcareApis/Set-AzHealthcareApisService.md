---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296278"
---
# <span data-ttu-id="4df0e-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="4df0e-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="4df0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df0e-102">SYNOPSIS</span></span>
<span data-ttu-id="4df0e-103">Aktualisiert einen vorhandenen Dienst für Gesundheitswesensapis.</span><span class="sxs-lookup"><span data-stu-id="4df0e-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="4df0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4df0e-104">SYNTAX</span></span>

### <span data-ttu-id="4df0e-105">ServiceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4df0e-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4df0e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4df0e-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4df0e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4df0e-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df0e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4df0e-108">DESCRIPTION</span></span>
<span data-ttu-id="4df0e-109">Aktualisiert einen vorhandenen Dienst für Gesundheitswesensapis.</span><span class="sxs-lookup"><span data-stu-id="4df0e-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="4df0e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4df0e-110">EXAMPLES</span></span>

### <span data-ttu-id="4df0e-111">Beispiel 1: Aktualisiert den vorhandenen Dienst "MyService" im Gesundheitswesen in der Ressourcengruppe "MyResourceGroup" mit dem "durchsdb OfferThroughput = 500".</span><span class="sxs-lookup"><span data-stu-id="4df0e-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="4df0e-112">Beispiel 2: Aktualisiert den vorhandenen Dienst "MyService" im Gesundheitswesen in der Ressourcengruppe "MyResourceGroup" mit dem "aktualisierungsdb OfferThroughput = 500" und dem Schlüsseltresorschlüssel -URI "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="4df0e-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

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

## <span data-ttu-id="4df0e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df0e-113">PARAMETERS</span></span>

### <span data-ttu-id="4df0e-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="4df0e-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="4df0e-115">Liste der Access-Richtlinienobjekt-IDs.</span><span class="sxs-lookup"><span data-stu-id="4df0e-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="4df0e-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="4df0e-116">-AllowCorsCredential</span></span>
<span data-ttu-id="4df0e-117">HealthcareApis F vorbestellenService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="4df0e-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="4df0e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4df0e-118">-AsJob</span></span>
<span data-ttu-id="4df0e-119">Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="4df0e-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="4df0e-120">-Audience</span><span class="sxs-lookup"><span data-stu-id="4df0e-120">-Audience</span></span>
<span data-ttu-id="4df0e-121">HealthcareApis FserviceService Audience.</span><span class="sxs-lookup"><span data-stu-id="4df0e-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="4df0e-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="4df0e-122">-Authority</span></span>
<span data-ttu-id="4df0e-123">HealthcareApis F vor dem Gesundheitswesen.</span><span class="sxs-lookup"><span data-stu-id="4df0e-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="4df0e-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="4df0e-124">-CorsHeader</span></span>
<span data-ttu-id="4df0e-125">HealthcareApis F vordienst-Liste der Kors-Kopfzeilen.</span><span class="sxs-lookup"><span data-stu-id="4df0e-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="4df0e-126">Geben Sie die HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4df0e-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="4df0e-127">Verwenden Sie " \* " für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="4df0e-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="4df0e-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="4df0e-128">-CorsMaxAge</span></span>
<span data-ttu-id="4df0e-129">HealthcareApis FserviceService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="4df0e-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="4df0e-130">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4df0e-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="4df0e-131">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="4df0e-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="4df0e-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="4df0e-132">-CorsMethod</span></span>
<span data-ttu-id="4df0e-133">HealthcareApis F vordienst-Liste der Methoden von "Cors".</span><span class="sxs-lookup"><span data-stu-id="4df0e-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="4df0e-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="4df0e-134">-CorsOrigin</span></span>
<span data-ttu-id="4df0e-135">HealthcareApis Fservice List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="4df0e-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="4df0e-136">Geben Sie URLs von Ursprungswebsites an, die auf diese API zugreifen können, oder verwenden Sie " \* ", um den Zugriff von einer beliebigen Website aus zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="4df0e-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="4df0e-137">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="4df0e-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="4df0e-138">HealthcareApis F vor DienstschnursKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="4df0e-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="4df0e-139">Der URI des vom Kunden verwalteten Schlüssels für die Sicherungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="4df0e-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="4df0e-140">-UmspielersOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="4df0e-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="4df0e-141">HealthcareApis F vorÜberführungsservice AbtofferThroughput.</span><span class="sxs-lookup"><span data-stu-id="4df0e-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="4df0e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df0e-142">-DefaultProfile</span></span>
<span data-ttu-id="4df0e-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4df0e-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df0e-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="4df0e-144">-DisableCorsCredential</span></span>
<span data-ttu-id="4df0e-145">HealthcareApis F vorBelastetService CorsCredentials Not Allowed.</span><span class="sxs-lookup"><span data-stu-id="4df0e-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="4df0e-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4df0e-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="4df0e-147">"Verwaltete Identität deaktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="4df0e-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="4df0e-148">-DisableMethProxy</span><span class="sxs-lookup"><span data-stu-id="4df0e-148">-DisableSmartProxy</span></span>
<span data-ttu-id="4df0e-149">HealthcareApis F vor dem DeaktivierenBenachrichtigungsservice.</span><span class="sxs-lookup"><span data-stu-id="4df0e-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="4df0e-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4df0e-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="4df0e-151">"Verwaltete Identität aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="4df0e-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="4df0e-152">-EnableMethProxy</span><span class="sxs-lookup"><span data-stu-id="4df0e-152">-EnableSmartProxy</span></span>
<span data-ttu-id="4df0e-153">HealthcareApis FserviceService EnableApiProxy.</span><span class="sxs-lookup"><span data-stu-id="4df0e-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="4df0e-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4df0e-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="4df0e-155">Name des Dienstexportspeicherkontos für HealthcareApis F vor dem Exportdienst.</span><span class="sxs-lookup"><span data-stu-id="4df0e-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="4df0e-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4df0e-156">-InputObject</span></span>
<span data-ttu-id="4df0e-157">Der Dienst "HealthcareApis f vor" wird von "Get-AzHealthcareApisF beservice" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4df0e-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="4df0e-158">-Name</span><span class="sxs-lookup"><span data-stu-id="4df0e-158">-Name</span></span>
<span data-ttu-id="4df0e-159">Dienstname von HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="4df0e-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="4df0e-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="4df0e-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="4df0e-161">Der Netzwerkzugriffstyp für den Dienst "Fservice".</span><span class="sxs-lookup"><span data-stu-id="4df0e-161">The network access type for Fhir service.</span></span> <span data-ttu-id="4df0e-162">Häufig `Enabled` oder `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="4df0e-162">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="4df0e-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df0e-163">-ResourceGroupName</span></span>
<span data-ttu-id="4df0e-164">Name der Dienstressourcengruppe "Gesundheitswesen".</span><span class="sxs-lookup"><span data-stu-id="4df0e-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="4df0e-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4df0e-165">-ResourceId</span></span>
<span data-ttu-id="4df0e-166">HealthcareApis F vor dem Dienst "ResourceId".</span><span class="sxs-lookup"><span data-stu-id="4df0e-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="4df0e-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="4df0e-167">-Tag</span></span>
<span data-ttu-id="4df0e-168">Dienstkontotags für HealthcareApis F vor dem Dienst</span><span class="sxs-lookup"><span data-stu-id="4df0e-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="4df0e-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4df0e-169">-Confirm</span></span>
<span data-ttu-id="4df0e-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4df0e-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df0e-171">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4df0e-171">-WhatIf</span></span>
<span data-ttu-id="4df0e-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4df0e-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df0e-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4df0e-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df0e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df0e-174">CommonParameters</span></span>
<span data-ttu-id="4df0e-175">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df0e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df0e-176">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4df0e-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df0e-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4df0e-177">INPUTS</span></span>

### <span data-ttu-id="4df0e-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="4df0e-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="4df0e-179">System.String</span><span class="sxs-lookup"><span data-stu-id="4df0e-179">System.String</span></span>

## <span data-ttu-id="4df0e-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4df0e-180">OUTPUTS</span></span>

### <span data-ttu-id="4df0e-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="4df0e-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="4df0e-182">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4df0e-182">NOTES</span></span>

## <span data-ttu-id="4df0e-183">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4df0e-183">RELATED LINKS</span></span>
