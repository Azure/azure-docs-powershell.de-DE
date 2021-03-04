---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0334f022266843290f56fa8ee635634bce7caa56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929768"
---
# <span data-ttu-id="283f2-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="283f2-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="283f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="283f2-102">SYNOPSIS</span></span>
<span data-ttu-id="283f2-103">Ruft eine kurzfristige Sicherungsaufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="283f2-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="283f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="283f2-104">SYNTAX</span></span>

### <span data-ttu-id="283f2-105">PolicyByResourceInstanceDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="283f2-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="283f2-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="283f2-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="283f2-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="283f2-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="283f2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="283f2-108">DESCRIPTION</span></span>
<span data-ttu-id="283f2-109">Das **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy-Cmdlet** ruft die kurzfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="283f2-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="283f2-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Punkt-in-Zeit-Wiederherstellungssicherungen.</span><span class="sxs-lookup"><span data-stu-id="283f2-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="283f2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="283f2-111">EXAMPLES</span></span>

### <span data-ttu-id="283f2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="283f2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="283f2-113">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für datenbank01 ab.</span><span class="sxs-lookup"><span data-stu-id="283f2-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="283f2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="283f2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="283f2-115">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für Datenbank01 über Piping in einem Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="283f2-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="283f2-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="283f2-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="283f2-117">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für alle gelöschten Datenbanken mit dem Namen "datenbank01" über Piping in einem gelöschten Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="283f2-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="283f2-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="283f2-118">PARAMETERS</span></span>

### <span data-ttu-id="283f2-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="283f2-119">-DatabaseName</span></span>
<span data-ttu-id="283f2-120">Der Name der Azure SQL-Instanzdatenbank, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="283f2-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283f2-121">-DefaultProfile</span></span>
<span data-ttu-id="283f2-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="283f2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="283f2-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="283f2-123">-DeletionDate</span></span>
<span data-ttu-id="283f2-124">Das Löschdatum der Azure SQL-Instanzdatenbank zum Abrufen von Sicherungen mit Millisekundengenauigkeit (z. B. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="283f2-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283f2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="283f2-125">-InputObject</span></span>
<span data-ttu-id="283f2-126">Das Live- oder gelöschte Datenbankobjekt, für das sie die Richtlinie erhalten/festlegen soll.</span><span class="sxs-lookup"><span data-stu-id="283f2-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="283f2-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="283f2-127">-InstanceName</span></span>
<span data-ttu-id="283f2-128">Der Name der azure SQL verwaltete Instanz, in der sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="283f2-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283f2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283f2-129">-ResourceGroupName</span></span>
<span data-ttu-id="283f2-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="283f2-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="283f2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="283f2-131">-ResourceId</span></span>
<span data-ttu-id="283f2-132">Die ressourcen-ID für die kurzfristige Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="283f2-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="283f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283f2-133">CommonParameters</span></span>
<span data-ttu-id="283f2-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283f2-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="283f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283f2-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="283f2-136">INPUTS</span></span>

### <span data-ttu-id="283f2-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="283f2-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="283f2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="283f2-138">System.String</span></span>

## <span data-ttu-id="283f2-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="283f2-139">OUTPUTS</span></span>

### <span data-ttu-id="283f2-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="283f2-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="283f2-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="283f2-141">NOTES</span></span>

## <span data-ttu-id="283f2-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="283f2-142">RELATED LINKS</span></span>
