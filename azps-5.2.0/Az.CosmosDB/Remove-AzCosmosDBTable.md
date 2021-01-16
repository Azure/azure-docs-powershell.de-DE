---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356962"
---
# <span data-ttu-id="bc367-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="bc367-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="bc367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc367-102">SYNOPSIS</span></span>
<span data-ttu-id="bc367-103">Löscht die Tabelle "Nach unten".</span><span class="sxs-lookup"><span data-stu-id="bc367-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="bc367-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc367-104">SYNTAX</span></span>

### <span data-ttu-id="bc367-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc367-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc367-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc367-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc367-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc367-107">DESCRIPTION</span></span>
<span data-ttu-id="bc367-108">Das **Cmdlet "Remove-AzCosmosDBTable"** löscht die Tabelle "DessDB".</span><span class="sxs-lookup"><span data-stu-id="bc367-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="bc367-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc367-109">EXAMPLES</span></span>

### <span data-ttu-id="bc367-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc367-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="bc367-111">Das Cmdlet gibt ein Objekt vom Typ boolesch (wenn -PassThru übergeben wird) zurück, das "true" ist, wenn das Löschen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bc367-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="bc367-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc367-112">PARAMETERS</span></span>

### <span data-ttu-id="bc367-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bc367-113">-AccountName</span></span>
<span data-ttu-id="bc367-114">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="bc367-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bc367-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc367-115">-Confirm</span></span>
<span data-ttu-id="bc367-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc367-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc367-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc367-117">-DefaultProfile</span></span>
<span data-ttu-id="bc367-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc367-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc367-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc367-119">-InputObject</span></span>
<span data-ttu-id="bc367-120">Sql-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="bc367-120">Sql Database object.</span></span>

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

### <span data-ttu-id="bc367-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bc367-121">-Name</span></span>
<span data-ttu-id="bc367-122">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bc367-122">Name of the Table.</span></span>

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

### <span data-ttu-id="bc367-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc367-123">-PassThru</span></span>
<span data-ttu-id="bc367-124">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="bc367-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="bc367-125">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="bc367-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="bc367-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc367-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc367-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc367-127">Name of resource group.</span></span>

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

### <span data-ttu-id="bc367-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bc367-128">-WhatIf</span></span>
<span data-ttu-id="bc367-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc367-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc367-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc367-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc367-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc367-131">CommonParameters</span></span>
<span data-ttu-id="bc367-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc367-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc367-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc367-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc367-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc367-134">INPUTS</span></span>

### <span data-ttu-id="bc367-135">Microsoft.Azure.Commands.ExesDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="bc367-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="bc367-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc367-136">OUTPUTS</span></span>

### <span data-ttu-id="bc367-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="bc367-137">System.Void</span></span>

### <span data-ttu-id="bc367-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc367-138">System.Boolean</span></span>

## <span data-ttu-id="bc367-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bc367-139">NOTES</span></span>

## <span data-ttu-id="bc367-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bc367-140">RELATED LINKS</span></span>
