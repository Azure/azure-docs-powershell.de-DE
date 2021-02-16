---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150588"
---
# <span data-ttu-id="b8b3f-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b3f-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="b8b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b3f-103">Ruft eine kurzfristige Aufbewahrungsrichtlinie für eine Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="b8b3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8b3f-104">SYNTAX</span></span>

### <span data-ttu-id="b8b3f-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8b3f-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8b3f-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8b3f-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8b3f-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8b3f-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8b3f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8b3f-108">DESCRIPTION</span></span>
<span data-ttu-id="b8b3f-109">Das **Cmdlet "Get-AzSqlDatabaseBackupShortTermRetentionPolicy"** ruft die kurzfristige Aufbewahrungsrichtlinie ab, die in dieser Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="b8b3f-110">Die Richtlinie ist der Aufbewahrungszeitraum (in Tagen) für Point-in-Time-Wiederherstellungssicherungen.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="b8b3f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8b3f-111">EXAMPLES</span></span>

### <span data-ttu-id="b8b3f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8b3f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="b8b3f-113">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 ab.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="b8b3f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b8b3f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="b8b3f-115">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 über die Piping in einem Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="b8b3f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b3f-116">PARAMETERS</span></span>

### <span data-ttu-id="b8b3f-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b8b3f-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="b8b3f-118">Das Datenbankobjekt, für das die Richtlinie erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8b3f-119">-DatabaseName</span></span>
<span data-ttu-id="b8b3f-120">Der Name der Azure SQL Zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b3f-121">-DefaultProfile</span></span>
<span data-ttu-id="b8b3f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8b3f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b3f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8b3f-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8b3f-125">-ResourceId</span></span>
<span data-ttu-id="b8b3f-126">Die ressourcen-ID der kurzfristigen Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3f-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8b3f-127">-ServerName</span></span>
<span data-ttu-id="b8b3f-128">Der Name des Azure-SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b3f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b3f-129">CommonParameters</span></span>
<span data-ttu-id="b8b3f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b3f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b3f-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8b3f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b3f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b3f-132">INPUTS</span></span>

### <span data-ttu-id="b8b3f-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b8b3f-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="b8b3f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b8b3f-134">System.String</span></span>

## <span data-ttu-id="b8b3f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b3f-135">OUTPUTS</span></span>

### <span data-ttu-id="b8b3f-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b8b3f-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b8b3f-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8b3f-137">NOTES</span></span>

## <span data-ttu-id="b8b3f-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8b3f-138">RELATED LINKS</span></span>
