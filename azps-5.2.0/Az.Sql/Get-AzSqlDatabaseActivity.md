---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361891"
---
# <span data-ttu-id="12e6c-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="12e6c-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="12e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="12e6c-103">Ruft den Status von Datenbankvorgängen ab.</span><span class="sxs-lookup"><span data-stu-id="12e6c-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="12e6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e6c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e6c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="12e6c-106">Das **Cmdlet "Get-AzSqlDatabaseActivity"** ruft den Status von Datenbankvorgängen in Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="12e6c-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="12e6c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="12e6c-108">Beispiel 1: Erhalten des Status für alle SQL Datenbankinstanzen</span><span class="sxs-lookup"><span data-stu-id="12e6c-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="12e6c-109">Dieser Befehl gibt den Vorgangsstatus aller SQL Datenbankinstanzen in einem Pool namens "Poolpool 1" zurück.</span><span class="sxs-lookup"><span data-stu-id="12e6c-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="12e6c-110">Beispiel 2: Erhalten des Status für alle SQL Datenbankvorgänge</span><span class="sxs-lookup"><span data-stu-id="12e6c-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="12e6c-111">Dieser Befehl gibt den Status aller SQL Datenbankvorgänge in einer Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="12e6c-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="12e6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e6c-112">PARAMETERS</span></span>

### <span data-ttu-id="12e6c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12e6c-113">-DatabaseName</span></span>
<span data-ttu-id="12e6c-114">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="12e6c-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="12e6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e6c-115">-DefaultProfile</span></span>
<span data-ttu-id="12e6c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12e6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12e6c-117">-PoolName</span><span class="sxs-lookup"><span data-stu-id="12e6c-117">-ElasticPoolName</span></span>
<span data-ttu-id="12e6c-118">Gibt den Namen des Datenbankpools des Datenbankbands an, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="12e6c-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="12e6c-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="12e6c-119">-OperationId</span></span>
<span data-ttu-id="12e6c-120">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="12e6c-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12e6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="12e6c-122">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="12e6c-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="12e6c-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12e6c-123">-ServerName</span></span>
<span data-ttu-id="12e6c-124">Gibt den Namen des Microsoft SQL Server an, das die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="12e6c-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="12e6c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12e6c-125">-Confirm</span></span>
<span data-ttu-id="12e6c-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12e6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e6c-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="12e6c-127">-WhatIf</span></span>
<span data-ttu-id="12e6c-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12e6c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e6c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12e6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e6c-130">CommonParameters</span></span>
<span data-ttu-id="12e6c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e6c-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e6c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e6c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e6c-133">INPUTS</span></span>

### <span data-ttu-id="12e6c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="12e6c-134">System.String</span></span>

### <span data-ttu-id="12e6c-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12e6c-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="12e6c-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e6c-136">OUTPUTS</span></span>

### <span data-ttu-id="12e6c-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="12e6c-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="12e6c-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12e6c-138">NOTES</span></span>

## <span data-ttu-id="12e6c-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12e6c-139">RELATED LINKS</span></span>
