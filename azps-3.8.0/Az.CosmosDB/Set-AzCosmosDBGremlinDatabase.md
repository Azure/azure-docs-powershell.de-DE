---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004642"
---
# <span data-ttu-id="757ad-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="757ad-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="757ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="757ad-102">SYNOPSIS</span></span>
<span data-ttu-id="757ad-103">Legt die CosmosDB-Gremlin-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="757ad-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="757ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="757ad-104">SYNTAX</span></span>

### <span data-ttu-id="757ad-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="757ad-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="757ad-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="757ad-107">DESCRIPTION</span></span>
<span data-ttu-id="757ad-108">Das Cmdlet " **Set-AzCosmosDBGremlinDatabase** " legt die CosmosDB-Gremlin-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="757ad-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="757ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="757ad-109">EXAMPLES</span></span>

### <span data-ttu-id="757ad-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="757ad-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="757ad-111">Das Ressourcenobjekt enthält _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="757ad-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="757ad-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="757ad-112">PARAMETERS</span></span>

### <span data-ttu-id="757ad-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="757ad-113">-AccountName</span></span>
<span data-ttu-id="757ad-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="757ad-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="757ad-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="757ad-115">-Confirm</span></span>
<span data-ttu-id="757ad-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="757ad-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757ad-117">-DefaultProfile</span></span>
<span data-ttu-id="757ad-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="757ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="757ad-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="757ad-119">-InputObject</span></span>
<span data-ttu-id="757ad-120">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="757ad-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="757ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="757ad-121">-Name</span></span>
<span data-ttu-id="757ad-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="757ad-122">Database name.</span></span>

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

### <span data-ttu-id="757ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="757ad-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="757ad-124">Name of resource group.</span></span>

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

### <span data-ttu-id="757ad-125">-Durchsatz</span><span class="sxs-lookup"><span data-stu-id="757ad-125">-Throughput</span></span>
<span data-ttu-id="757ad-126">Der Durchsatz der Gremlin-Datenbank (ru/s).</span><span class="sxs-lookup"><span data-stu-id="757ad-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="757ad-127">Der Standardwert ist 400.</span><span class="sxs-lookup"><span data-stu-id="757ad-127">Default value is 400.</span></span>

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

### <span data-ttu-id="757ad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757ad-128">-WhatIf</span></span>
<span data-ttu-id="757ad-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="757ad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757ad-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="757ad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757ad-131">CommonParameters</span></span>
<span data-ttu-id="757ad-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757ad-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="757ad-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757ad-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="757ad-134">INPUTS</span></span>

### <span data-ttu-id="757ad-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="757ad-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="757ad-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="757ad-136">OUTPUTS</span></span>

### <span data-ttu-id="757ad-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="757ad-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="757ad-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="757ad-138">NOTES</span></span>

## <span data-ttu-id="757ad-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="757ad-139">RELATED LINKS</span></span>
