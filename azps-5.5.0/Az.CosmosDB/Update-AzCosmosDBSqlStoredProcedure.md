---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148452"
---
# <span data-ttu-id="795b5-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="795b5-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="795b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="795b5-102">SYNOPSIS</span></span>
<span data-ttu-id="795b5-103">Aktualisiert die Datenbankdatenbank Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="795b5-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="795b5-104">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene StoredProcedure gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="795b5-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="795b5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="795b5-105">SYNTAX</span></span>

### <span data-ttu-id="795b5-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="795b5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="795b5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="795b5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="795b5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="795b5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="795b5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="795b5-109">DESCRIPTION</span></span>
<span data-ttu-id="795b5-110">Aktualisiert die Datenbankdatenbank Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="795b5-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="795b5-111">Führt einen clientseitigen Patchvorgang durch, indem die vorhandene StoredProcedure gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="795b5-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="795b5-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="795b5-112">EXAMPLES</span></span>

### <span data-ttu-id="795b5-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="795b5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="795b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="795b5-114">PARAMETERS</span></span>

### <span data-ttu-id="795b5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="795b5-115">-AccountName</span></span>
<span data-ttu-id="795b5-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="795b5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="795b5-117">-Body</span><span class="sxs-lookup"><span data-stu-id="795b5-117">-Body</span></span>
<span data-ttu-id="795b5-118">Der Textkörper der gespeicherten Prozedur.</span><span class="sxs-lookup"><span data-stu-id="795b5-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="795b5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="795b5-119">-Confirm</span></span>
<span data-ttu-id="795b5-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="795b5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795b5-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="795b5-121">-ContainerName</span></span>
<span data-ttu-id="795b5-122">Containername.</span><span class="sxs-lookup"><span data-stu-id="795b5-122">Container name.</span></span>

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

### <span data-ttu-id="795b5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="795b5-123">-DatabaseName</span></span>
<span data-ttu-id="795b5-124">Datenbankname.</span><span class="sxs-lookup"><span data-stu-id="795b5-124">Database name.</span></span>

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

### <span data-ttu-id="795b5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795b5-125">-DefaultProfile</span></span>
<span data-ttu-id="795b5-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="795b5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795b5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="795b5-127">-InputObject</span></span>
<span data-ttu-id="795b5-128">Sql Stored Procedure Object</span><span class="sxs-lookup"><span data-stu-id="795b5-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="795b5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="795b5-129">-Name</span></span>
<span data-ttu-id="795b5-130">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="795b5-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="795b5-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="795b5-131">-ParentObject</span></span>
<span data-ttu-id="795b5-132">Sql Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="795b5-132">Sql Container object.</span></span>

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

### <span data-ttu-id="795b5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795b5-133">-ResourceGroupName</span></span>
<span data-ttu-id="795b5-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="795b5-134">Name of resource group.</span></span>

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

### <span data-ttu-id="795b5-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="795b5-135">-WhatIf</span></span>
<span data-ttu-id="795b5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="795b5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795b5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="795b5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795b5-138">CommonParameters</span></span>
<span data-ttu-id="795b5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795b5-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="795b5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795b5-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="795b5-141">INPUTS</span></span>

### <span data-ttu-id="795b5-142">Microsoft.Azure.Commands.ExesDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="795b5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="795b5-143">Microsoft.Azure.Commands.ExesDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="795b5-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="795b5-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="795b5-144">OUTPUTS</span></span>

### <span data-ttu-id="795b5-145">Microsoft.Azure.Commands.ExesDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="795b5-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="795b5-146">Microsoft.Azure.Commands.UmsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="795b5-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="795b5-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="795b5-147">NOTES</span></span>

## <span data-ttu-id="795b5-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="795b5-148">RELATED LINKS</span></span>
