---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 94efd633a64bd1437206a00b83d86cf09fc56036
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825695"
---
# <span data-ttu-id="11f74-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11f74-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="11f74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11f74-102">SYNOPSIS</span></span>
<span data-ttu-id="11f74-103">Ruft eine kurzfristige Aufbewahrungsrichtlinie für Backups ab.</span><span class="sxs-lookup"><span data-stu-id="11f74-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="11f74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11f74-104">SYNTAX</span></span>

### <span data-ttu-id="11f74-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="11f74-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f74-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11f74-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f74-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11f74-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11f74-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11f74-108">DESCRIPTION</span></span>
<span data-ttu-id="11f74-109">Das Cmdlet " **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** " Ruft die für diese Datenbank registrierte kurzfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="11f74-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="11f74-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Point-in-Time-Wiederherstellungs Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="11f74-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="11f74-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11f74-111">EXAMPLES</span></span>

### <span data-ttu-id="11f74-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11f74-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="11f74-113">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für database01 ab.</span><span class="sxs-lookup"><span data-stu-id="11f74-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="11f74-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="11f74-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="11f74-115">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für database01 über die Rohrverlegung in einem Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="11f74-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="11f74-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="11f74-116">PARAMETERS</span></span>

### <span data-ttu-id="11f74-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="11f74-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="11f74-118">Das Datenbankobjekt, für das die Richtlinie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="11f74-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="11f74-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11f74-119">-DatabaseName</span></span>
<span data-ttu-id="11f74-120">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="11f74-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="11f74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f74-121">-DefaultProfile</span></span>
<span data-ttu-id="11f74-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11f74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11f74-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f74-123">-ResourceGroupName</span></span>
<span data-ttu-id="11f74-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="11f74-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="11f74-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="11f74-125">-ResourceId</span></span>
<span data-ttu-id="11f74-126">Die Ressourcen-ID für kurzfristige Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="11f74-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="11f74-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="11f74-127">-ServerName</span></span>
<span data-ttu-id="11f74-128">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="11f74-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="11f74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f74-129">CommonParameters</span></span>
<span data-ttu-id="11f74-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f74-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11f74-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f74-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11f74-132">INPUTS</span></span>

### <span data-ttu-id="11f74-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="11f74-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="11f74-134">System. String</span><span class="sxs-lookup"><span data-stu-id="11f74-134">System.String</span></span>

## <span data-ttu-id="11f74-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11f74-135">OUTPUTS</span></span>

### <span data-ttu-id="11f74-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="11f74-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="11f74-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="11f74-137">NOTES</span></span>

## <span data-ttu-id="11f74-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11f74-138">RELATED LINKS</span></span>
