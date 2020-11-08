---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176898"
---
# <span data-ttu-id="66357-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="66357-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="66357-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66357-102">SYNOPSIS</span></span>
<span data-ttu-id="66357-103">Ruft eine Datenbank-langfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="66357-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="66357-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66357-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66357-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66357-105">DESCRIPTION</span></span>
<span data-ttu-id="66357-106">Das Cmdlet " **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** " Ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="66357-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="66357-107">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66357-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="66357-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66357-108">EXAMPLES</span></span>

### <span data-ttu-id="66357-109">Beispiel 1: Abrufen der aktuellen Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="66357-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="66357-110">Dieser Befehl ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für database01 ab.</span><span class="sxs-lookup"><span data-stu-id="66357-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="66357-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="66357-111">PARAMETERS</span></span>

### <span data-ttu-id="66357-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66357-112">-DatabaseName</span></span>
<span data-ttu-id="66357-113">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="66357-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="66357-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66357-114">-DefaultProfile</span></span>
<span data-ttu-id="66357-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66357-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66357-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66357-116">-ResourceGroupName</span></span>
<span data-ttu-id="66357-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66357-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="66357-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="66357-118">-ServerName</span></span>
<span data-ttu-id="66357-119">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="66357-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="66357-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66357-120">-Confirm</span></span>
<span data-ttu-id="66357-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66357-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66357-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66357-122">-WhatIf</span></span>
<span data-ttu-id="66357-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66357-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66357-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66357-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66357-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66357-125">CommonParameters</span></span>
<span data-ttu-id="66357-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66357-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66357-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66357-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66357-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66357-128">INPUTS</span></span>

### <span data-ttu-id="66357-129">System. String</span><span class="sxs-lookup"><span data-stu-id="66357-129">System.String</span></span>

## <span data-ttu-id="66357-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66357-130">OUTPUTS</span></span>

### <span data-ttu-id="66357-131">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="66357-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="66357-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="66357-132">NOTES</span></span>

## <span data-ttu-id="66357-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66357-133">RELATED LINKS</span></span>

[<span data-ttu-id="66357-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="66357-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="66357-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="66357-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="66357-136">Satz-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="66357-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="66357-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="66357-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)