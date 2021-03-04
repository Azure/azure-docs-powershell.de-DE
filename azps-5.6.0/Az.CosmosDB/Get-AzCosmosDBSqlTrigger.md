---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936251"
---
# <span data-ttu-id="5217a-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5217a-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5217a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5217a-102">SYNOPSIS</span></span>
<span data-ttu-id="5217a-103">Ruft den CosmosDB Sql Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="5217a-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5217a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5217a-104">SYNTAX</span></span>

### <span data-ttu-id="5217a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5217a-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5217a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5217a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5217a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5217a-107">DESCRIPTION</span></span>
<span data-ttu-id="5217a-108">Das **Get-AzCosmosDBSqlTrigger-Cmdlet** ruft die Liste aller vorhandenen CosmosDB-Sql-Trigger für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab und ruft einen einzelnen CosmosDB-Sql-Trigger für einen bestimmten ResourceGroupName, AccountName, DatabaseName, ContainerName und TriggerName ab.</span><span class="sxs-lookup"><span data-stu-id="5217a-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="5217a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5217a-109">EXAMPLES</span></span>

### <span data-ttu-id="5217a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5217a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="5217a-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5217a-111">PARAMETERS</span></span>

### <span data-ttu-id="5217a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5217a-112">-AccountName</span></span>
<span data-ttu-id="5217a-113">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="5217a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5217a-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5217a-114">-ContainerName</span></span>
<span data-ttu-id="5217a-115">Containername.</span><span class="sxs-lookup"><span data-stu-id="5217a-115">Container name.</span></span>

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

### <span data-ttu-id="5217a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5217a-116">-DatabaseName</span></span>
<span data-ttu-id="5217a-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="5217a-117">Database name.</span></span>

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

### <span data-ttu-id="5217a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5217a-118">-DefaultProfile</span></span>
<span data-ttu-id="5217a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5217a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5217a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5217a-120">-Name</span></span>
<span data-ttu-id="5217a-121">Triggername.</span><span class="sxs-lookup"><span data-stu-id="5217a-121">Trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5217a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5217a-122">-ParentObject</span></span>
<span data-ttu-id="5217a-123">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5217a-123">Sql Container object.</span></span>

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

### <span data-ttu-id="5217a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5217a-124">-ResourceGroupName</span></span>
<span data-ttu-id="5217a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5217a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5217a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5217a-126">CommonParameters</span></span>
<span data-ttu-id="5217a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5217a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5217a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5217a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5217a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5217a-129">INPUTS</span></span>

### <span data-ttu-id="5217a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="5217a-130">None</span></span>

## <span data-ttu-id="5217a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5217a-131">OUTPUTS</span></span>

### <span data-ttu-id="5217a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="5217a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="5217a-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5217a-133">NOTES</span></span>

## <span data-ttu-id="5217a-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5217a-134">RELATED LINKS</span></span>
