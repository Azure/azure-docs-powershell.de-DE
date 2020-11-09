---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299140"
---
# <span data-ttu-id="a102f-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a102f-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="a102f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a102f-102">SYNOPSIS</span></span>
<span data-ttu-id="a102f-103">Löscht die CosmosDB SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a102f-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a102f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a102f-104">SYNTAX</span></span>

### <span data-ttu-id="a102f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a102f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a102f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a102f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a102f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a102f-107">DESCRIPTION</span></span>
<span data-ttu-id="a102f-108">Das Cmdlet **Remove-AzCosmosDBSqlDatabase** löscht die CosmosDB-SQL-Datenbank, die den angegebenen ResourceGroupName, Accountname und DATABASENAME entspricht.</span><span class="sxs-lookup"><span data-stu-id="a102f-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="a102f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a102f-109">EXAMPLES</span></span>

### <span data-ttu-id="a102f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a102f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="a102f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a102f-111">PARAMETERS</span></span>

### <span data-ttu-id="a102f-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a102f-112">-AccountName</span></span>
<span data-ttu-id="a102f-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="a102f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a102f-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a102f-114">-Confirm</span></span>
<span data-ttu-id="a102f-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a102f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a102f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a102f-116">-DefaultProfile</span></span>
<span data-ttu-id="a102f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a102f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a102f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a102f-118">-InputObject</span></span>
<span data-ttu-id="a102f-119">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="a102f-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a102f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a102f-120">-Name</span></span>
<span data-ttu-id="a102f-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="a102f-121">Database name.</span></span>

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

### <span data-ttu-id="a102f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a102f-122">-PassThru</span></span>
<span data-ttu-id="a102f-123">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="a102f-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a102f-124">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a102f-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a102f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a102f-125">-ResourceGroupName</span></span>
<span data-ttu-id="a102f-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a102f-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a102f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a102f-127">-WhatIf</span></span>
<span data-ttu-id="a102f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a102f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a102f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a102f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a102f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a102f-130">CommonParameters</span></span>
<span data-ttu-id="a102f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a102f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a102f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a102f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a102f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a102f-133">INPUTS</span></span>

### <span data-ttu-id="a102f-134">Keine</span><span class="sxs-lookup"><span data-stu-id="a102f-134">None</span></span>

## <span data-ttu-id="a102f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a102f-135">OUTPUTS</span></span>

### <span data-ttu-id="a102f-136">System. void</span><span class="sxs-lookup"><span data-stu-id="a102f-136">System.Void</span></span>

### <span data-ttu-id="a102f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a102f-137">System.Boolean</span></span>

## <span data-ttu-id="a102f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a102f-138">NOTES</span></span>

## <span data-ttu-id="a102f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a102f-139">RELATED LINKS</span></span>
