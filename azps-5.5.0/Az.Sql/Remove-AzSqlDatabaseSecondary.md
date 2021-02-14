---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163260"
---
# <span data-ttu-id="76109-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76109-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="76109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76109-102">SYNOPSIS</span></span>
<span data-ttu-id="76109-103">Beendet die Datenreplikation zwischen SQL Datenbank und der angegebenen sekundären Datenbank.</span><span class="sxs-lookup"><span data-stu-id="76109-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="76109-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76109-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76109-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76109-105">DESCRIPTION</span></span>
<span data-ttu-id="76109-106">Das **Cmdlet "Remove-AzSqlDatabaseSecondary"** erzwingt das Beenden einer Georeplikationsverknüpfung.</span><span class="sxs-lookup"><span data-stu-id="76109-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="76109-107">Dieses Cmdlet ersetzt das Stop-AzSqlDatabaseCopy Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76109-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="76109-108">Vor dem Beenden gibt es keine Replikationssynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="76109-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="76109-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76109-109">EXAMPLES</span></span>

## <span data-ttu-id="76109-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76109-110">PARAMETERS</span></span>

### <span data-ttu-id="76109-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76109-111">-DatabaseName</span></span>
<span data-ttu-id="76109-112">Gibt den Namen der primären Azure SQL-Datenbank an, die über die von diesem Cmdlet entfernte Replikationsverknüpfung verfügt.</span><span class="sxs-lookup"><span data-stu-id="76109-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76109-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76109-113">-DefaultProfile</span></span>
<span data-ttu-id="76109-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="76109-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76109-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76109-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="76109-116">Gibt den Namen der Partnerressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="76109-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="76109-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="76109-117">-PartnerServerName</span></span>
<span data-ttu-id="76109-118">Gibt den Namen des Partners an, SQL Server.</span><span class="sxs-lookup"><span data-stu-id="76109-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="76109-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76109-119">-ResourceGroupName</span></span>
<span data-ttu-id="76109-120">Gibt den Namen der Ressourcengruppe an, die der Replikationsverknüpfung zugeordnet ist, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76109-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="76109-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76109-121">-ServerName</span></span>
<span data-ttu-id="76109-122">Gibt den Namen des SQL Server an, das über die zu entfernende Replikationsverknüpfung verfügt.</span><span class="sxs-lookup"><span data-stu-id="76109-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="76109-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76109-123">-Confirm</span></span>
<span data-ttu-id="76109-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76109-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76109-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76109-125">-WhatIf</span></span>
<span data-ttu-id="76109-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76109-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76109-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76109-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76109-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76109-128">CommonParameters</span></span>
<span data-ttu-id="76109-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76109-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76109-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76109-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76109-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76109-131">INPUTS</span></span>

### <span data-ttu-id="76109-132">System.String</span><span class="sxs-lookup"><span data-stu-id="76109-132">System.String</span></span>

## <span data-ttu-id="76109-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76109-133">OUTPUTS</span></span>

### <span data-ttu-id="76109-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="76109-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="76109-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76109-135">NOTES</span></span>

## <span data-ttu-id="76109-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76109-136">RELATED LINKS</span></span>

[<span data-ttu-id="76109-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76109-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="76109-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76109-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="76109-139">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="76109-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
