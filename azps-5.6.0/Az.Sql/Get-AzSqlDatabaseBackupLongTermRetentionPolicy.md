---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b0f3f657caea0da29ecf78baff15fe0afb7008ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926376"
---
# <span data-ttu-id="8d4ee-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d4ee-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="8d4ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4ee-103">Ruft eine datenbank langfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="8d4ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d4ee-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d4ee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4ee-106">Das **Get-AzSqlDatabaseBackupLongTermRetentionPolicy-Cmdlet** ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="8d4ee-107">Die Richtlinie ist eine Azure Backup-Ressource, die zum Definieren der Sicherungsspeicherrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="8d4ee-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d4ee-108">EXAMPLES</span></span>

### <span data-ttu-id="8d4ee-109">Beispiel 1: Holen Sie sich die aktuelle Version der langfristigen Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="8d4ee-110">Dieser Befehl ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für Datenbank ab01</span><span class="sxs-lookup"><span data-stu-id="8d4ee-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="8d4ee-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d4ee-111">PARAMETERS</span></span>

### <span data-ttu-id="8d4ee-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d4ee-112">-DatabaseName</span></span>
<span data-ttu-id="8d4ee-113">Der Name der azure SQL zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="8d4ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4ee-114">-DefaultProfile</span></span>
<span data-ttu-id="8d4ee-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d4ee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4ee-116">-ResourceGroupName</span></span>
<span data-ttu-id="8d4ee-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d4ee-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="8d4ee-118">-ServerName</span></span>
<span data-ttu-id="8d4ee-119">Der Name des Azure-SQL Server in der Datenbank enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="8d4ee-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d4ee-120">-Confirm</span></span>
<span data-ttu-id="8d4ee-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d4ee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4ee-122">-WhatIf</span></span>
<span data-ttu-id="8d4ee-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d4ee-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d4ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4ee-125">CommonParameters</span></span>
<span data-ttu-id="8d4ee-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4ee-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d4ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4ee-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d4ee-128">INPUTS</span></span>

### <span data-ttu-id="8d4ee-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8d4ee-129">System.String</span></span>

## <span data-ttu-id="8d4ee-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d4ee-130">OUTPUTS</span></span>

### <span data-ttu-id="8d4ee-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8d4ee-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="8d4ee-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8d4ee-132">NOTES</span></span>

## <span data-ttu-id="8d4ee-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8d4ee-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d4ee-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8d4ee-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8d4ee-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8d4ee-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8d4ee-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d4ee-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8d4ee-137">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="8d4ee-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)