---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b088eaf9e09408b8a294965c66acf88ac2715dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924192"
---
# <span data-ttu-id="3d824-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="3d824-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="3d824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d824-102">SYNOPSIS</span></span>
<span data-ttu-id="3d824-103">Erstellt eine neue CosmosDB Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="3d824-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="3d824-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d824-104">SYNTAX</span></span>

### <span data-ttu-id="3d824-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d824-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d824-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d824-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d824-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d824-107">DESCRIPTION</span></span>
<span data-ttu-id="3d824-108">Erstellt eine neue CosmosDB Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="3d824-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="3d824-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d824-109">EXAMPLES</span></span>

### <span data-ttu-id="3d824-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d824-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="3d824-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3d824-111">PARAMETERS</span></span>

### <span data-ttu-id="3d824-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d824-112">-AccountName</span></span>
<span data-ttu-id="3d824-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="3d824-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3d824-114">-Body</span><span class="sxs-lookup"><span data-stu-id="3d824-114">-Body</span></span>
<span data-ttu-id="3d824-115">Der Textkörper der gespeicherten Prozedur.</span><span class="sxs-lookup"><span data-stu-id="3d824-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="3d824-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d824-116">-Confirm</span></span>
<span data-ttu-id="3d824-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d824-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d824-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3d824-118">-ContainerName</span></span>
<span data-ttu-id="3d824-119">Containername.</span><span class="sxs-lookup"><span data-stu-id="3d824-119">Container name.</span></span>

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

### <span data-ttu-id="3d824-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d824-120">-DatabaseName</span></span>
<span data-ttu-id="3d824-121">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="3d824-121">Database name.</span></span>

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

### <span data-ttu-id="3d824-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d824-122">-DefaultProfile</span></span>
<span data-ttu-id="3d824-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d824-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d824-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d824-124">-Name</span></span>
<span data-ttu-id="3d824-125">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="3d824-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="3d824-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d824-126">-ParentObject</span></span>
<span data-ttu-id="3d824-127">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3d824-127">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d824-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d824-128">-ResourceGroupName</span></span>
<span data-ttu-id="3d824-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d824-129">Name of resource group.</span></span>

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

### <span data-ttu-id="3d824-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d824-130">-WhatIf</span></span>
<span data-ttu-id="3d824-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d824-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d824-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d824-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d824-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d824-133">CommonParameters</span></span>
<span data-ttu-id="3d824-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d824-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d824-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d824-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d824-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d824-136">INPUTS</span></span>

### <span data-ttu-id="3d824-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="3d824-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="3d824-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d824-138">OUTPUTS</span></span>

### <span data-ttu-id="3d824-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="3d824-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="3d824-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="3d824-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="3d824-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3d824-141">NOTES</span></span>

## <span data-ttu-id="3d824-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3d824-142">RELATED LINKS</span></span>
