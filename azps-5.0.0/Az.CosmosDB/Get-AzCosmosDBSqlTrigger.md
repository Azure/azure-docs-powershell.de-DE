---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299487"
---
# <span data-ttu-id="b953a-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="b953a-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="b953a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b953a-102">SYNOPSIS</span></span>
<span data-ttu-id="b953a-103">Ruft den CosmosDB-SQL-Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="b953a-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="b953a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b953a-104">SYNTAX</span></span>

### <span data-ttu-id="b953a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b953a-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b953a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b953a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b953a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b953a-107">DESCRIPTION</span></span>
<span data-ttu-id="b953a-108">Das Cmdlet " **Get-AzCosmosDBSqlTrigger** " Ruft die Liste aller vorhandenen CosmosDB-SQL-Trigger für einen angegebenen ResourceGroupName, Accountname, DatabaseName und Containername ab und Ruft einen einzelnen CosmosDB-SQL-Trigger für einen bestimmten ResourceGroupName, Accountname, DatabaseName, Containername und Triggername ab.</span><span class="sxs-lookup"><span data-stu-id="b953a-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="b953a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b953a-109">EXAMPLES</span></span>

### <span data-ttu-id="b953a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b953a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="b953a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b953a-111">PARAMETERS</span></span>

### <span data-ttu-id="b953a-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b953a-112">-AccountName</span></span>
<span data-ttu-id="b953a-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b953a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b953a-114">-Containername</span><span class="sxs-lookup"><span data-stu-id="b953a-114">-ContainerName</span></span>
<span data-ttu-id="b953a-115">Container Name.</span><span class="sxs-lookup"><span data-stu-id="b953a-115">Container name.</span></span>

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

### <span data-ttu-id="b953a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b953a-116">-DatabaseName</span></span>
<span data-ttu-id="b953a-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b953a-117">Database name.</span></span>

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

### <span data-ttu-id="b953a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b953a-118">-DefaultProfile</span></span>
<span data-ttu-id="b953a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b953a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b953a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b953a-120">-Name</span></span>
<span data-ttu-id="b953a-121">Name des Triggers</span><span class="sxs-lookup"><span data-stu-id="b953a-121">Trigger name.</span></span>

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

### <span data-ttu-id="b953a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b953a-122">-ParentObject</span></span>
<span data-ttu-id="b953a-123">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="b953a-123">Sql Container object.</span></span>

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

### <span data-ttu-id="b953a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b953a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b953a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b953a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b953a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b953a-126">CommonParameters</span></span>
<span data-ttu-id="b953a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b953a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b953a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b953a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b953a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b953a-129">INPUTS</span></span>

### <span data-ttu-id="b953a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="b953a-130">None</span></span>

## <span data-ttu-id="b953a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b953a-131">OUTPUTS</span></span>

### <span data-ttu-id="b953a-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="b953a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="b953a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b953a-133">NOTES</span></span>

## <span data-ttu-id="b953a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b953a-134">RELATED LINKS</span></span>
