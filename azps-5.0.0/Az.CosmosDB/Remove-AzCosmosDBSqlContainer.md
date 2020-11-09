---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299146"
---
# <span data-ttu-id="2c3b8-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2c3b8-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2c3b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3b8-103">Löscht den CosmosDB-SQL-Container.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2c3b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c3b8-104">SYNTAX</span></span>

### <span data-ttu-id="2c3b8-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c3b8-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c3b8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3b8-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c3b8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c3b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2c3b8-108">Das Cmdlet **Remove-AzCosmosDBSqlContainer** löscht den CosmosDB-SQL-Container, der den angegebenen ResourceGroupName, Accountname, DatabaseName und Containername entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="2c3b8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c3b8-109">EXAMPLES</span></span>

### <span data-ttu-id="2c3b8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c3b8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="2c3b8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c3b8-111">PARAMETERS</span></span>

### <span data-ttu-id="2c3b8-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="2c3b8-112">-AccountName</span></span>
<span data-ttu-id="2c3b8-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2c3b8-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c3b8-114">-Confirm</span></span>
<span data-ttu-id="2c3b8-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3b8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c3b8-116">-DatabaseName</span></span>
<span data-ttu-id="2c3b8-117">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="2c3b8-117">Database name.</span></span>

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

### <span data-ttu-id="2c3b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3b8-118">-DefaultProfile</span></span>
<span data-ttu-id="2c3b8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c3b8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c3b8-120">-InputObject</span></span>
<span data-ttu-id="2c3b8-121">SQL-Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3b8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2c3b8-122">-Name</span></span>
<span data-ttu-id="2c3b8-123">Container Name.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-123">Container name.</span></span>

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

### <span data-ttu-id="2c3b8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c3b8-124">-PassThru</span></span>
<span data-ttu-id="2c3b8-125">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="2c3b8-126">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="2c3b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c3b8-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2c3b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3b8-129">-WhatIf</span></span>
<span data-ttu-id="2c3b8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3b8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3b8-132">CommonParameters</span></span>
<span data-ttu-id="2c3b8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3b8-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c3b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3b8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c3b8-135">INPUTS</span></span>

### <span data-ttu-id="2c3b8-136">Keine</span><span class="sxs-lookup"><span data-stu-id="2c3b8-136">None</span></span>

## <span data-ttu-id="2c3b8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c3b8-137">OUTPUTS</span></span>

### <span data-ttu-id="2c3b8-138">System. void</span><span class="sxs-lookup"><span data-stu-id="2c3b8-138">System.Void</span></span>

### <span data-ttu-id="2c3b8-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c3b8-139">System.Boolean</span></span>

## <span data-ttu-id="2c3b8-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c3b8-140">NOTES</span></span>

## <span data-ttu-id="2c3b8-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c3b8-141">RELATED LINKS</span></span>
