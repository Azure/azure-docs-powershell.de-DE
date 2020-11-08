---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166061"
---
# <span data-ttu-id="ec799-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec799-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="ec799-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec799-102">SYNOPSIS</span></span>
<span data-ttu-id="ec799-103">Ruft eine kurzfristige Aufbewahrungsrichtlinie für Backups ab.</span><span class="sxs-lookup"><span data-stu-id="ec799-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="ec799-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec799-104">SYNTAX</span></span>

### <span data-ttu-id="ec799-105">PolicyByResourceServerDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec799-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec799-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ec799-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec799-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ec799-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec799-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec799-108">DESCRIPTION</span></span>
<span data-ttu-id="ec799-109">Das Cmdlet " **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** " Ruft die für diese Datenbank registrierte kurzfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="ec799-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="ec799-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Point-in-Time-Wiederherstellungs Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="ec799-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="ec799-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec799-111">EXAMPLES</span></span>

### <span data-ttu-id="ec799-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec799-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="ec799-113">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für database01 ab.</span><span class="sxs-lookup"><span data-stu-id="ec799-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="ec799-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ec799-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="ec799-115">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für database01 über die Rohrverlegung in einem Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="ec799-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="ec799-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec799-116">PARAMETERS</span></span>

### <span data-ttu-id="ec799-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ec799-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="ec799-118">Das Datenbankobjekt, für das die Richtlinie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec799-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="ec799-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec799-119">-DatabaseName</span></span>
<span data-ttu-id="ec799-120">Der Name der zu verwendenden Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ec799-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="ec799-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec799-121">-DefaultProfile</span></span>
<span data-ttu-id="ec799-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec799-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec799-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec799-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec799-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec799-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec799-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ec799-125">-ResourceId</span></span>
<span data-ttu-id="ec799-126">Die Ressourcen-ID für kurzfristige Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="ec799-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="ec799-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="ec799-127">-ServerName</span></span>
<span data-ttu-id="ec799-128">Der Name des Azure SQL Server, in dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ec799-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="ec799-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec799-129">CommonParameters</span></span>
<span data-ttu-id="ec799-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec799-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec799-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec799-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec799-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec799-132">INPUTS</span></span>

### <span data-ttu-id="ec799-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ec799-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="ec799-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ec799-134">System.String</span></span>

## <span data-ttu-id="ec799-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec799-135">OUTPUTS</span></span>

### <span data-ttu-id="ec799-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ec799-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="ec799-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec799-137">NOTES</span></span>

## <span data-ttu-id="ec799-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec799-138">RELATED LINKS</span></span>
