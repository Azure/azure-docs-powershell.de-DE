---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004641"
---
# <span data-ttu-id="c610b-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="c610b-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="c610b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c610b-102">SYNOPSIS</span></span>
<span data-ttu-id="c610b-103">Legt die CosmosDB-MongoDB-Datenbank fest</span><span class="sxs-lookup"><span data-stu-id="c610b-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="c610b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c610b-104">SYNTAX</span></span>

### <span data-ttu-id="c610b-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c610b-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c610b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c610b-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c610b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c610b-107">DESCRIPTION</span></span>
<span data-ttu-id="c610b-108">Das Cmdlet " **Satz-AzCosmosDBMongoDBDatabase** " Ruft die CosmosDB MongoDB-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c610b-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="c610b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c610b-109">EXAMPLES</span></span>

### <span data-ttu-id="c610b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c610b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="c610b-111">Das Ressourcenobjekt enthält _rid, _ts, _etag Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c610b-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="c610b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c610b-112">PARAMETERS</span></span>

### <span data-ttu-id="c610b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c610b-113">-AccountName</span></span>
<span data-ttu-id="c610b-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="c610b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c610b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c610b-115">-Confirm</span></span>
<span data-ttu-id="c610b-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c610b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c610b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c610b-117">-DefaultProfile</span></span>
<span data-ttu-id="c610b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c610b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c610b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c610b-119">-InputObject</span></span>
<span data-ttu-id="c610b-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="c610b-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c610b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c610b-121">-Name</span></span>
<span data-ttu-id="c610b-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="c610b-122">Database name.</span></span>

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

### <span data-ttu-id="c610b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c610b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c610b-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c610b-124">Name of resource group.</span></span>

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

### <span data-ttu-id="c610b-125">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="c610b-125">-Throughput</span></span>
<span data-ttu-id="c610b-126">Der Durchsatz der Mongo-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="c610b-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="c610b-127">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="c610b-127">Default value is 400.</span></span>

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

### <span data-ttu-id="c610b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c610b-128">-WhatIf</span></span>
<span data-ttu-id="c610b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c610b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c610b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c610b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c610b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c610b-131">CommonParameters</span></span>
<span data-ttu-id="c610b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c610b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c610b-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c610b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c610b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c610b-134">INPUTS</span></span>

### <span data-ttu-id="c610b-135">Keine</span><span class="sxs-lookup"><span data-stu-id="c610b-135">None</span></span>

## <span data-ttu-id="c610b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c610b-136">OUTPUTS</span></span>

### <span data-ttu-id="c610b-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c610b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="c610b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c610b-138">NOTES</span></span>

## <span data-ttu-id="c610b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c610b-139">RELATED LINKS</span></span>
