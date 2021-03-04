---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: e99c060cc7446cbecc46040ec4a498cf9f545e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949203"
---
# <span data-ttu-id="0b9ec-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0b9ec-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="0b9ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9ec-103">Erstellt die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="0b9ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b9ec-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b9ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="0b9ec-106">Erstellt oder aktualisiert die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="0b9ec-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="0b9ec-108">Beispiel 1: Erstellt einen neuen Azure Healthcareapis-Fhir-Dienst mit dem Namen MyService in der Ressourcengruppe MyResourceGroup an einem Speicherort westus2 mit dem Angebotsdurchsatz von cosmosdb = 400</span><span class="sxs-lookup"><span data-stu-id="0b9ec-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
CosmosDbOfferThroughput : 400
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

### <span data-ttu-id="0b9ec-109">Beispiel 2: Erstellt einen neuen Azure Healthcareapis-Fhir-Dienst mit dem Namen MyService in der Ressourcengruppe MyResourceGroup an einem Speicherort westus2 mit cosmosdb offer throughput = 400 und key vault key uri "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="0b9ec-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 400
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

## <span data-ttu-id="0b9ec-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="0b9ec-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="0b9ec-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="0b9ec-112">Liste der Access-Richtlinienobjekt-IDs.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="0b9ec-113">-AllowCorsCredential</span></span>
<span data-ttu-id="0b9ec-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="0b9ec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b9ec-115">-AsJob</span></span>
<span data-ttu-id="0b9ec-116">Führen Sie das Cmdlet als Auftrag im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="0b9ec-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="0b9ec-117">-Audience</span></span>
<span data-ttu-id="0b9ec-118">HealthcareApis Fhir Service Audience.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="0b9ec-119">-Autorität</span><span class="sxs-lookup"><span data-stu-id="0b9ec-119">-Authority</span></span>
<span data-ttu-id="0b9ec-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="0b9ec-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="0b9ec-121">-CorsHeader</span></span>
<span data-ttu-id="0b9ec-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="0b9ec-123">Geben Sie HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="0b9ec-124">Verwenden Sie " \* " für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="0b9ec-125">-CorsMaxAge</span></span>
<span data-ttu-id="0b9ec-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="0b9ec-127">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="0b9ec-128">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="0b9ec-129">-CorsMethod</span></span>
<span data-ttu-id="0b9ec-130">HealthcareApis Fhir Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="0b9ec-131">-CorsOrigin</span></span>
<span data-ttu-id="0b9ec-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="0b9ec-133">Geben Sie URLs von Ursprungswebsites an, die auf diese API zugreifen können, oder verwenden Sie " \* ", um den Zugriff von einer beliebigen Website aus zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="0b9ec-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="0b9ec-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="0b9ec-136">Der URI des vom Kunden verwalteten Schlüssels für die Sicherungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="0b9ec-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="0b9ec-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="0b9ec-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9ec-139">-DefaultProfile</span></span>
<span data-ttu-id="0b9ec-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b9ec-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="0b9ec-141">-EnableSmartProxy</span></span>
<span data-ttu-id="0b9ec-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="0b9ec-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b9ec-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="0b9ec-144">HealthcareApis Fhir Service Export Storage Account Name.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="0b9ec-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="0b9ec-145">-FhirVersion</span></span>
<span data-ttu-id="0b9ec-146">Fhir-Version.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-146">Fhir Version.</span></span>

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

### <span data-ttu-id="0b9ec-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="0b9ec-147">-Kind</span></span>
<span data-ttu-id="0b9ec-148">Art des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="0b9ec-149">Der Standardwert ist "Fhir".</span><span class="sxs-lookup"><span data-stu-id="0b9ec-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="0b9ec-150">-Location</span><span class="sxs-lookup"><span data-stu-id="0b9ec-150">-Location</span></span>
<span data-ttu-id="0b9ec-151">HealthcareApis Service Location.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0b9ec-152">-ManagedIdentity</span></span>
<span data-ttu-id="0b9ec-153">Verwenden Sie verwaltete Identität?</span><span class="sxs-lookup"><span data-stu-id="0b9ec-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="0b9ec-154">-Name</span><span class="sxs-lookup"><span data-stu-id="0b9ec-154">-Name</span></span>
<span data-ttu-id="0b9ec-155">Name des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0b9ec-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="0b9ec-157">Der Netzwerkzugriffstyp für den Dienst "Fhir".</span><span class="sxs-lookup"><span data-stu-id="0b9ec-157">The network access type for Fhir service.</span></span> <span data-ttu-id="0b9ec-158">Häufig `Enabled` oder `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="0b9ec-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9ec-159">-ResourceGroupName</span></span>
<span data-ttu-id="0b9ec-160">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b9ec-161">-Tag</span></span>
<span data-ttu-id="0b9ec-162">HealthcareApis Fhir Service Account Tags.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b9ec-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b9ec-163">-Confirm</span></span>
<span data-ttu-id="0b9ec-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b9ec-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b9ec-165">-WhatIf</span></span>
<span data-ttu-id="0b9ec-166">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b9ec-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b9ec-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9ec-168">CommonParameters</span></span>
<span data-ttu-id="0b9ec-169">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b9ec-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9ec-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b9ec-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9ec-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b9ec-171">INPUTS</span></span>

### <span data-ttu-id="0b9ec-172">System.String</span><span class="sxs-lookup"><span data-stu-id="0b9ec-172">System.String</span></span>

## <span data-ttu-id="0b9ec-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b9ec-173">OUTPUTS</span></span>

### <span data-ttu-id="0b9ec-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0b9ec-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="0b9ec-175">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b9ec-175">NOTES</span></span>

## <span data-ttu-id="0b9ec-176">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b9ec-176">RELATED LINKS</span></span>
