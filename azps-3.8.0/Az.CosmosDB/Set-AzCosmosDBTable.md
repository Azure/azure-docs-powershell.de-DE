---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996895"
---
# <span data-ttu-id="08f59-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="08f59-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="08f59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08f59-102">SYNOPSIS</span></span>
<span data-ttu-id="08f59-103">Legt die CosmosDB-Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="08f59-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="08f59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08f59-104">SYNTAX</span></span>

### <span data-ttu-id="08f59-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="08f59-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f59-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f59-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f59-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08f59-107">DESCRIPTION</span></span>
<span data-ttu-id="08f59-108">Das Cmdlet " **Satz-AzCosmosDBTable** " erstellt eine neue Tabelle oder aktualisiert eine vorhandene Tabelle, wobei die vorhandene Tabelle vollständig ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="08f59-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="08f59-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08f59-109">EXAMPLES</span></span>

### <span data-ttu-id="08f59-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08f59-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="08f59-111">Das Ressourcenobjekt enthält _rid, _ts, _ ETag-Eigenschaften der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="08f59-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="08f59-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08f59-112">PARAMETERS</span></span>

### <span data-ttu-id="08f59-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="08f59-113">-AccountName</span></span>
<span data-ttu-id="08f59-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="08f59-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="08f59-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08f59-115">-Confirm</span></span>
<span data-ttu-id="08f59-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08f59-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f59-117">-DefaultProfile</span></span>
<span data-ttu-id="08f59-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08f59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f59-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08f59-119">-InputObject</span></span>
<span data-ttu-id="08f59-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="08f59-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f59-121">-Name</span><span class="sxs-lookup"><span data-stu-id="08f59-121">-Name</span></span>
<span data-ttu-id="08f59-122">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="08f59-122">Name of the Table.</span></span>

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

### <span data-ttu-id="08f59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f59-123">-ResourceGroupName</span></span>
<span data-ttu-id="08f59-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08f59-124">Name of resource group.</span></span>

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

### <span data-ttu-id="08f59-125">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="08f59-125">-Throughput</span></span>
<span data-ttu-id="08f59-126">Der Durchsatz der Tabelle (ru/s).</span><span class="sxs-lookup"><span data-stu-id="08f59-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="08f59-127">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="08f59-127">Default value is 400.</span></span>

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

### <span data-ttu-id="08f59-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f59-128">-WhatIf</span></span>
<span data-ttu-id="08f59-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08f59-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f59-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08f59-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f59-131">CommonParameters</span></span>
<span data-ttu-id="08f59-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f59-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f59-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f59-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08f59-134">INPUTS</span></span>

### <span data-ttu-id="08f59-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="08f59-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="08f59-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08f59-136">OUTPUTS</span></span>

### <span data-ttu-id="08f59-137">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="08f59-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="08f59-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="08f59-138">NOTES</span></span>

## <span data-ttu-id="08f59-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08f59-139">RELATED LINKS</span></span>
