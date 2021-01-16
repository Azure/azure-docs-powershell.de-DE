---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298627"
---
# <span data-ttu-id="0992e-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0992e-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="0992e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0992e-102">SYNOPSIS</span></span>
<span data-ttu-id="0992e-103">Ruft die unterschiedlichen Wiederherstellungspunkte ab, aus denen SQL Data Warehouse wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0992e-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="0992e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0992e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0992e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0992e-105">DESCRIPTION</span></span>
<span data-ttu-id="0992e-106">Das **Cmdlet "Get-AzSqlDatabaseRestorePoint"** ruft die unterschiedlichen Wiederherstellungspunkte ab, aus der ein Azure SQL Data Warehouse wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0992e-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="0992e-107">Bei einer Azure SQL-Datenbank ist das Fenster zum Wiederherstellen fortlaufend.</span><span class="sxs-lookup"><span data-stu-id="0992e-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="0992e-108">Dies bedeutet, dass jeder beliebige Zeitpunkt im Sicherungsaufbewahrungszeitraum der Datenbank als Wiederherstellungspunkt verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0992e-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="0992e-109">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0992e-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0992e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0992e-110">EXAMPLES</span></span>

### <span data-ttu-id="0992e-111">Beispiel 1: Alle Wiederherstellungspunkte erhalten</span><span class="sxs-lookup"><span data-stu-id="0992e-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="0992e-112">Dieser Befehl gibt alle verfügbaren Wiederherstellungspunkte für die Azure SQL Database01 zurück.</span><span class="sxs-lookup"><span data-stu-id="0992e-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="0992e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0992e-113">PARAMETERS</span></span>

### <span data-ttu-id="0992e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0992e-114">-DatabaseName</span></span>
<span data-ttu-id="0992e-115">Gibt den Namen der datenbank SQL an.</span><span class="sxs-lookup"><span data-stu-id="0992e-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="0992e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0992e-116">-DefaultProfile</span></span>
<span data-ttu-id="0992e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0992e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0992e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0992e-118">-ResourceGroupName</span></span>
<span data-ttu-id="0992e-119">Gibt den Namen der Ressourcengruppe an, der die SQL Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0992e-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="0992e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0992e-120">-ServerName</span></span>
<span data-ttu-id="0992e-121">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="0992e-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="0992e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0992e-122">-Confirm</span></span>
<span data-ttu-id="0992e-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0992e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0992e-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0992e-124">-WhatIf</span></span>
<span data-ttu-id="0992e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0992e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0992e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0992e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0992e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0992e-127">CommonParameters</span></span>
<span data-ttu-id="0992e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0992e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0992e-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0992e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0992e-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0992e-130">INPUTS</span></span>

### <span data-ttu-id="0992e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0992e-131">System.String</span></span>

## <span data-ttu-id="0992e-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0992e-132">OUTPUTS</span></span>

### <span data-ttu-id="0992e-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="0992e-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="0992e-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0992e-134">NOTES</span></span>

## <span data-ttu-id="0992e-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0992e-135">RELATED LINKS</span></span>
