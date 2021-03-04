---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: ab64359e8db417c3c87a49a773fe56c3dcc5334b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921331"
---
# <span data-ttu-id="59766-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="59766-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="59766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59766-102">SYNOPSIS</span></span>
<span data-ttu-id="59766-103">Löscht den CosmosDB Sql Container.</span><span class="sxs-lookup"><span data-stu-id="59766-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="59766-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59766-104">SYNTAX</span></span>

### <span data-ttu-id="59766-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59766-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59766-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59766-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59766-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59766-107">DESCRIPTION</span></span>
<span data-ttu-id="59766-108">Das **Cmdlet Remove-AzCosmosDBSqlContainer** löscht den CosmosDB Sql Container, der den angegebenen ResourceGroupName, AccountName, DatabaseName und ContainerName entspricht.</span><span class="sxs-lookup"><span data-stu-id="59766-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="59766-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59766-109">EXAMPLES</span></span>

### <span data-ttu-id="59766-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59766-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="59766-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59766-111">PARAMETERS</span></span>

### <span data-ttu-id="59766-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59766-112">-AccountName</span></span>
<span data-ttu-id="59766-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="59766-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="59766-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59766-114">-Confirm</span></span>
<span data-ttu-id="59766-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59766-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59766-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59766-116">-DatabaseName</span></span>
<span data-ttu-id="59766-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="59766-117">Database name.</span></span>

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

### <span data-ttu-id="59766-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59766-118">-DefaultProfile</span></span>
<span data-ttu-id="59766-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59766-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59766-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59766-120">-InputObject</span></span>
<span data-ttu-id="59766-121">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="59766-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59766-122">-Name</span><span class="sxs-lookup"><span data-stu-id="59766-122">-Name</span></span>
<span data-ttu-id="59766-123">Containername.</span><span class="sxs-lookup"><span data-stu-id="59766-123">Container name.</span></span>

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

### <span data-ttu-id="59766-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59766-124">-PassThru</span></span>
<span data-ttu-id="59766-125">Um auf true festgelegt zu sein, wenn der Benutzer eine Ausgabe erhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="59766-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="59766-126">Die Ausgabe ist true, wenn der Vorgang erfolgreich war und ein Fehler ausgelöst wird, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="59766-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="59766-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59766-127">-ResourceGroupName</span></span>
<span data-ttu-id="59766-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59766-128">Name of resource group.</span></span>

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

### <span data-ttu-id="59766-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59766-129">-WhatIf</span></span>
<span data-ttu-id="59766-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59766-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59766-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59766-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59766-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59766-132">CommonParameters</span></span>
<span data-ttu-id="59766-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59766-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59766-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59766-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59766-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59766-135">INPUTS</span></span>

### <span data-ttu-id="59766-136">Keine</span><span class="sxs-lookup"><span data-stu-id="59766-136">None</span></span>

## <span data-ttu-id="59766-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59766-137">OUTPUTS</span></span>

### <span data-ttu-id="59766-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="59766-138">System.Void</span></span>

### <span data-ttu-id="59766-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59766-139">System.Boolean</span></span>

## <span data-ttu-id="59766-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="59766-140">NOTES</span></span>

## <span data-ttu-id="59766-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="59766-141">RELATED LINKS</span></span>
