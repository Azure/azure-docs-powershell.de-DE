---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 12b44d2045574b1d787dd0b2bdb70ec44b616ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939867"
---
# <span data-ttu-id="3adfb-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="3adfb-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="3adfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3adfb-102">SYNOPSIS</span></span>
<span data-ttu-id="3adfb-103">Ruft den Status von Datenbankvorgängen ab.</span><span class="sxs-lookup"><span data-stu-id="3adfb-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="3adfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3adfb-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3adfb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3adfb-105">DESCRIPTION</span></span>
<span data-ttu-id="3adfb-106">Das **Get-AzSqlDatabaseActivity-Cmdlet** erhält den Status von Datenbankvorgängen in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3adfb-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="3adfb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3adfb-107">EXAMPLES</span></span>

### <span data-ttu-id="3adfb-108">Beispiel 1: Status für alle SQL Datenbankinstanzen</span><span class="sxs-lookup"><span data-stu-id="3adfb-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="3adfb-109">Dieser Befehl gibt den Vorgangsstatus aller SQL Datenbankinstanzen in einem Pool mit dem Namen "ElasticPool01" zurück.</span><span class="sxs-lookup"><span data-stu-id="3adfb-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="3adfb-110">Beispiel 2: Status für alle SQL Datenbankvorgänge</span><span class="sxs-lookup"><span data-stu-id="3adfb-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3adfb-111">Dieser Befehl gibt den Status aller SQL Datenbankvorgänge in einer Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="3adfb-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="3adfb-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3adfb-112">PARAMETERS</span></span>

### <span data-ttu-id="3adfb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3adfb-113">-DatabaseName</span></span>
<span data-ttu-id="3adfb-114">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="3adfb-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3adfb-115">-DefaultProfile</span></span>
<span data-ttu-id="3adfb-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3adfb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3adfb-117">-ElasticPoolName</span></span>
<span data-ttu-id="3adfb-118">Gibt den Namen des Pools für die flexible Datenbank an, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="3adfb-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3adfb-119">-OperationId</span></span>
<span data-ttu-id="3adfb-120">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3adfb-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3adfb-121">-ResourceGroupName</span></span>
<span data-ttu-id="3adfb-122">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3adfb-122">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="3adfb-123">-ServerName</span></span>
<span data-ttu-id="3adfb-124">Gibt den Namen des Microsoft SQL Server an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="3adfb-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3adfb-125">-Confirm</span></span>
<span data-ttu-id="3adfb-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3adfb-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3adfb-127">-WhatIf</span></span>
<span data-ttu-id="3adfb-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3adfb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3adfb-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3adfb-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adfb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adfb-130">CommonParameters</span></span>
<span data-ttu-id="3adfb-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adfb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adfb-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3adfb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adfb-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3adfb-133">INPUTS</span></span>

### <span data-ttu-id="3adfb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3adfb-134">System.String</span></span>

### <span data-ttu-id="3adfb-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3adfb-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3adfb-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3adfb-136">OUTPUTS</span></span>

### <span data-ttu-id="3adfb-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="3adfb-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="3adfb-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3adfb-138">NOTES</span></span>

## <span data-ttu-id="3adfb-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3adfb-139">RELATED LINKS</span></span>
