---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995253"
---
# <span data-ttu-id="36215-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="36215-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="36215-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36215-102">SYNOPSIS</span></span>
<span data-ttu-id="36215-103">Erstellt eine neue oder aktualisiert eine vorhandene CosmosDB SQL-StoredProcedure Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="36215-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="36215-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36215-104">SYNTAX</span></span>

### <span data-ttu-id="36215-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36215-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36215-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36215-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36215-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36215-107">DESCRIPTION</span></span>
<span data-ttu-id="36215-108">Das Cmdlet " **Satz-AzCosmosDBSqlStoredProcedure** " erstellt eine neue oder aktualisiert eine vorhandene CosmosDB SQL-StoredProcedure Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="36215-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="36215-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36215-109">EXAMPLES</span></span>

### <span data-ttu-id="36215-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36215-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="36215-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="36215-111">PARAMETERS</span></span>

### <span data-ttu-id="36215-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="36215-112">-AccountName</span></span>
<span data-ttu-id="36215-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="36215-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36215-114">-Body</span><span class="sxs-lookup"><span data-stu-id="36215-114">-Body</span></span>
<span data-ttu-id="36215-115">Der Text der gespeicherten Prozedur.</span><span class="sxs-lookup"><span data-stu-id="36215-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="36215-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36215-116">-Confirm</span></span>
<span data-ttu-id="36215-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36215-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36215-118">-Containername</span><span class="sxs-lookup"><span data-stu-id="36215-118">-ContainerName</span></span>
<span data-ttu-id="36215-119">Container Name.</span><span class="sxs-lookup"><span data-stu-id="36215-119">Container name.</span></span>

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

### <span data-ttu-id="36215-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36215-120">-DatabaseName</span></span>
<span data-ttu-id="36215-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="36215-121">Database name.</span></span>

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

### <span data-ttu-id="36215-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36215-122">-DefaultProfile</span></span>
<span data-ttu-id="36215-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36215-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36215-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36215-124">-InputObject</span></span>
<span data-ttu-id="36215-125">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="36215-125">Sql Container object.</span></span>

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

### <span data-ttu-id="36215-126">-Name</span><span class="sxs-lookup"><span data-stu-id="36215-126">-Name</span></span>
<span data-ttu-id="36215-127">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="36215-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="36215-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36215-128">-ResourceGroupName</span></span>
<span data-ttu-id="36215-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="36215-129">Name of resource group.</span></span>

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

### <span data-ttu-id="36215-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36215-130">-WhatIf</span></span>
<span data-ttu-id="36215-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36215-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36215-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36215-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36215-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36215-133">CommonParameters</span></span>
<span data-ttu-id="36215-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36215-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36215-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36215-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36215-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36215-136">INPUTS</span></span>

### <span data-ttu-id="36215-137">Keine</span><span class="sxs-lookup"><span data-stu-id="36215-137">None</span></span>

## <span data-ttu-id="36215-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36215-138">OUTPUTS</span></span>

### <span data-ttu-id="36215-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="36215-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="36215-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="36215-140">NOTES</span></span>

## <span data-ttu-id="36215-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36215-141">RELATED LINKS</span></span>
