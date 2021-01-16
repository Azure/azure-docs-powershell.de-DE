---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372391"
---
# <span data-ttu-id="ae082-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="ae082-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="ae082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae082-102">SYNOPSIS</span></span>
<span data-ttu-id="ae082-103">Ruft den Auslöser für Die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ae082-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="ae082-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae082-104">SYNTAX</span></span>

### <span data-ttu-id="ae082-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae082-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae082-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae082-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae082-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae082-107">DESCRIPTION</span></span>
<span data-ttu-id="ae082-108">Das **Cmdlet "Get-AzCosmosDBSqlTrigger"** ruft die Liste aller vorhandenen Sql-Auslöser von "Aufgrunddb" für einen bestimmten ResourceGroupName, AccountName, DatabaseName und ContainerName ab und ruft einen einzelnen "Durchgeh"-Sql-Trigger für einen bestimmten ResourceGroupName, AccountName, DatabaseName, ContainerName und TriggerName ab.</span><span class="sxs-lookup"><span data-stu-id="ae082-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="ae082-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae082-109">EXAMPLES</span></span>

### <span data-ttu-id="ae082-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae082-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="ae082-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae082-111">PARAMETERS</span></span>

### <span data-ttu-id="ae082-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae082-112">-AccountName</span></span>
<span data-ttu-id="ae082-113">Name des Dbdatenbankkontos".</span><span class="sxs-lookup"><span data-stu-id="ae082-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ae082-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ae082-114">-ContainerName</span></span>
<span data-ttu-id="ae082-115">Containername.</span><span class="sxs-lookup"><span data-stu-id="ae082-115">Container name.</span></span>

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

### <span data-ttu-id="ae082-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae082-116">-DatabaseName</span></span>
<span data-ttu-id="ae082-117">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="ae082-117">Database name.</span></span>

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

### <span data-ttu-id="ae082-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae082-118">-DefaultProfile</span></span>
<span data-ttu-id="ae082-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae082-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae082-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ae082-120">-Name</span></span>
<span data-ttu-id="ae082-121">Triggername.</span><span class="sxs-lookup"><span data-stu-id="ae082-121">Trigger name.</span></span>

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

### <span data-ttu-id="ae082-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ae082-122">-ParentObject</span></span>
<span data-ttu-id="ae082-123">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae082-123">Sql Container object.</span></span>

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

### <span data-ttu-id="ae082-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae082-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae082-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ae082-125">Name of resource group.</span></span>

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

### <span data-ttu-id="ae082-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae082-126">CommonParameters</span></span>
<span data-ttu-id="ae082-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae082-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae082-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae082-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae082-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae082-129">INPUTS</span></span>

### <span data-ttu-id="ae082-130">Keine</span><span class="sxs-lookup"><span data-stu-id="ae082-130">None</span></span>

## <span data-ttu-id="ae082-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae082-131">OUTPUTS</span></span>

### <span data-ttu-id="ae082-132">Microsoft.Azure.Commands.ExesDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="ae082-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="ae082-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae082-133">NOTES</span></span>

## <span data-ttu-id="ae082-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae082-134">RELATED LINKS</span></span>
