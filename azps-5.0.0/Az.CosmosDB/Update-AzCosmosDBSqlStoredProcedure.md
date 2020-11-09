---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298990"
---
# <span data-ttu-id="d743d-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="d743d-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="d743d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d743d-102">SYNOPSIS</span></span>
<span data-ttu-id="d743d-103">Aktualisiert das CosmosDB SQL-StoredProcedure Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="d743d-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="d743d-104">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen StoredProcedure Befehlstyp aus.</span><span class="sxs-lookup"><span data-stu-id="d743d-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="d743d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d743d-105">SYNTAX</span></span>

### <span data-ttu-id="d743d-106">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d743d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d743d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d743d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d743d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d743d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d743d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d743d-109">DESCRIPTION</span></span>
<span data-ttu-id="d743d-110">Aktualisiert das CosmosDB SQL-StoredProcedure Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="d743d-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="d743d-111">Führt einen clientseitigen Patch-Vorgang durchlesen der vorhandenen StoredProcedure Befehlstyp aus.</span><span class="sxs-lookup"><span data-stu-id="d743d-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="d743d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d743d-112">EXAMPLES</span></span>

### <span data-ttu-id="d743d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d743d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="d743d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d743d-114">PARAMETERS</span></span>

### <span data-ttu-id="d743d-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d743d-115">-AccountName</span></span>
<span data-ttu-id="d743d-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="d743d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d743d-117">-Body</span><span class="sxs-lookup"><span data-stu-id="d743d-117">-Body</span></span>
<span data-ttu-id="d743d-118">Der Text der gespeicherten Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d743d-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="d743d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d743d-119">-Confirm</span></span>
<span data-ttu-id="d743d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d743d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d743d-121">-Containername</span><span class="sxs-lookup"><span data-stu-id="d743d-121">-ContainerName</span></span>
<span data-ttu-id="d743d-122">Container Name.</span><span class="sxs-lookup"><span data-stu-id="d743d-122">Container name.</span></span>

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

### <span data-ttu-id="d743d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d743d-123">-DatabaseName</span></span>
<span data-ttu-id="d743d-124">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="d743d-124">Database name.</span></span>

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

### <span data-ttu-id="d743d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d743d-125">-DefaultProfile</span></span>
<span data-ttu-id="d743d-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d743d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d743d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d743d-127">-InputObject</span></span>
<span data-ttu-id="d743d-128">Gespeicherte SQL-Prozedur (Objekt)</span><span class="sxs-lookup"><span data-stu-id="d743d-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="d743d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d743d-129">-Name</span></span>
<span data-ttu-id="d743d-130">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="d743d-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="d743d-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d743d-131">-ParentObject</span></span>
<span data-ttu-id="d743d-132">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="d743d-132">Sql Container object.</span></span>

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

### <span data-ttu-id="d743d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d743d-133">-ResourceGroupName</span></span>
<span data-ttu-id="d743d-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d743d-134">Name of resource group.</span></span>

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

### <span data-ttu-id="d743d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d743d-135">-WhatIf</span></span>
<span data-ttu-id="d743d-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d743d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d743d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d743d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d743d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d743d-138">CommonParameters</span></span>
<span data-ttu-id="d743d-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d743d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d743d-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d743d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d743d-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d743d-141">INPUTS</span></span>

### <span data-ttu-id="d743d-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d743d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="d743d-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d743d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="d743d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d743d-144">OUTPUTS</span></span>

### <span data-ttu-id="d743d-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d743d-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="d743d-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d743d-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d743d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d743d-147">NOTES</span></span>

## <span data-ttu-id="d743d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d743d-148">RELATED LINKS</span></span>
