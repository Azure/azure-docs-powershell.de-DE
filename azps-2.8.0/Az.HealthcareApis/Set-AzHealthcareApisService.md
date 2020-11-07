---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 36632398d95acdd16d2a7b41c09bed7172391639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651012"
---
# <span data-ttu-id="1edaf-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="1edaf-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="1edaf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1edaf-102">SYNOPSIS</span></span>
<span data-ttu-id="1edaf-103">Aktualisiert einen vorhandenen healthcareApis-fhir-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1edaf-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="1edaf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1edaf-104">SYNTAX</span></span>

### <span data-ttu-id="1edaf-105">ServiceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1edaf-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1edaf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1edaf-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1edaf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1edaf-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1edaf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1edaf-108">DESCRIPTION</span></span>
<span data-ttu-id="1edaf-109">Aktualisiert einen vorhandenen healthcareApis-fhir-Dienst.</span><span class="sxs-lookup"><span data-stu-id="1edaf-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="1edaf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1edaf-110">EXAMPLES</span></span>

### <span data-ttu-id="1edaf-111">Beispiel 1: aktualisiert den vorhandenen healthcareapis-Dienst mit dem Namen MyService in der Ressourcengruppe myresourcegroup mit dem cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="1edaf-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="1edaf-112">Beispiel 2: aktualisiert den vorhandenen healthcareapis-Dienst mit dem Namen MyService in der Ressourcengruppe myresourcegroup mit dem cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="1edaf-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="1edaf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1edaf-113">PARAMETERS</span></span>

### <span data-ttu-id="1edaf-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="1edaf-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="1edaf-115">Liste der Zugriffsrichtlinien-Objekt-IDs</span><span class="sxs-lookup"><span data-stu-id="1edaf-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="1edaf-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="1edaf-116">-AllowCorsCredential</span></span>
<span data-ttu-id="1edaf-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="1edaf-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="1edaf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1edaf-118">-AsJob</span></span>
<span data-ttu-id="1edaf-119">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="1edaf-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="1edaf-120">-Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="1edaf-120">-Audience</span></span>
<span data-ttu-id="1edaf-121">HealthcareApis FhirService-Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="1edaf-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="1edaf-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="1edaf-122">-Authority</span></span>
<span data-ttu-id="1edaf-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="1edaf-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="1edaf-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="1edaf-124">-CorsHeader</span></span>
<span data-ttu-id="1edaf-125">HealthcareApis Fhir-Dienstliste der cors-Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="1edaf-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="1edaf-126">Geben Sie HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1edaf-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="1edaf-127">Verwenden Sie \* für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="1edaf-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="1edaf-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="1edaf-128">-CorsMaxAge</span></span>
<span data-ttu-id="1edaf-129">HealthcareApis Fhir Service cors max age.</span><span class="sxs-lookup"><span data-stu-id="1edaf-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="1edaf-130">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1edaf-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="1edaf-131">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="1edaf-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="1edaf-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="1edaf-132">-CorsMethod</span></span>
<span data-ttu-id="1edaf-133">HealthcareApis FhirService-Liste der cors-Methoden.</span><span class="sxs-lookup"><span data-stu-id="1edaf-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edaf-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="1edaf-134">-CorsOrigin</span></span>
<span data-ttu-id="1edaf-135">HealthcareApis FhirService cors Origins.</span><span class="sxs-lookup"><span data-stu-id="1edaf-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="1edaf-136">HealthcareApis Fhir-Dienstliste mit cors Herkunft.</span><span class="sxs-lookup"><span data-stu-id="1edaf-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="1edaf-137">Geben Sie URLs von Ursprungs Websites an, die auf diese API zugreifen können, oder verwenden Sie \*, um von einer beliebigen Website aus Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1edaf-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="1edaf-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="1edaf-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="1edaf-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="1edaf-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="1edaf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1edaf-140">-DefaultProfile</span></span>
<span data-ttu-id="1edaf-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1edaf-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1edaf-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="1edaf-142">-DisableCorsCredential</span></span>
<span data-ttu-id="1edaf-143">HealthcareApis FhirService CorsCredentials nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1edaf-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="1edaf-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="1edaf-144">-DisableSmartProxy</span></span>
<span data-ttu-id="1edaf-145">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="1edaf-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="1edaf-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="1edaf-146">-EnableSmartProxy</span></span>
<span data-ttu-id="1edaf-147">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="1edaf-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="1edaf-148">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1edaf-148">-InputObject</span></span>
<span data-ttu-id="1edaf-149">HealthcareApis fhir-Dienst, der von Get-AzHealthcareApisFhirService geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1edaf-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="1edaf-150">-Name</span><span class="sxs-lookup"><span data-stu-id="1edaf-150">-Name</span></span>
<span data-ttu-id="1edaf-151">Name des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="1edaf-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="1edaf-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1edaf-152">-ResourceGroupName</span></span>
<span data-ttu-id="1edaf-153">Name der HealthcareApis-Dienst Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1edaf-153">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="1edaf-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1edaf-154">-ResourceId</span></span>
<span data-ttu-id="1edaf-155">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="1edaf-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="1edaf-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="1edaf-156">-Tag</span></span>
<span data-ttu-id="1edaf-157">HealthcareApis Fhir-Dienstkonto Kategorien.</span><span class="sxs-lookup"><span data-stu-id="1edaf-157">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="1edaf-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1edaf-158">-Confirm</span></span>
<span data-ttu-id="1edaf-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1edaf-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1edaf-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1edaf-160">-WhatIf</span></span>
<span data-ttu-id="1edaf-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1edaf-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1edaf-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1edaf-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1edaf-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1edaf-163">CommonParameters</span></span>
<span data-ttu-id="1edaf-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1edaf-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1edaf-165">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1edaf-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1edaf-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1edaf-166">INPUTS</span></span>

### <span data-ttu-id="1edaf-167">System. String</span><span class="sxs-lookup"><span data-stu-id="1edaf-167">System.String</span></span>

### <span data-ttu-id="1edaf-168">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="1edaf-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="1edaf-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1edaf-169">OUTPUTS</span></span>

### <span data-ttu-id="1edaf-170">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="1edaf-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="1edaf-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="1edaf-171">NOTES</span></span>

## <span data-ttu-id="1edaf-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1edaf-172">RELATED LINKS</span></span>
