---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663096"
---
# <span data-ttu-id="d6677-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6677-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d6677-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6677-102">SYNOPSIS</span></span>
<span data-ttu-id="d6677-103">Ruft eine Datenbank-langfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="d6677-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6677-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6677-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6677-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6677-105">DESCRIPTION</span></span>
<span data-ttu-id="d6677-106">Das Cmdlet " **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** " Ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d6677-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="d6677-107">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6677-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="d6677-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6677-108">EXAMPLES</span></span>

### <span data-ttu-id="d6677-109">Beispiel 1: Abrufen der aktuellen Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d6677-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="d6677-110">Dieser Befehl ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für database01 ab.</span><span class="sxs-lookup"><span data-stu-id="d6677-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="d6677-111">Beispiel 2: Abrufen der älteren Version der langfristigen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d6677-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="d6677-112">Dieser Befehl ruft die Legacy Version der langfristigen Aufbewahrungsrichtlinie für database01</span><span class="sxs-lookup"><span data-stu-id="d6677-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="d6677-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6677-113">PARAMETERS</span></span>

### <span data-ttu-id="d6677-114">-Current</span><span class="sxs-lookup"><span data-stu-id="d6677-114">-Current</span></span>
<span data-ttu-id="d6677-115">Wenn Sie nicht bereitgestellt wird, gibt der Befehl die Legacy Informationen zur langfristigen Aufbewahrungsrichtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="d6677-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="d6677-116">Andernfalls gibt der Befehl die aktuelle Version der langfristigen Aufbewahrungsrichtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="d6677-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6677-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6677-117">-DatabaseName</span></span>
<span data-ttu-id="d6677-118">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d6677-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="d6677-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6677-119">-DefaultProfile</span></span>
<span data-ttu-id="d6677-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6677-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6677-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6677-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6677-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d6677-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6677-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="d6677-123">-ServerName</span></span>
<span data-ttu-id="d6677-124">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="d6677-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="d6677-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6677-125">-Confirm</span></span>
<span data-ttu-id="d6677-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6677-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6677-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6677-127">-WhatIf</span></span>
<span data-ttu-id="d6677-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6677-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6677-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6677-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6677-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6677-130">CommonParameters</span></span>
<span data-ttu-id="d6677-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6677-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6677-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6677-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6677-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6677-133">INPUTS</span></span>

### <span data-ttu-id="d6677-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d6677-134">System.String</span></span>

## <span data-ttu-id="d6677-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6677-135">OUTPUTS</span></span>

### <span data-ttu-id="d6677-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d6677-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d6677-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6677-137">NOTES</span></span>

## <span data-ttu-id="d6677-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6677-138">RELATED LINKS</span></span>

[<span data-ttu-id="d6677-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d6677-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d6677-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d6677-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d6677-141">Satz-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6677-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d6677-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d6677-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
