---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163500"
---
# <span data-ttu-id="00fb4-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="00fb4-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="00fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="00fb4-103">Erstellt die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="00fb4-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="00fb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00fb4-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00fb4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="00fb4-106">Erstellt oder aktualisiert die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="00fb4-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="00fb4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00fb4-107">EXAMPLES</span></span>

### <span data-ttu-id="00fb4-108">Beispiel 1: Erstellt einen neuen Dienst für Azure-Gesundheitswesenapis mit dem Namen "MyService" in der Ressourcengruppe "MyResourceGroup" an einem Speicherort "westus2" mit einem Durchsatz für das Angebot "Durchsatz" = 400.</span><span class="sxs-lookup"><span data-stu-id="00fb4-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

### <span data-ttu-id="00fb4-109">Beispiel 2: Erstellt einen neuen Dienst für Azure-Gesundheitswesenapis mit dem Namen "MyService" in der Ressourcengruppe "MyResourceGroup" an einem Speicherort "westus2" mit einem Durchsatz des Abonnements "400" und dem Schlüsseltresorschlüssel-URI "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="00fb4-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
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

## <span data-ttu-id="00fb4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00fb4-110">PARAMETERS</span></span>

### <span data-ttu-id="00fb4-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="00fb4-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="00fb4-112">Liste der Access-Richtlinienobjekt-IDs.</span><span class="sxs-lookup"><span data-stu-id="00fb4-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="00fb4-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="00fb4-113">-AllowCorsCredential</span></span>
<span data-ttu-id="00fb4-114">HealthcareApis F vor dem Dienst AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="00fb4-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="00fb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00fb4-115">-AsJob</span></span>
<span data-ttu-id="00fb4-116">Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="00fb4-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="00fb4-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="00fb4-117">-Audience</span></span>
<span data-ttu-id="00fb4-118">Gesundheitswesen ( Dienstpublikum)</span><span class="sxs-lookup"><span data-stu-id="00fb4-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="00fb4-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="00fb4-119">-Authority</span></span>
<span data-ttu-id="00fb4-120">HealthcareApis F vor dem Dienst.</span><span class="sxs-lookup"><span data-stu-id="00fb4-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="00fb4-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="00fb4-121">-CorsHeader</span></span>
<span data-ttu-id="00fb4-122">HealthcareApis F vor der Dienstliste von "Cors Header".</span><span class="sxs-lookup"><span data-stu-id="00fb4-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="00fb4-123">Geben Sie die HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="00fb4-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="00fb4-124">Verwenden Sie " \* " für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="00fb4-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="00fb4-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="00fb4-125">-CorsMaxAge</span></span>
<span data-ttu-id="00fb4-126">HealthcareApis F vorn (Service Cors Max Age).</span><span class="sxs-lookup"><span data-stu-id="00fb4-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="00fb4-127">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="00fb4-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="00fb4-128">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="00fb4-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="00fb4-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="00fb4-129">-CorsMethod</span></span>
<span data-ttu-id="00fb4-130">HealthcareApis F ben Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="00fb4-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="00fb4-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="00fb4-131">-CorsOrigin</span></span>
<span data-ttu-id="00fb4-132">HealthcareApis F vor der Dienstliste von "Cors Origin".</span><span class="sxs-lookup"><span data-stu-id="00fb4-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="00fb4-133">Geben Sie URLs von Ursprungswebsites an, die auf diese API zugreifen können, oder verwenden Sie " \* ", um den Zugriff von einer beliebigen Website aus zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="00fb4-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="00fb4-134">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="00fb4-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="00fb4-135">HealthcareApis F vor DienstschnurenKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="00fb4-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="00fb4-136">Der URI des vom Kunden verwalteten Schlüssels für die Sicherungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="00fb4-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="00fb4-137">-UmspielersOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="00fb4-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="00fb4-138">HealthcareApis F vor DienstdingenOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="00fb4-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="00fb4-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fb4-139">-DefaultProfile</span></span>
<span data-ttu-id="00fb4-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00fb4-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00fb4-141">-EnableMethProxy</span><span class="sxs-lookup"><span data-stu-id="00fb4-141">-EnableSmartProxy</span></span>
<span data-ttu-id="00fb4-142">HealthcareApis F vor dem Dienst EnableApiProxy.</span><span class="sxs-lookup"><span data-stu-id="00fb4-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="00fb4-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="00fb4-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="00fb4-144">Name des Dienstexportspeicherkontos für HealthcareApis F vor dem Exportdienst.</span><span class="sxs-lookup"><span data-stu-id="00fb4-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="00fb4-145">-F vor Kehrversion</span><span class="sxs-lookup"><span data-stu-id="00fb4-145">-FhirVersion</span></span>
<span data-ttu-id="00fb4-146">F vor.</span><span class="sxs-lookup"><span data-stu-id="00fb4-146">Fhir Version.</span></span>

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

### <span data-ttu-id="00fb4-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="00fb4-147">-Kind</span></span>
<span data-ttu-id="00fb4-148">Art des Diensts "Gesundheitswesen".</span><span class="sxs-lookup"><span data-stu-id="00fb4-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="00fb4-149">Der Standardwert ist "F be"</span><span class="sxs-lookup"><span data-stu-id="00fb4-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="00fb4-150">-Location</span><span class="sxs-lookup"><span data-stu-id="00fb4-150">-Location</span></span>
<span data-ttu-id="00fb4-151">Dienststandort im Gesundheitswesen.</span><span class="sxs-lookup"><span data-stu-id="00fb4-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="00fb4-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="00fb4-152">-ManagedIdentity</span></span>
<span data-ttu-id="00fb4-153">Verwaltete Identität verwenden?</span><span class="sxs-lookup"><span data-stu-id="00fb4-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="00fb4-154">-Name</span><span class="sxs-lookup"><span data-stu-id="00fb4-154">-Name</span></span>
<span data-ttu-id="00fb4-155">Dienstname von HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="00fb4-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="00fb4-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="00fb4-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="00fb4-157">Der Netzwerkzugriffstyp für den Dienst "Fservice".</span><span class="sxs-lookup"><span data-stu-id="00fb4-157">The network access type for Fhir service.</span></span> <span data-ttu-id="00fb4-158">Häufig `Enabled` oder `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="00fb4-158">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="00fb4-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fb4-159">-ResourceGroupName</span></span>
<span data-ttu-id="00fb4-160">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="00fb4-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="00fb4-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="00fb4-161">-Tag</span></span>
<span data-ttu-id="00fb4-162">Dienstkontotags für HealthcareApis F vor dem Dienst</span><span class="sxs-lookup"><span data-stu-id="00fb4-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="00fb4-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00fb4-163">-Confirm</span></span>
<span data-ttu-id="00fb4-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00fb4-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fb4-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="00fb4-165">-WhatIf</span></span>
<span data-ttu-id="00fb4-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00fb4-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fb4-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00fb4-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fb4-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fb4-168">CommonParameters</span></span>
<span data-ttu-id="00fb4-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fb4-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fb4-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00fb4-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fb4-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00fb4-171">INPUTS</span></span>

### <span data-ttu-id="00fb4-172">System.String</span><span class="sxs-lookup"><span data-stu-id="00fb4-172">System.String</span></span>

## <span data-ttu-id="00fb4-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00fb4-173">OUTPUTS</span></span>

### <span data-ttu-id="00fb4-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="00fb4-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="00fb4-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="00fb4-175">NOTES</span></span>

## <span data-ttu-id="00fb4-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="00fb4-176">RELATED LINKS</span></span>
