---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175284"
---
# <span data-ttu-id="caeec-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="caeec-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="caeec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="caeec-102">SYNOPSIS</span></span>
<span data-ttu-id="caeec-103">Löscht das CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="caeec-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="caeec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="caeec-104">SYNTAX</span></span>

### <span data-ttu-id="caeec-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="caeec-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caeec-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caeec-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caeec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="caeec-107">DESCRIPTION</span></span>
<span data-ttu-id="caeec-108">Das Cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** löscht die CosmosDB SQL-UserDefinedFunction, die den angegebenen ResourceGroupName, Accountname und DATABASENAME entspricht.</span><span class="sxs-lookup"><span data-stu-id="caeec-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="caeec-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="caeec-109">EXAMPLES</span></span>

### <span data-ttu-id="caeec-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="caeec-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="caeec-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="caeec-111">PARAMETERS</span></span>

### <span data-ttu-id="caeec-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="caeec-112">-AccountName</span></span>
<span data-ttu-id="caeec-113">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="caeec-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="caeec-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="caeec-114">-Confirm</span></span>
<span data-ttu-id="caeec-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="caeec-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caeec-116">-Containername</span><span class="sxs-lookup"><span data-stu-id="caeec-116">-ContainerName</span></span>
<span data-ttu-id="caeec-117">Container Name.</span><span class="sxs-lookup"><span data-stu-id="caeec-117">Container name.</span></span>

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

### <span data-ttu-id="caeec-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="caeec-118">-DatabaseName</span></span>
<span data-ttu-id="caeec-119">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="caeec-119">Database name.</span></span>

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

### <span data-ttu-id="caeec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caeec-120">-DefaultProfile</span></span>
<span data-ttu-id="caeec-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="caeec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caeec-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="caeec-122">-InputObject</span></span>
<span data-ttu-id="caeec-123">SQL-benutzerdefiniertes Funktionsobjekt</span><span class="sxs-lookup"><span data-stu-id="caeec-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="caeec-124">-Name</span><span class="sxs-lookup"><span data-stu-id="caeec-124">-Name</span></span>
<span data-ttu-id="caeec-125">Name der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="caeec-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="caeec-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caeec-126">-PassThru</span></span>
<span data-ttu-id="caeec-127">Auf "true" festgelegt werden, wenn der Benutzer eine Ausgabe empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="caeec-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="caeec-128">Die Ausgabe ist wahr, wenn der Vorgang erfolgreich war, und andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="caeec-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="caeec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caeec-129">-ResourceGroupName</span></span>
<span data-ttu-id="caeec-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="caeec-130">Name of resource group.</span></span>

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

### <span data-ttu-id="caeec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caeec-131">-WhatIf</span></span>
<span data-ttu-id="caeec-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="caeec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caeec-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="caeec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caeec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caeec-134">CommonParameters</span></span>
<span data-ttu-id="caeec-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caeec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caeec-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="caeec-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caeec-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="caeec-137">INPUTS</span></span>

### <span data-ttu-id="caeec-138">Keine</span><span class="sxs-lookup"><span data-stu-id="caeec-138">None</span></span>

## <span data-ttu-id="caeec-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="caeec-139">OUTPUTS</span></span>

### <span data-ttu-id="caeec-140">System. void</span><span class="sxs-lookup"><span data-stu-id="caeec-140">System.Void</span></span>

### <span data-ttu-id="caeec-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="caeec-141">System.Boolean</span></span>

## <span data-ttu-id="caeec-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="caeec-142">NOTES</span></span>

## <span data-ttu-id="caeec-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="caeec-143">RELATED LINKS</span></span>
