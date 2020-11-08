---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173456"
---
# <span data-ttu-id="3ac9b-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3ac9b-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="3ac9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ac9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac9b-103">Ruft eine kurzfristige Aufbewahrungsrichtlinie für Backups ab.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="3ac9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ac9b-104">SYNTAX</span></span>

### <span data-ttu-id="3ac9b-105">PolicyByResourceInstanceDatabaseSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ac9b-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac9b-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ac9b-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ac9b-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3ac9b-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac9b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ac9b-108">DESCRIPTION</span></span>
<span data-ttu-id="3ac9b-109">Das Cmdlet " **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** " Ruft die für diese Datenbank registrierte kurzfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="3ac9b-110">Die Richtlinie ist der Aufbewahrungszeitraum in Tagen für Point-in-Time-Wiederherstellungs Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="3ac9b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ac9b-111">EXAMPLES</span></span>

### <span data-ttu-id="3ac9b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ac9b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="3ac9b-113">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für database01 ab.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="3ac9b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3ac9b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="3ac9b-115">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für database01 über die Rohrverlegung in einem Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="3ac9b-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3ac9b-116">Example 3</span></span>
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

<span data-ttu-id="3ac9b-117">Dieser Befehl ruft die kurzfristige Aufbewahrungsrichtlinie für alle gelöschten Datenbanken mit dem Namen database01 über die Rohrverlegung in einem gelöschten Datenbankobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="3ac9b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ac9b-118">PARAMETERS</span></span>

### <span data-ttu-id="3ac9b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ac9b-119">-DatabaseName</span></span>
<span data-ttu-id="3ac9b-120">Der Name der Azure SQL-Instanzen Datenbank, für die Sicherungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="3ac9b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac9b-121">-DefaultProfile</span></span>
<span data-ttu-id="3ac9b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac9b-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="3ac9b-123">-DeletionDate</span></span>
<span data-ttu-id="3ac9b-124">Das Löschdatum der Azure SQL-Instanzen Datenbank zum Abrufen von Sicherungen für, mit Millisekunden-Genauigkeit (z. b. 2016-02-23T00:21:22.847 z)</span><span class="sxs-lookup"><span data-stu-id="3ac9b-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="3ac9b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ac9b-125">-InputObject</span></span>
<span data-ttu-id="3ac9b-126">Das Live-oder gelöschte Datenbankobjekt, für das die Richtlinie abgerufen/gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="3ac9b-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3ac9b-127">-InstanceName</span></span>
<span data-ttu-id="3ac9b-128">Der Name der verwalteten Azure SQL-Instanz, in der sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="3ac9b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac9b-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ac9b-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ac9b-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3ac9b-131">-ResourceId</span></span>
<span data-ttu-id="3ac9b-132">Die Ressourcen-ID für kurzfristige Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="3ac9b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac9b-133">CommonParameters</span></span>
<span data-ttu-id="3ac9b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac9b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac9b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ac9b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac9b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ac9b-136">INPUTS</span></span>

### <span data-ttu-id="3ac9b-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="3ac9b-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="3ac9b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3ac9b-138">System.String</span></span>

## <span data-ttu-id="3ac9b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ac9b-139">OUTPUTS</span></span>

### <span data-ttu-id="3ac9b-140">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3ac9b-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3ac9b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ac9b-141">NOTES</span></span>

## <span data-ttu-id="3ac9b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ac9b-142">RELATED LINKS</span></span>
