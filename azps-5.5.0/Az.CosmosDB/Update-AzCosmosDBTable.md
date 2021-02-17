---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163956"
---
# <span data-ttu-id="55edc-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="55edc-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="55edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55edc-102">SYNOPSIS</span></span>
<span data-ttu-id="55edc-103">Aktualisiert die Tabelle "ÄnderungenDB".</span><span class="sxs-lookup"><span data-stu-id="55edc-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="55edc-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Tabelle gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="55edc-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="55edc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55edc-105">SYNTAX</span></span>

### <span data-ttu-id="55edc-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55edc-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55edc-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55edc-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55edc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55edc-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55edc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55edc-109">DESCRIPTION</span></span>
<span data-ttu-id="55edc-110">Aktualisiert die Tabelle "ÄnderungenDB".</span><span class="sxs-lookup"><span data-stu-id="55edc-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="55edc-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene Tabelle gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="55edc-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="55edc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55edc-112">EXAMPLES</span></span>

### <span data-ttu-id="55edc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55edc-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="55edc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55edc-114">PARAMETERS</span></span>

### <span data-ttu-id="55edc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55edc-115">-AccountName</span></span>
<span data-ttu-id="55edc-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="55edc-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55edc-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="55edc-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="55edc-118">Der maximale Durchsatzwert, wenn die Automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="55edc-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55edc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55edc-119">-Confirm</span></span>
<span data-ttu-id="55edc-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55edc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55edc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55edc-121">-DefaultProfile</span></span>
<span data-ttu-id="55edc-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55edc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55edc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55edc-123">-InputObject</span></span>
<span data-ttu-id="55edc-124">Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="55edc-124">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55edc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="55edc-125">-Name</span></span>
<span data-ttu-id="55edc-126">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="55edc-126">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55edc-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55edc-127">-ParentObject</span></span>
<span data-ttu-id="55edc-128">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="55edc-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55edc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55edc-129">-ResourceGroupName</span></span>
<span data-ttu-id="55edc-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55edc-130">Name of resource group.</span></span>

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

### <span data-ttu-id="55edc-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="55edc-131">-Throughput</span></span>
<span data-ttu-id="55edc-132">Der Durchsatz von Tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="55edc-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="55edc-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="55edc-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55edc-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55edc-134">-WhatIf</span></span>
<span data-ttu-id="55edc-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55edc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55edc-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55edc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55edc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55edc-137">CommonParameters</span></span>
<span data-ttu-id="55edc-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55edc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55edc-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55edc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55edc-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55edc-140">INPUTS</span></span>

### <span data-ttu-id="55edc-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="55edc-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="55edc-142">Microsoft.Azure.Commands.ExesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="55edc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="55edc-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55edc-143">OUTPUTS</span></span>

### <span data-ttu-id="55edc-144">Microsoft.Azure.Commands.ExesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="55edc-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="55edc-145">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="55edc-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="55edc-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55edc-146">NOTES</span></span>

## <span data-ttu-id="55edc-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55edc-147">RELATED LINKS</span></span>
