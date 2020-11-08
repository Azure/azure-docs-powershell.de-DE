---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009940"
---
# <span data-ttu-id="3d500-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="3d500-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="3d500-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d500-102">SYNOPSIS</span></span>
<span data-ttu-id="3d500-103">Löscht eine CosmosDB-Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3d500-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="3d500-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d500-104">SYNTAX</span></span>

### <span data-ttu-id="3d500-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d500-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d500-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d500-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d500-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d500-107">DESCRIPTION</span></span>
<span data-ttu-id="3d500-108">Das Cmdlet **Remove-AzCosmosDBGremlinDatabase** löscht eine CosmosDB Gremlin-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3d500-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="3d500-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d500-109">EXAMPLES</span></span>

### <span data-ttu-id="3d500-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d500-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="3d500-111">Das Cmdlet gibt ein Objekt vom Typ bool zurück (wenn-passthru übergeben wird), das wahr ist, wenn der Löschvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3d500-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="3d500-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d500-112">PARAMETERS</span></span>

### <span data-ttu-id="3d500-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="3d500-113">-AccountName</span></span>
<span data-ttu-id="3d500-114">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="3d500-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3d500-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d500-115">-Confirm</span></span>
<span data-ttu-id="3d500-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d500-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d500-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d500-117">-DefaultProfile</span></span>
<span data-ttu-id="3d500-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d500-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d500-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d500-119">-InputObject</span></span>
<span data-ttu-id="3d500-120">Gremlin-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="3d500-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d500-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3d500-121">-Name</span></span>
<span data-ttu-id="3d500-122">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="3d500-122">Database name.</span></span>

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

### <span data-ttu-id="3d500-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d500-123">-PassThru</span></span>
<span data-ttu-id="3d500-124">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="3d500-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="3d500-125">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3d500-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="3d500-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d500-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d500-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d500-127">Name of resource group.</span></span>

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

### <span data-ttu-id="3d500-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d500-128">-WhatIf</span></span>
<span data-ttu-id="3d500-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d500-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d500-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d500-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d500-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d500-131">CommonParameters</span></span>
<span data-ttu-id="3d500-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d500-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d500-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d500-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d500-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d500-134">INPUTS</span></span>

### <span data-ttu-id="3d500-135">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3d500-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="3d500-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d500-136">OUTPUTS</span></span>

### <span data-ttu-id="3d500-137">System. void</span><span class="sxs-lookup"><span data-stu-id="3d500-137">System.Void</span></span>

### <span data-ttu-id="3d500-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d500-138">System.Boolean</span></span>

## <span data-ttu-id="3d500-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d500-139">NOTES</span></span>

## <span data-ttu-id="3d500-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d500-140">RELATED LINKS</span></span>
