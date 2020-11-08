---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174398"
---
# <span data-ttu-id="7af92-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="7af92-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="7af92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7af92-102">SYNOPSIS</span></span>
<span data-ttu-id="7af92-103">Löscht das CosmosDB SQL-StoredProcedure Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="7af92-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="7af92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7af92-104">SYNTAX</span></span>

### <span data-ttu-id="7af92-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7af92-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7af92-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7af92-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7af92-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7af92-107">DESCRIPTION</span></span>
<span data-ttu-id="7af92-108">Das Cmdlet **Remove-AzCosmosDBSqlStoredProcedure** löscht die CosmosDB SQL-StoredProcedure Befehlstyp, die den angegebenen ResourceGroupName, Accountname und DATABASENAME entspricht.</span><span class="sxs-lookup"><span data-stu-id="7af92-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="7af92-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7af92-109">EXAMPLES</span></span>

### <span data-ttu-id="7af92-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7af92-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="7af92-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7af92-111">PARAMETERS</span></span>

### <span data-ttu-id="7af92-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="7af92-112">-AccountName</span></span>
<span data-ttu-id="7af92-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="7af92-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7af92-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7af92-114">-Confirm</span></span>
<span data-ttu-id="7af92-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7af92-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7af92-116">-Containername</span><span class="sxs-lookup"><span data-stu-id="7af92-116">-ContainerName</span></span>
<span data-ttu-id="7af92-117">Container Name.</span><span class="sxs-lookup"><span data-stu-id="7af92-117">Container name.</span></span>

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

### <span data-ttu-id="7af92-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7af92-118">-DatabaseName</span></span>
<span data-ttu-id="7af92-119">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="7af92-119">Database name.</span></span>

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

### <span data-ttu-id="7af92-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af92-120">-DefaultProfile</span></span>
<span data-ttu-id="7af92-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7af92-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7af92-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7af92-122">-InputObject</span></span>
<span data-ttu-id="7af92-123">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="7af92-123">Sql Database object.</span></span>

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

### <span data-ttu-id="7af92-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7af92-124">-Name</span></span>
<span data-ttu-id="7af92-125">Gespeicherter Prcodecure-Name.</span><span class="sxs-lookup"><span data-stu-id="7af92-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="7af92-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7af92-126">-PassThru</span></span>
<span data-ttu-id="7af92-127">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="7af92-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="7af92-128">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7af92-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="7af92-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af92-129">-ResourceGroupName</span></span>
<span data-ttu-id="7af92-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7af92-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7af92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7af92-131">-WhatIf</span></span>
<span data-ttu-id="7af92-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7af92-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7af92-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7af92-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7af92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af92-134">CommonParameters</span></span>
<span data-ttu-id="7af92-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af92-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7af92-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af92-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7af92-137">INPUTS</span></span>

### <span data-ttu-id="7af92-138">Keine</span><span class="sxs-lookup"><span data-stu-id="7af92-138">None</span></span>

## <span data-ttu-id="7af92-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7af92-139">OUTPUTS</span></span>

### <span data-ttu-id="7af92-140">System. void</span><span class="sxs-lookup"><span data-stu-id="7af92-140">System.Void</span></span>

### <span data-ttu-id="7af92-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7af92-141">System.Boolean</span></span>

## <span data-ttu-id="7af92-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="7af92-142">NOTES</span></span>

## <span data-ttu-id="7af92-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7af92-143">RELATED LINKS</span></span>
