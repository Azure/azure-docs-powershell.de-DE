---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003820"
---
# <span data-ttu-id="09fb8-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09fb8-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="09fb8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="09fb8-103">Löscht die CosmosDB SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="09fb8-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="09fb8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09fb8-104">SYNTAX</span></span>

### <span data-ttu-id="09fb8-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09fb8-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09fb8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09fb8-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fb8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="09fb8-108">Das Cmdlet **Remove-AzCosmosDBSqlDatabase** löscht die CosmosDB-SQL-Datenbank, die den angegebenen ResourceGroupName, Accountname und DATABASENAME entspricht.</span><span class="sxs-lookup"><span data-stu-id="09fb8-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="09fb8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09fb8-109">EXAMPLES</span></span>

### <span data-ttu-id="09fb8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09fb8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="09fb8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="09fb8-111">PARAMETERS</span></span>

### <span data-ttu-id="09fb8-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="09fb8-112">-AccountName</span></span>
<span data-ttu-id="09fb8-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="09fb8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09fb8-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09fb8-114">-Confirm</span></span>
<span data-ttu-id="09fb8-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09fb8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09fb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fb8-116">-DefaultProfile</span></span>
<span data-ttu-id="09fb8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09fb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09fb8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09fb8-118">-InputObject</span></span>
<span data-ttu-id="09fb8-119">SQL-Datenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="09fb8-119">Sql Database object.</span></span>

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

### <span data-ttu-id="09fb8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="09fb8-120">-Name</span></span>
<span data-ttu-id="09fb8-121">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="09fb8-121">Database name.</span></span>

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

### <span data-ttu-id="09fb8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09fb8-122">-PassThru</span></span>
<span data-ttu-id="09fb8-123">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="09fb8-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="09fb8-124">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="09fb8-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="09fb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="09fb8-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09fb8-126">Name of resource group.</span></span>

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

### <span data-ttu-id="09fb8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fb8-127">-WhatIf</span></span>
<span data-ttu-id="09fb8-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09fb8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09fb8-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09fb8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09fb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fb8-130">CommonParameters</span></span>
<span data-ttu-id="09fb8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fb8-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09fb8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fb8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09fb8-133">INPUTS</span></span>

### <span data-ttu-id="09fb8-134">Keine</span><span class="sxs-lookup"><span data-stu-id="09fb8-134">None</span></span>

## <span data-ttu-id="09fb8-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09fb8-135">OUTPUTS</span></span>

### <span data-ttu-id="09fb8-136">System. void</span><span class="sxs-lookup"><span data-stu-id="09fb8-136">System.Void</span></span>

### <span data-ttu-id="09fb8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09fb8-137">System.Boolean</span></span>

## <span data-ttu-id="09fb8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="09fb8-138">NOTES</span></span>

## <span data-ttu-id="09fb8-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09fb8-139">RELATED LINKS</span></span>
