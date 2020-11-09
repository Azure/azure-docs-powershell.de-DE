---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299200"
---
# <span data-ttu-id="9514e-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="9514e-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="9514e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9514e-102">SYNOPSIS</span></span>
<span data-ttu-id="9514e-103">Erstellt eine neue CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9514e-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="9514e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9514e-104">SYNTAX</span></span>

### <span data-ttu-id="9514e-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9514e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9514e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9514e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9514e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9514e-107">DESCRIPTION</span></span>
<span data-ttu-id="9514e-108">Erstellt eine neue CosmosDB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9514e-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="9514e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9514e-109">EXAMPLES</span></span>

### <span data-ttu-id="9514e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9514e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="9514e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9514e-111">PARAMETERS</span></span>

### <span data-ttu-id="9514e-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9514e-112">-AccountName</span></span>
<span data-ttu-id="9514e-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="9514e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9514e-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9514e-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9514e-115">Maximaler Durchsatz, wenn "AutoScale" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9514e-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9514e-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9514e-116">-Confirm</span></span>
<span data-ttu-id="9514e-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9514e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9514e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9514e-118">-DefaultProfile</span></span>
<span data-ttu-id="9514e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9514e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9514e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9514e-120">-Name</span></span>
<span data-ttu-id="9514e-121">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9514e-121">Name of the Table.</span></span>

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

### <span data-ttu-id="9514e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9514e-122">-ParentObject</span></span>
<span data-ttu-id="9514e-123">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="9514e-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9514e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9514e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9514e-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9514e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="9514e-126">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="9514e-126">-Throughput</span></span>
<span data-ttu-id="9514e-127">Der Durchsatz der Tabelle (ru/s).</span><span class="sxs-lookup"><span data-stu-id="9514e-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="9514e-128">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="9514e-128">Default value is 400.</span></span>

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

### <span data-ttu-id="9514e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9514e-129">-WhatIf</span></span>
<span data-ttu-id="9514e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9514e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9514e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9514e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9514e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9514e-132">CommonParameters</span></span>
<span data-ttu-id="9514e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9514e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9514e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9514e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9514e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9514e-135">INPUTS</span></span>

### <span data-ttu-id="9514e-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9514e-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9514e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9514e-137">OUTPUTS</span></span>

### <span data-ttu-id="9514e-138">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="9514e-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="9514e-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="9514e-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="9514e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9514e-140">NOTES</span></span>

## <span data-ttu-id="9514e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9514e-141">RELATED LINKS</span></span>
