---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: a944982688dac8f9a28c10b3d26e71a8331451ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177580"
---
# <span data-ttu-id="49944-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="49944-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="49944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49944-102">SYNOPSIS</span></span>
<span data-ttu-id="49944-103">Aktualisiert einen vorhandenen healthcareApis-fhir-Dienst.</span><span class="sxs-lookup"><span data-stu-id="49944-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="49944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49944-104">SYNTAX</span></span>

### <span data-ttu-id="49944-105">ServiceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="49944-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49944-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49944-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity]
 [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49944-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49944-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49944-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49944-108">DESCRIPTION</span></span>
<span data-ttu-id="49944-109">Aktualisiert einen vorhandenen healthcareApis-fhir-Dienst.</span><span class="sxs-lookup"><span data-stu-id="49944-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="49944-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49944-110">EXAMPLES</span></span>

### <span data-ttu-id="49944-111">Beispiel 1: aktualisiert den vorhandenen healthcareapis-Dienst mit dem Namen MyService in der Ressourcengruppe myresourcegroup mit dem cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="49944-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="49944-112">Beispiel 2: aktualisiert den vorhandenen healthcareapis-Dienst mit dem Namen MyService in der Ressourcengruppe myresourcegroup mit dem cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="49944-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

## <span data-ttu-id="49944-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="49944-113">PARAMETERS</span></span>

### <span data-ttu-id="49944-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="49944-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="49944-115">Liste der Zugriffsrichtlinien-Objekt-IDs</span><span class="sxs-lookup"><span data-stu-id="49944-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="49944-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="49944-116">-AllowCorsCredential</span></span>
<span data-ttu-id="49944-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="49944-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="49944-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49944-118">-AsJob</span></span>
<span data-ttu-id="49944-119">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="49944-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="49944-120">-Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="49944-120">-Audience</span></span>
<span data-ttu-id="49944-121">HealthcareApis FhirService-Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="49944-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="49944-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="49944-122">-Authority</span></span>
<span data-ttu-id="49944-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="49944-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="49944-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="49944-124">-CorsHeader</span></span>
<span data-ttu-id="49944-125">HealthcareApis Fhir-Dienstliste der cors-Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="49944-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="49944-126">Geben Sie HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="49944-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="49944-127">Verwenden Sie \* für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="49944-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="49944-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="49944-128">-CorsMaxAge</span></span>
<span data-ttu-id="49944-129">HealthcareApis Fhir Service cors max age.</span><span class="sxs-lookup"><span data-stu-id="49944-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="49944-130">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="49944-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="49944-131">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="49944-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="49944-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="49944-132">-CorsMethod</span></span>
<span data-ttu-id="49944-133">HealthcareApis FhirService-Liste der cors-Methoden.</span><span class="sxs-lookup"><span data-stu-id="49944-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="49944-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="49944-134">-CorsOrigin</span></span>
<span data-ttu-id="49944-135">HealthcareApis FhirService cors Origins.</span><span class="sxs-lookup"><span data-stu-id="49944-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="49944-136">HealthcareApis Fhir-Dienstliste mit cors Herkunft.</span><span class="sxs-lookup"><span data-stu-id="49944-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="49944-137">Geben Sie URLs von Ursprungs Websites an, die auf diese API zugreifen können, oder verwenden Sie \*, um von einer beliebigen Website aus Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="49944-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="49944-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="49944-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="49944-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="49944-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="49944-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49944-140">-DefaultProfile</span></span>
<span data-ttu-id="49944-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49944-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49944-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="49944-142">-DisableCorsCredential</span></span>
<span data-ttu-id="49944-143">HealthcareApis FhirService CorsCredentials nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="49944-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="49944-144">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="49944-144">-DisableManagedIdentity</span></span>
<span data-ttu-id="49944-145">Deaktivieren der verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="49944-145">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="49944-146">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="49944-146">-DisableSmartProxy</span></span>
<span data-ttu-id="49944-147">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="49944-147">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="49944-148">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="49944-148">-EnableManagedIdentity</span></span>
<span data-ttu-id="49944-149">Aktivieren der verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="49944-149">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="49944-150">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="49944-150">-EnableSmartProxy</span></span>
<span data-ttu-id="49944-151">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="49944-151">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="49944-152">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="49944-152">-ExportStorageAccountName</span></span>
<span data-ttu-id="49944-153">Name des HealthcareApis-Fhir-Dienst Export speicherkontos</span><span class="sxs-lookup"><span data-stu-id="49944-153">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="49944-154">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="49944-154">-InputObject</span></span>
<span data-ttu-id="49944-155">HealthcareApis fhir-Dienst, der von Get-AzHealthcareApisFhirService geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="49944-155">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="49944-156">-Name</span><span class="sxs-lookup"><span data-stu-id="49944-156">-Name</span></span>
<span data-ttu-id="49944-157">Name des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="49944-157">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="49944-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49944-158">-ResourceGroupName</span></span>
<span data-ttu-id="49944-159">Name der HealthcareApis-Dienst Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="49944-159">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="49944-160">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="49944-160">-ResourceId</span></span>
<span data-ttu-id="49944-161">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="49944-161">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="49944-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="49944-162">-Tag</span></span>
<span data-ttu-id="49944-163">HealthcareApis Fhir-Dienstkonto Kategorien.</span><span class="sxs-lookup"><span data-stu-id="49944-163">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="49944-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49944-164">-Confirm</span></span>
<span data-ttu-id="49944-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49944-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49944-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49944-166">-WhatIf</span></span>
<span data-ttu-id="49944-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49944-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49944-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49944-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49944-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49944-169">CommonParameters</span></span>
<span data-ttu-id="49944-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49944-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49944-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49944-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49944-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49944-172">INPUTS</span></span>

### <span data-ttu-id="49944-173">System. String</span><span class="sxs-lookup"><span data-stu-id="49944-173">System.String</span></span>

### <span data-ttu-id="49944-174">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="49944-174">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="49944-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49944-175">OUTPUTS</span></span>

### <span data-ttu-id="49944-176">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="49944-176">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="49944-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="49944-177">NOTES</span></span>

## <span data-ttu-id="49944-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49944-178">RELATED LINKS</span></span>
