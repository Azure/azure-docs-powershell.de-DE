---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ff294af7e4305facd3265d96151c97b82ff9c052
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947992"
---
# <span data-ttu-id="dfcf2-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="dfcf2-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="dfcf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfcf2-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcf2-103">Löscht die Tabelle "CosmosDB".</span><span class="sxs-lookup"><span data-stu-id="dfcf2-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="dfcf2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfcf2-104">SYNTAX</span></span>

### <span data-ttu-id="dfcf2-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfcf2-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfcf2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfcf2-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcf2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfcf2-107">DESCRIPTION</span></span>
<span data-ttu-id="dfcf2-108">Das **Cmdlet Remove-AzCosmosDBTable** löscht die Tabelle "CosmosDB".</span><span class="sxs-lookup"><span data-stu-id="dfcf2-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="dfcf2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfcf2-109">EXAMPLES</span></span>

### <span data-ttu-id="dfcf2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dfcf2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="dfcf2-111">Das Cmdlet gibt ein Objekt vom Typ bool(wenn -PassThru übergeben wird) zurück, das wahr ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="dfcf2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dfcf2-112">PARAMETERS</span></span>

### <span data-ttu-id="dfcf2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dfcf2-113">-AccountName</span></span>
<span data-ttu-id="dfcf2-114">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="dfcf2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dfcf2-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfcf2-115">-Confirm</span></span>
<span data-ttu-id="dfcf2-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcf2-117">-DefaultProfile</span></span>
<span data-ttu-id="dfcf2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfcf2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfcf2-119">-InputObject</span></span>
<span data-ttu-id="dfcf2-120">Sql Database-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-120">Sql Database object.</span></span>

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

### <span data-ttu-id="dfcf2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dfcf2-121">-Name</span></span>
<span data-ttu-id="dfcf2-122">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-122">Name of the Table.</span></span>

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

### <span data-ttu-id="dfcf2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfcf2-123">-PassThru</span></span>
<span data-ttu-id="dfcf2-124">Um auf true festgelegt zu sein, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dfcf2-125">Die Ausgabe ist true, wenn der Vorgang erfolgreich war und ein Fehler ausgelöst wird, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dfcf2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcf2-126">-ResourceGroupName</span></span>
<span data-ttu-id="dfcf2-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-127">Name of resource group.</span></span>

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

### <span data-ttu-id="dfcf2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcf2-128">-WhatIf</span></span>
<span data-ttu-id="dfcf2-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcf2-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcf2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcf2-131">CommonParameters</span></span>
<span data-ttu-id="dfcf2-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcf2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcf2-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfcf2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcf2-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfcf2-134">INPUTS</span></span>

### <span data-ttu-id="dfcf2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="dfcf2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="dfcf2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfcf2-136">OUTPUTS</span></span>

### <span data-ttu-id="dfcf2-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="dfcf2-137">System.Void</span></span>

### <span data-ttu-id="dfcf2-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dfcf2-138">System.Boolean</span></span>

## <span data-ttu-id="dfcf2-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dfcf2-139">NOTES</span></span>

## <span data-ttu-id="dfcf2-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dfcf2-140">RELATED LINKS</span></span>
