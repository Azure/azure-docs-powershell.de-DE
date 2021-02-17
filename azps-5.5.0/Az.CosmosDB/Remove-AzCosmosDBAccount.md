---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163988"
---
# <span data-ttu-id="b8e1a-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b8e1a-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b8e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e1a-103">Entfernen Sie ein Konto aus Demdb.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="b8e1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8e1a-104">SYNTAX</span></span>

### <span data-ttu-id="b8e1a-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8e1a-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e1a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8e1a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e1a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8e1a-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e1a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8e1a-108">DESCRIPTION</span></span>
<span data-ttu-id="b8e1a-109">Entfernen Sie in der angegebenen Ressourcengruppe ein Konto vomTyp "Kundendb" mit einem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="b8e1a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8e1a-110">EXAMPLES</span></span>

### <span data-ttu-id="b8e1a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8e1a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="b8e1a-112">Das Konto mit dem Kontonamen "dbname" in "ResourceGroup rg" wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="b8e1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8e1a-113">PARAMETERS</span></span>

### <span data-ttu-id="b8e1a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8e1a-114">-AsJob</span></span>
<span data-ttu-id="b8e1a-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8e1a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8e1a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8e1a-116">-Confirm</span></span>
<span data-ttu-id="b8e1a-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e1a-118">-DefaultProfile</span></span>
<span data-ttu-id="b8e1a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e1a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8e1a-120">-InputObject</span></span>
<span data-ttu-id="b8e1a-121">Das Datenbankkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b8e1a-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e1a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b8e1a-122">-Name</span></span>
<span data-ttu-id="b8e1a-123">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b8e1a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8e1a-124">-PassThru</span></span>
<span data-ttu-id="b8e1a-125">Soll auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b8e1a-126">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war, und andern falls nicht, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b8e1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b8e1a-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b8e1a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e1a-129">-ResourceId</span></span>
<span data-ttu-id="b8e1a-130">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e1a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b8e1a-131">-WhatIf</span></span>
<span data-ttu-id="b8e1a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e1a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e1a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e1a-134">CommonParameters</span></span>
<span data-ttu-id="b8e1a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e1a-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8e1a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e1a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8e1a-137">INPUTS</span></span>

### <span data-ttu-id="b8e1a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b8e1a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b8e1a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8e1a-139">OUTPUTS</span></span>

### <span data-ttu-id="b8e1a-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b8e1a-140">System.Void</span></span>

## <span data-ttu-id="b8e1a-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8e1a-141">NOTES</span></span>

## <span data-ttu-id="b8e1a-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8e1a-142">RELATED LINKS</span></span>
