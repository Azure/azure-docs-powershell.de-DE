---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293219"
---
# <span data-ttu-id="71025-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="71025-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="71025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71025-102">SYNOPSIS</span></span>
<span data-ttu-id="71025-103">Entfernen Sie ein Kundenkonto..</span><span class="sxs-lookup"><span data-stu-id="71025-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="71025-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71025-104">SYNTAX</span></span>

### <span data-ttu-id="71025-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="71025-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71025-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71025-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71025-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71025-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71025-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71025-108">DESCRIPTION</span></span>
<span data-ttu-id="71025-109">Entfernen Sie in der angegebenen Ressourcengruppe ein Kundenkonto vom 1. Bis zum 1.</span><span class="sxs-lookup"><span data-stu-id="71025-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="71025-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71025-110">EXAMPLES</span></span>

### <span data-ttu-id="71025-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71025-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="71025-112">Das Konto mit dem Kontonamen "dbname" in "ResourceGroup rg" wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="71025-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="71025-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71025-113">PARAMETERS</span></span>

### <span data-ttu-id="71025-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71025-114">-AsJob</span></span>
<span data-ttu-id="71025-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="71025-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71025-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71025-116">-Confirm</span></span>
<span data-ttu-id="71025-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71025-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71025-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71025-118">-DefaultProfile</span></span>
<span data-ttu-id="71025-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71025-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71025-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71025-120">-InputObject</span></span>
<span data-ttu-id="71025-121">Das Datenbankkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="71025-121">The Database Account object</span></span>

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

### <span data-ttu-id="71025-122">-Name</span><span class="sxs-lookup"><span data-stu-id="71025-122">-Name</span></span>
<span data-ttu-id="71025-123">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="71025-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="71025-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71025-124">-PassThru</span></span>
<span data-ttu-id="71025-125">Wird auf "true" festgelegt, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="71025-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="71025-126">Die Ausgabe ist "true", wenn der Vorgang erfolgreich war und andern falls nicht ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="71025-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="71025-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71025-127">-ResourceGroupName</span></span>
<span data-ttu-id="71025-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71025-128">Name of resource group.</span></span>

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

### <span data-ttu-id="71025-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71025-129">-ResourceId</span></span>
<span data-ttu-id="71025-130">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="71025-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="71025-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71025-131">-WhatIf</span></span>
<span data-ttu-id="71025-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71025-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71025-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71025-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71025-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71025-134">CommonParameters</span></span>
<span data-ttu-id="71025-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71025-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71025-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71025-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71025-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71025-137">INPUTS</span></span>

### <span data-ttu-id="71025-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="71025-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="71025-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71025-139">OUTPUTS</span></span>

### <span data-ttu-id="71025-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="71025-140">System.Void</span></span>

## <span data-ttu-id="71025-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71025-141">NOTES</span></span>

## <span data-ttu-id="71025-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71025-142">RELATED LINKS</span></span>
