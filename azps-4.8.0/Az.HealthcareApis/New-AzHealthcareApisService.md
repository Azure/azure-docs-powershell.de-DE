---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f5f8f00a2ab73485b4da6ad6df17ecf526c360bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175133"
---
# <span data-ttu-id="fc302-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="fc302-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="fc302-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc302-102">SYNOPSIS</span></span>
<span data-ttu-id="fc302-103">Erstellt die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="fc302-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="fc302-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc302-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-ExportStorageAccountName <String>] [-EnableSmartProxy] [-ManagedIdentity]
 [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc302-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc302-105">DESCRIPTION</span></span>
<span data-ttu-id="fc302-106">Erstellt oder aktualisiert die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="fc302-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="fc302-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc302-107">EXAMPLES</span></span>

### <span data-ttu-id="fc302-108">Beispiel 1: erstellt einen neuen Azure healthcareapis-fhir-Dienst mit dem Namen MyService in der Ressourcengruppe myresourcegroup an einem Speicherort westus2 mit cosmosdb Angebots Durchsatz = 400</span><span class="sxs-lookup"><span data-stu-id="fc302-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="fc302-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc302-109">PARAMETERS</span></span>

### <span data-ttu-id="fc302-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="fc302-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="fc302-111">Liste der Zugriffsrichtlinien-Objekt-IDs</span><span class="sxs-lookup"><span data-stu-id="fc302-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="fc302-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="fc302-112">-AllowCorsCredential</span></span>
<span data-ttu-id="fc302-113">HealthcareApis Fhir Service AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="fc302-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="fc302-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc302-114">-AsJob</span></span>
<span data-ttu-id="fc302-115">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="fc302-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="fc302-116">-Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="fc302-116">-Audience</span></span>
<span data-ttu-id="fc302-117">HealthcareApis Fhir Service-Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc302-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="fc302-118">-Authority</span><span class="sxs-lookup"><span data-stu-id="fc302-118">-Authority</span></span>
<span data-ttu-id="fc302-119">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="fc302-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="fc302-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="fc302-120">-CorsHeader</span></span>
<span data-ttu-id="fc302-121">HealthcareApis Fhir-Dienstliste der cors-Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="fc302-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="fc302-122">Geben Sie HTTP-Header an, die während der Anforderung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fc302-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="fc302-123">Verwenden Sie \* für jede Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="fc302-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="fc302-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="fc302-124">-CorsMaxAge</span></span>
<span data-ttu-id="fc302-125">HealthcareApis Fhir Service cors max age.</span><span class="sxs-lookup"><span data-stu-id="fc302-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="fc302-126">Geben Sie an, wie lange ein Ergebnis einer Anforderung in Sekunden zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc302-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="fc302-127">Beispiel: 600 bedeutet 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="fc302-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="fc302-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="fc302-128">-CorsMethod</span></span>
<span data-ttu-id="fc302-129">HealthcareApis Fhir-Dienstliste der cors-Methode.</span><span class="sxs-lookup"><span data-stu-id="fc302-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="fc302-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="fc302-130">-CorsOrigin</span></span>
<span data-ttu-id="fc302-131">HealthcareApis Fhir-Dienstliste mit cors Herkunft.</span><span class="sxs-lookup"><span data-stu-id="fc302-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="fc302-132">Geben Sie URLs von Ursprungs Websites an, die auf diese API zugreifen können, oder verwenden Sie \*, um von einer beliebigen Website aus Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fc302-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="fc302-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="fc302-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="fc302-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="fc302-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="fc302-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc302-135">-DefaultProfile</span></span>
<span data-ttu-id="fc302-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc302-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc302-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="fc302-137">-EnableSmartProxy</span></span>
<span data-ttu-id="fc302-138">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="fc302-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="fc302-139">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fc302-139">-ExportStorageAccountName</span></span>
<span data-ttu-id="fc302-140">Name des HealthcareApis-Fhir-Dienst Export speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fc302-140">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="fc302-141">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="fc302-141">-FhirVersion</span></span>
<span data-ttu-id="fc302-142">Fhir-Version.</span><span class="sxs-lookup"><span data-stu-id="fc302-142">Fhir Version.</span></span>

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

### <span data-ttu-id="fc302-143">-Art</span><span class="sxs-lookup"><span data-stu-id="fc302-143">-Kind</span></span>
<span data-ttu-id="fc302-144">Art des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="fc302-144">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="fc302-145">Der Standardwert ist Fhir</span><span class="sxs-lookup"><span data-stu-id="fc302-145">The default value is Fhir</span></span>

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

### <span data-ttu-id="fc302-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="fc302-146">-Location</span></span>
<span data-ttu-id="fc302-147">HealthcareApis-Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="fc302-147">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="fc302-148">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="fc302-148">-ManagedIdentity</span></span>
<span data-ttu-id="fc302-149">Verwaltete Identität verwenden?</span><span class="sxs-lookup"><span data-stu-id="fc302-149">Use Managed Identity?</span></span>

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

### <span data-ttu-id="fc302-150">-Name</span><span class="sxs-lookup"><span data-stu-id="fc302-150">-Name</span></span>
<span data-ttu-id="fc302-151">Name des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="fc302-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="fc302-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc302-152">-ResourceGroupName</span></span>
<span data-ttu-id="fc302-153">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc302-153">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc302-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc302-154">-Tag</span></span>
<span data-ttu-id="fc302-155">HealthcareApis Fhir-Dienstkonto Kategorien.</span><span class="sxs-lookup"><span data-stu-id="fc302-155">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="fc302-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc302-156">-Confirm</span></span>
<span data-ttu-id="fc302-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc302-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc302-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc302-158">-WhatIf</span></span>
<span data-ttu-id="fc302-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc302-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc302-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc302-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc302-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc302-161">CommonParameters</span></span>
<span data-ttu-id="fc302-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc302-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc302-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc302-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc302-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc302-164">INPUTS</span></span>

### <span data-ttu-id="fc302-165">System. String</span><span class="sxs-lookup"><span data-stu-id="fc302-165">System.String</span></span>

## <span data-ttu-id="fc302-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc302-166">OUTPUTS</span></span>

### <span data-ttu-id="fc302-167">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="fc302-167">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="fc302-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc302-168">NOTES</span></span>

## <span data-ttu-id="fc302-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc302-169">RELATED LINKS</span></span>
