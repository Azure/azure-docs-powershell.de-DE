---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298978"
---
# <span data-ttu-id="e1f42-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="e1f42-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="e1f42-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1f42-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f42-103">Aktualisiert das CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="e1f42-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="e1f42-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen UserDefinedFunction aus.</span><span class="sxs-lookup"><span data-stu-id="e1f42-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="e1f42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1f42-105">SYNTAX</span></span>

### <span data-ttu-id="e1f42-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1f42-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f42-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1f42-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f42-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1f42-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1f42-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1f42-109">DESCRIPTION</span></span>
<span data-ttu-id="e1f42-110">Aktualisiert das CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="e1f42-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="e1f42-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen UserDefinedFunction aus.</span><span class="sxs-lookup"><span data-stu-id="e1f42-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="e1f42-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1f42-112">EXAMPLES</span></span>

### <span data-ttu-id="e1f42-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1f42-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="e1f42-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1f42-114">PARAMETERS</span></span>

### <span data-ttu-id="e1f42-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="e1f42-115">-AccountName</span></span>
<span data-ttu-id="e1f42-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="e1f42-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e1f42-117">-Body</span><span class="sxs-lookup"><span data-stu-id="e1f42-117">-Body</span></span>
<span data-ttu-id="e1f42-118">Der Text der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1f42-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="e1f42-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1f42-119">-Confirm</span></span>
<span data-ttu-id="e1f42-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1f42-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1f42-121">-Containername</span><span class="sxs-lookup"><span data-stu-id="e1f42-121">-ContainerName</span></span>
<span data-ttu-id="e1f42-122">Container Name.</span><span class="sxs-lookup"><span data-stu-id="e1f42-122">Container name.</span></span>

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

### <span data-ttu-id="e1f42-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1f42-123">-DatabaseName</span></span>
<span data-ttu-id="e1f42-124">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="e1f42-124">Database name.</span></span>

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

### <span data-ttu-id="e1f42-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f42-125">-DefaultProfile</span></span>
<span data-ttu-id="e1f42-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1f42-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f42-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e1f42-127">-InputObject</span></span>
<span data-ttu-id="e1f42-128">SQL-benutzerdefiniertes Funktionsobjekt</span><span class="sxs-lookup"><span data-stu-id="e1f42-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f42-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e1f42-129">-Name</span></span>
<span data-ttu-id="e1f42-130">Name der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1f42-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="e1f42-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e1f42-131">-ParentObject</span></span>
<span data-ttu-id="e1f42-132">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1f42-132">Sql Container object.</span></span>

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

### <span data-ttu-id="e1f42-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f42-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1f42-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1f42-134">Name of resource group.</span></span>

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

### <span data-ttu-id="e1f42-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f42-135">-WhatIf</span></span>
<span data-ttu-id="e1f42-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1f42-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1f42-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1f42-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1f42-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f42-138">CommonParameters</span></span>
<span data-ttu-id="e1f42-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f42-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f42-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1f42-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f42-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1f42-141">INPUTS</span></span>

### <span data-ttu-id="e1f42-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e1f42-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e1f42-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="e1f42-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="e1f42-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1f42-144">OUTPUTS</span></span>

### <span data-ttu-id="e1f42-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="e1f42-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="e1f42-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e1f42-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e1f42-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1f42-147">NOTES</span></span>

## <span data-ttu-id="e1f42-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1f42-148">RELATED LINKS</span></span>
