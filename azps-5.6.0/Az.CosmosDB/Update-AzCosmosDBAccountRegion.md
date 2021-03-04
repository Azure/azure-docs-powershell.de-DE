---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: 643cdbf8aa0aed98dba7497fa0107d8d81583bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922032"
---
# <span data-ttu-id="3b1c0-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="3b1c0-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="3b1c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1c0-103">Aktualisieren von Regionen eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="3b1c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b1c0-104">SYNTAX</span></span>

### <span data-ttu-id="3b1c0-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b1c0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b1c0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1c0-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b1c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1c0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1c0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b1c0-108">DESCRIPTION</span></span>
<span data-ttu-id="3b1c0-109">Aktualisieren von Regionen eines CosmosDB-Kontos.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="3b1c0-110">Der Speicherort kann entweder als Objekt vom Typ PSLocation oder als Zeichenfolgen des Positionsnamens angegeben werden, die nach Failoverpriorität geordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="3b1c0-111">Der Parameter LocationObject erwartet, dass die Liste der aktuellen Speicherorte (eingeschlossene Failover prioritiies) von den neuen LocationObjects angefügt wird, die neuen Speicherorten entsprechend hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="3b1c0-112">Der Parameter Position erwartet die Liste der aktuellen Position (nach Failoverpriorität geordnet) und die neuen Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="3b1c0-113">Bitte beachten Sie, dass wir nur "Addition of Regions" unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="3b1c0-114">Geben Sie entweder "Ort" oder "LocationObject" an.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="3b1c0-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b1c0-115">EXAMPLES</span></span>

### <span data-ttu-id="3b1c0-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b1c0-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="3b1c0-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3b1c0-117">PARAMETERS</span></span>

### <span data-ttu-id="3b1c0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b1c0-118">-AsJob</span></span>
<span data-ttu-id="3b1c0-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3b1c0-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b1c0-120">-Confirm</span></span>
<span data-ttu-id="3b1c0-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1c0-122">-DefaultProfile</span></span>
<span data-ttu-id="3b1c0-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b1c0-124">-InputObject</span></span>
<span data-ttu-id="3b1c0-125">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-126">-Location</span><span class="sxs-lookup"><span data-stu-id="3b1c0-126">-Location</span></span>
<span data-ttu-id="3b1c0-127">Name des speicherorts, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="3b1c0-128">-LocationObject</span></span>
<span data-ttu-id="3b1c0-129">Fügen Sie dem Datenbankkonto "Cosmos DB" einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="3b1c0-130">Array von PSLocation-Objekten.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3b1c0-131">-Name</span></span>
<span data-ttu-id="3b1c0-132">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="3b1c0-132">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1c0-133">-ResourceGroupName</span></span>
<span data-ttu-id="3b1c0-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-134">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b1c0-135">-ResourceId</span></span>
<span data-ttu-id="3b1c0-136">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-136">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1c0-137">-WhatIf</span></span>
<span data-ttu-id="3b1c0-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b1c0-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1c0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1c0-140">CommonParameters</span></span>
<span data-ttu-id="3b1c0-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b1c0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1c0-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b1c0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1c0-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b1c0-143">INPUTS</span></span>

### <span data-ttu-id="3b1c0-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3b1c0-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3b1c0-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b1c0-145">OUTPUTS</span></span>

### <span data-ttu-id="3b1c0-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3b1c0-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3b1c0-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3b1c0-147">NOTES</span></span>

## <span data-ttu-id="3b1c0-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3b1c0-148">RELATED LINKS</span></span>
