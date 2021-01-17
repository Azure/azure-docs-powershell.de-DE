---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374659"
---
# <span data-ttu-id="cf8a4-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf8a4-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="cf8a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8a4-103">Entfernt eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="cf8a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf8a4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf8a4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8a4-106">Das **Cmdlet "Remove-AzSqlDatabase"** entfernt eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="cf8a4-107">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cf8a4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf8a4-108">EXAMPLES</span></span>

### <span data-ttu-id="cf8a4-109">Beispiel 1: Entfernen einer Datenbank von einem Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cf8a4-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="cf8a4-110">Mit diesem Befehl wird die Datenbank mit dem Namen "Database01" von Server Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="cf8a4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf8a4-111">PARAMETERS</span></span>

### <span data-ttu-id="cf8a4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf8a4-112">-DatabaseName</span></span>
<span data-ttu-id="cf8a4-113">Gibt den Namen der Datenbank an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8a4-114">-DefaultProfile</span></span>
<span data-ttu-id="cf8a4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cf8a4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf8a4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cf8a4-116">-Force</span></span>
<span data-ttu-id="cf8a4-117">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf8a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf8a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="cf8a4-119">Gibt den Namen der Azure-Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cf8a4-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cf8a4-120">-ServerName</span></span>
<span data-ttu-id="cf8a4-121">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="cf8a4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf8a4-122">-Confirm</span></span>
<span data-ttu-id="cf8a4-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf8a4-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cf8a4-124">-WhatIf</span></span>
<span data-ttu-id="cf8a4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf8a4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf8a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8a4-127">CommonParameters</span></span>
<span data-ttu-id="cf8a4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8a4-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf8a4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8a4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf8a4-130">INPUTS</span></span>

### <span data-ttu-id="cf8a4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cf8a4-131">System.String</span></span>

## <span data-ttu-id="cf8a4-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf8a4-132">OUTPUTS</span></span>

### <span data-ttu-id="cf8a4-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cf8a4-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cf8a4-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf8a4-134">NOTES</span></span>

## <span data-ttu-id="cf8a4-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf8a4-135">RELATED LINKS</span></span>

[<span data-ttu-id="cf8a4-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf8a4-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="cf8a4-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf8a4-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="cf8a4-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf8a4-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="cf8a4-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf8a4-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="cf8a4-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cf8a4-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="cf8a4-141">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="cf8a4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


