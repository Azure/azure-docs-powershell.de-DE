---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175300"
---
# <span data-ttu-id="a896c-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="a896c-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="a896c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a896c-102">SYNOPSIS</span></span>
<span data-ttu-id="a896c-103">Ruft den CosmosDB-SQL-Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="a896c-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a896c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a896c-104">SYNTAX</span></span>

### <span data-ttu-id="a896c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a896c-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a896c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a896c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a896c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a896c-107">DESCRIPTION</span></span>
<span data-ttu-id="a896c-108">Das Cmdlet " **Get-AzCosmosDBSqlTrigger** " Ruft die Liste aller vorhandenen CosmosDB-SQL-Trigger für einen angegebenen ResourceGroupName, Accountname, DatabaseName und Containername ab und Ruft einen einzelnen CosmosDB-SQL-Trigger für einen bestimmten ResourceGroupName, Accountname, DatabaseName, Containername und Triggername ab.</span><span class="sxs-lookup"><span data-stu-id="a896c-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="a896c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a896c-109">EXAMPLES</span></span>

### <span data-ttu-id="a896c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a896c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="a896c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a896c-111">PARAMETERS</span></span>

### <span data-ttu-id="a896c-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a896c-112">-AccountName</span></span>
<span data-ttu-id="a896c-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="a896c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a896c-114">-Containername</span><span class="sxs-lookup"><span data-stu-id="a896c-114">-ContainerName</span></span>
<span data-ttu-id="a896c-115">Container Name.</span><span class="sxs-lookup"><span data-stu-id="a896c-115">Container name.</span></span>

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

### <span data-ttu-id="a896c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a896c-116">-DatabaseName</span></span>
<span data-ttu-id="a896c-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="a896c-117">Database name.</span></span>

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

### <span data-ttu-id="a896c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a896c-118">-DefaultProfile</span></span>
<span data-ttu-id="a896c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a896c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a896c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a896c-120">-Name</span></span>
<span data-ttu-id="a896c-121">Name des Triggers</span><span class="sxs-lookup"><span data-stu-id="a896c-121">Trigger name.</span></span>

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

### <span data-ttu-id="a896c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a896c-122">-ParentObject</span></span>
<span data-ttu-id="a896c-123">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="a896c-123">Sql Container object.</span></span>

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

### <span data-ttu-id="a896c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a896c-124">-ResourceGroupName</span></span>
<span data-ttu-id="a896c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a896c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a896c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a896c-126">CommonParameters</span></span>
<span data-ttu-id="a896c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a896c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a896c-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a896c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a896c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a896c-129">INPUTS</span></span>

### <span data-ttu-id="a896c-130">Keine</span><span class="sxs-lookup"><span data-stu-id="a896c-130">None</span></span>

## <span data-ttu-id="a896c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a896c-131">OUTPUTS</span></span>

### <span data-ttu-id="a896c-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="a896c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="a896c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a896c-133">NOTES</span></span>

## <span data-ttu-id="a896c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a896c-134">RELATED LINKS</span></span>
