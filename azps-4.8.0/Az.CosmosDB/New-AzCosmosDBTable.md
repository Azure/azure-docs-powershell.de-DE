---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167265"
---
# <span data-ttu-id="f7380-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="f7380-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="f7380-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7380-102">SYNOPSIS</span></span>
<span data-ttu-id="f7380-103">Erstellt eine neue CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f7380-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="f7380-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7380-104">SYNTAX</span></span>

### <span data-ttu-id="f7380-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7380-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7380-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7380-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7380-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7380-107">DESCRIPTION</span></span>
<span data-ttu-id="f7380-108">Erstellt eine neue CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f7380-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="f7380-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7380-109">EXAMPLES</span></span>

### <span data-ttu-id="f7380-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7380-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="f7380-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7380-111">PARAMETERS</span></span>

### <span data-ttu-id="f7380-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="f7380-112">-AccountName</span></span>
<span data-ttu-id="f7380-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="f7380-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7380-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f7380-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f7380-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f7380-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f7380-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7380-116">-Confirm</span></span>
<span data-ttu-id="f7380-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7380-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7380-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7380-118">-DefaultProfile</span></span>
<span data-ttu-id="f7380-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7380-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7380-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f7380-120">-Name</span></span>
<span data-ttu-id="f7380-121">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f7380-121">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7380-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7380-122">-ParentObject</span></span>
<span data-ttu-id="f7380-123">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="f7380-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f7380-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7380-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7380-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7380-125">Name of resource group.</span></span>

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

### <span data-ttu-id="f7380-126">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="f7380-126">-Throughput</span></span>
<span data-ttu-id="f7380-127">Der Durchsatz der Tabelle (ru/s).</span><span class="sxs-lookup"><span data-stu-id="f7380-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="f7380-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="f7380-128">Default value is 400.</span></span>

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

### <span data-ttu-id="f7380-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7380-129">-WhatIf</span></span>
<span data-ttu-id="f7380-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7380-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7380-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7380-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7380-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7380-132">CommonParameters</span></span>
<span data-ttu-id="f7380-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7380-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7380-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7380-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7380-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7380-135">INPUTS</span></span>

### <span data-ttu-id="f7380-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f7380-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f7380-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7380-137">OUTPUTS</span></span>

### <span data-ttu-id="f7380-138">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f7380-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="f7380-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f7380-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f7380-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7380-140">NOTES</span></span>

## <span data-ttu-id="f7380-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7380-141">RELATED LINKS</span></span>
