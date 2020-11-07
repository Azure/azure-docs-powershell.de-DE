---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846591"
---
# <span data-ttu-id="dc0e7-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc0e7-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="dc0e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0e7-103">Das Cmdlet " **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** " legt die langfristige Aufbewahrungsrichtlinie einer verwalteten Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="dc0e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc0e7-104">SYNTAX</span></span>

### <span data-ttu-id="dc0e7-105">WeeklyRetentionRequired (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc0e7-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0e7-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="dc0e7-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0e7-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="dc0e7-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0e7-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="dc0e7-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc0e7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc0e7-109">DESCRIPTION</span></span>
<span data-ttu-id="dc0e7-110">Das Cmdlet " **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** " legt die langfristige Aufbewahrungsrichtlinie für diese verwaltete Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="dc0e7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc0e7-111">EXAMPLES</span></span>

### <span data-ttu-id="dc0e7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc0e7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="dc0e7-113">Konfiguriert die wöchentliche Richtlinie für die langfristige Aufbewahrung der Datenbank auf eine Woche.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="dc0e7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc0e7-114">Example 2</span></span>
```
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```


<span data-ttu-id="dc0e7-115">Mit diesem Befehl wird die langfristige Aufbewahrungsrichtlinie aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="dc0e7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc0e7-116">PARAMETERS</span></span>

### <span data-ttu-id="dc0e7-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc0e7-117">-DatabaseName</span></span>
<span data-ttu-id="dc0e7-118">Der Name der zu verwendenden Azure-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-118">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0e7-119">-DefaultProfile</span></span>
<span data-ttu-id="dc0e7-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="dc0e7-121">-InstanceName</span></span>
<span data-ttu-id="dc0e7-122">Der Name der Azure-verwalteten Instanz, zu der die Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-122">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="dc0e7-123">-MonthlyRetention</span></span>
<span data-ttu-id="dc0e7-124">Die monatliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-124">The Monthly Retention.</span></span>
<span data-ttu-id="dc0e7-125">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dc0e7-126">Es gibt einen Mindestbetrag von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="dc0e7-127">-RemovePolicy</span></span>
<span data-ttu-id="dc0e7-128">Falls angegeben, wird die Richtlinie für die Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-128">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0e7-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc0e7-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="dc0e7-131">-WeeklyRetention</span></span>
<span data-ttu-id="dc0e7-132">Die wöchentliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-132">The Weekly Retention.</span></span>
<span data-ttu-id="dc0e7-133">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dc0e7-134">Es gibt einen Mindestbetrag von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="dc0e7-135">-WeekOfYear</span></span>
<span data-ttu-id="dc0e7-136">Die Woche des Jahres, 1 bis 52, um die jährliche Aufbewahrung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="dc0e7-137">-YearlyRetention</span></span>
<span data-ttu-id="dc0e7-138">Die jährliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-138">The Yearly Retention.</span></span>
<span data-ttu-id="dc0e7-139">Wenn nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben wird, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dc0e7-140">Es gibt einen Mindestbetrag von 7 Tagen und maximal 10 Jahren.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc0e7-141">-Confirm</span></span>
<span data-ttu-id="dc0e7-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0e7-143">-WhatIf</span></span>
<span data-ttu-id="dc0e7-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0e7-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0e7-146">CommonParameters</span></span>
<span data-ttu-id="dc0e7-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0e7-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc0e7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0e7-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc0e7-149">INPUTS</span></span>

### <span data-ttu-id="dc0e7-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dc0e7-150">System.String</span></span>

### <span data-ttu-id="dc0e7-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dc0e7-151">System.Int32</span></span>

## <span data-ttu-id="dc0e7-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc0e7-152">OUTPUTS</span></span>

### <span data-ttu-id="dc0e7-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="dc0e7-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="dc0e7-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc0e7-154">NOTES</span></span>

## <span data-ttu-id="dc0e7-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc0e7-155">RELATED LINKS</span></span>

[<span data-ttu-id="dc0e7-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc0e7-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="dc0e7-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dc0e7-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dc0e7-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dc0e7-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dc0e7-159">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="dc0e7-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)