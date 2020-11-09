---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299097"
---
# <span data-ttu-id="55b05-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="55b05-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="55b05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55b05-102">SYNOPSIS</span></span>
<span data-ttu-id="55b05-103">Aktualisieren von Bereichen eines CosmosDB-Kontos</span><span class="sxs-lookup"><span data-stu-id="55b05-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="55b05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55b05-104">SYNTAX</span></span>

### <span data-ttu-id="55b05-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55b05-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55b05-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55b05-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55b05-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55b05-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b05-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55b05-108">DESCRIPTION</span></span>
<span data-ttu-id="55b05-109">Aktualisieren von Bereichen eines CosmosDB-Kontos</span><span class="sxs-lookup"><span data-stu-id="55b05-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="55b05-110">Der Speicherort kann entweder als Objekt vom Typ PSLocation oder als Zeichenfolgen mit dem Positionsnamen angegeben werden, die nach der Failover-Priorität geordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55b05-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="55b05-111">Der locationobject-Parameter erwartet, dass die Liste der aktuellen Speicherorte (einschließlich der Failover-prioritiies) vom neuen LocationObjects entsprechend den neuen Speicherorten angefügt wird, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55b05-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="55b05-112">Location-Parameter erwartet die Liste des aktuellen Speicherorts (geordnet nach Failover-Priorität) und den neuen Speicherorten.</span><span class="sxs-lookup"><span data-stu-id="55b05-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="55b05-113">Bitte beachten Sie, dass wir nur das Hinzufügen von Regionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="55b05-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="55b05-114">Geben Sie entweder Location oder locationobject an.</span><span class="sxs-lookup"><span data-stu-id="55b05-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="55b05-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55b05-115">EXAMPLES</span></span>

### <span data-ttu-id="55b05-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55b05-116">Example 1</span></span>
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

## <span data-ttu-id="55b05-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="55b05-117">PARAMETERS</span></span>

### <span data-ttu-id="55b05-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b05-118">-AsJob</span></span>
<span data-ttu-id="55b05-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55b05-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55b05-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55b05-120">-Confirm</span></span>
<span data-ttu-id="55b05-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55b05-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b05-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b05-122">-DefaultProfile</span></span>
<span data-ttu-id="55b05-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55b05-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b05-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55b05-124">-InputObject</span></span>
<span data-ttu-id="55b05-125">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="55b05-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="55b05-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="55b05-126">-Location</span></span>
<span data-ttu-id="55b05-127">Der Name des hinzuzufügenden Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="55b05-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="55b05-128">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="55b05-128">-LocationObject</span></span>
<span data-ttu-id="55b05-129">Fügen Sie dem Cosmos DB-Daten Bank Konto einen Speicherort hinzu.</span><span class="sxs-lookup"><span data-stu-id="55b05-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="55b05-130">Array von PSLocation-Objekten.</span><span class="sxs-lookup"><span data-stu-id="55b05-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="55b05-131">-Name</span><span class="sxs-lookup"><span data-stu-id="55b05-131">-Name</span></span>
<span data-ttu-id="55b05-132">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="55b05-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55b05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b05-133">-ResourceGroupName</span></span>
<span data-ttu-id="55b05-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55b05-134">Name of resource group.</span></span>

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

### <span data-ttu-id="55b05-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="55b05-135">-ResourceId</span></span>
<span data-ttu-id="55b05-136">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="55b05-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="55b05-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b05-137">-WhatIf</span></span>
<span data-ttu-id="55b05-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55b05-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b05-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55b05-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b05-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b05-140">CommonParameters</span></span>
<span data-ttu-id="55b05-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b05-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b05-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55b05-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b05-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55b05-143">INPUTS</span></span>

### <span data-ttu-id="55b05-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="55b05-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="55b05-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55b05-145">OUTPUTS</span></span>

### <span data-ttu-id="55b05-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="55b05-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="55b05-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="55b05-147">NOTES</span></span>

## <span data-ttu-id="55b05-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55b05-148">RELATED LINKS</span></span>
