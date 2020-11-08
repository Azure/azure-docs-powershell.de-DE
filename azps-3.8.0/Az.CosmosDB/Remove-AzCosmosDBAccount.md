---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: e9ec1f1626a1fb4335c6e5df43a96727692538c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003921"
---
# <span data-ttu-id="5e37f-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="5e37f-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="5e37f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e37f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e37f-103">Entfernen eines CosmosDB-Kontos</span><span class="sxs-lookup"><span data-stu-id="5e37f-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="5e37f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e37f-104">SYNTAX</span></span>

### <span data-ttu-id="5e37f-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e37f-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e37f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e37f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e37f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e37f-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e37f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e37f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e37f-109">Entfernen Sie ein CosmosDB-Konto mit einem angegebenen Namen in der angegebenen ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5e37f-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="5e37f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e37f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e37f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e37f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="5e37f-112">Das Konto mit dem Kontonamen dbname in der ResourceGroup RG wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5e37f-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="5e37f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e37f-113">PARAMETERS</span></span>

### <span data-ttu-id="5e37f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e37f-114">-AsJob</span></span>
<span data-ttu-id="5e37f-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5e37f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e37f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e37f-116">-Confirm</span></span>
<span data-ttu-id="5e37f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e37f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e37f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e37f-118">-DefaultProfile</span></span>
<span data-ttu-id="5e37f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e37f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e37f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e37f-120">-InputObject</span></span>
<span data-ttu-id="5e37f-121">Das Daten Bank Konto-Objekt</span><span class="sxs-lookup"><span data-stu-id="5e37f-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e37f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5e37f-122">-Name</span></span>
<span data-ttu-id="5e37f-123">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="5e37f-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e37f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e37f-124">-PassThru</span></span>
<span data-ttu-id="5e37f-125">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="5e37f-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5e37f-126">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="5e37f-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5e37f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e37f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e37f-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e37f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="5e37f-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e37f-129">-ResourceId</span></span>
<span data-ttu-id="5e37f-130">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="5e37f-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="5e37f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e37f-131">-WhatIf</span></span>
<span data-ttu-id="5e37f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e37f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e37f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e37f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e37f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e37f-134">CommonParameters</span></span>
<span data-ttu-id="5e37f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e37f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e37f-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e37f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e37f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e37f-137">INPUTS</span></span>

### <span data-ttu-id="5e37f-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5e37f-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5e37f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e37f-139">OUTPUTS</span></span>

### <span data-ttu-id="5e37f-140">System. void</span><span class="sxs-lookup"><span data-stu-id="5e37f-140">System.Void</span></span>

## <span data-ttu-id="5e37f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e37f-141">NOTES</span></span>

## <span data-ttu-id="5e37f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e37f-142">RELATED LINKS</span></span>
