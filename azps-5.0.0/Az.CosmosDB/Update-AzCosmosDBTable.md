---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298972"
---
# <span data-ttu-id="d4baf-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="d4baf-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="d4baf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4baf-102">SYNOPSIS</span></span>
<span data-ttu-id="d4baf-103">Aktualisiert die CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d4baf-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="d4baf-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="d4baf-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="d4baf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4baf-105">SYNTAX</span></span>

### <span data-ttu-id="d4baf-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4baf-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4baf-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4baf-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4baf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4baf-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4baf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4baf-109">DESCRIPTION</span></span>
<span data-ttu-id="d4baf-110">Aktualisiert die CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d4baf-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="d4baf-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="d4baf-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="d4baf-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4baf-112">EXAMPLES</span></span>

### <span data-ttu-id="d4baf-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4baf-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="d4baf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4baf-114">PARAMETERS</span></span>

### <span data-ttu-id="d4baf-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d4baf-115">-AccountName</span></span>
<span data-ttu-id="d4baf-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="d4baf-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d4baf-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d4baf-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d4baf-118">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4baf-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d4baf-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4baf-119">-Confirm</span></span>
<span data-ttu-id="d4baf-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4baf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4baf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4baf-121">-DefaultProfile</span></span>
<span data-ttu-id="d4baf-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4baf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4baf-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4baf-123">-InputObject</span></span>
<span data-ttu-id="d4baf-124">Table-Objekt</span><span class="sxs-lookup"><span data-stu-id="d4baf-124">Table Object.</span></span>

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

### <span data-ttu-id="d4baf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d4baf-125">-Name</span></span>
<span data-ttu-id="d4baf-126">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d4baf-126">Name of the Table.</span></span>

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

### <span data-ttu-id="d4baf-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d4baf-127">-ParentObject</span></span>
<span data-ttu-id="d4baf-128">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d4baf-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d4baf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4baf-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4baf-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4baf-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d4baf-131">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="d4baf-131">-Throughput</span></span>
<span data-ttu-id="d4baf-132">Der Durchsatz der Tabelle (ru/s).</span><span class="sxs-lookup"><span data-stu-id="d4baf-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="d4baf-133">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="d4baf-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d4baf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4baf-134">-WhatIf</span></span>
<span data-ttu-id="d4baf-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4baf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4baf-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4baf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4baf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4baf-137">CommonParameters</span></span>
<span data-ttu-id="d4baf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4baf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4baf-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4baf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4baf-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4baf-140">INPUTS</span></span>

### <span data-ttu-id="d4baf-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d4baf-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="d4baf-142">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d4baf-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="d4baf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4baf-143">OUTPUTS</span></span>

### <span data-ttu-id="d4baf-144">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d4baf-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="d4baf-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d4baf-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d4baf-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4baf-146">NOTES</span></span>

## <span data-ttu-id="d4baf-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4baf-147">RELATED LINKS</span></span>
