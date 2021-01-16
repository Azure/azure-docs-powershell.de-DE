---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302112"
---
# <span data-ttu-id="e1d30-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d30-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="e1d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d30-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d30-103">Das **Cmdlet "Set-AzSqlInstanceDatabaseLongTermRetentionBackup"** legt die langfristige Aufbewahrungsrichtlinie für eine verwaltete Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="e1d30-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="e1d30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1d30-104">SYNTAX</span></span>

### <span data-ttu-id="e1d30-105">WeeklyRetentionRequired (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1d30-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d30-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="e1d30-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d30-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="e1d30-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d30-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="e1d30-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d30-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1d30-109">DESCRIPTION</span></span>
<span data-ttu-id="e1d30-110">Das **Cmdlet "Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy"** legt die langfristige Aufbewahrungsrichtlinie für diese verwaltete Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="e1d30-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="e1d30-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1d30-111">EXAMPLES</span></span>

### <span data-ttu-id="e1d30-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1d30-112">Example 1</span></span>
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

<span data-ttu-id="e1d30-113">Konfiguriert die wöchentliche Richtlinie für die langfristige Aufbewahrung der Datenbank auf eine Woche.</span><span class="sxs-lookup"><span data-stu-id="e1d30-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="e1d30-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e1d30-114">Example 2</span></span>
```powershell
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

<span data-ttu-id="e1d30-115">Mit diesem Befehl wird die langfristige Aufbewahrungsrichtlinie aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="e1d30-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="e1d30-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e1d30-116">Example 3</span></span>

<span data-ttu-id="e1d30-117">Das Set-AzSqlInstanceDatabaseLongTermRetentionBackup-Cmdlet legt die langfristige Aufbewahrungsrichtlinie einer verwalteten Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="e1d30-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="e1d30-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="e1d30-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="e1d30-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d30-119">PARAMETERS</span></span>

### <span data-ttu-id="e1d30-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1d30-120">-DatabaseName</span></span>
<span data-ttu-id="e1d30-121">Der Name der in Azure verwalteten Datenbank, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1d30-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="e1d30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d30-122">-DefaultProfile</span></span>
<span data-ttu-id="e1d30-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1d30-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1d30-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e1d30-124">-InstanceName</span></span>
<span data-ttu-id="e1d30-125">Der Name der azure verwalteten Instanz, zu der die Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="e1d30-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="e1d30-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="e1d30-126">-MonthlyRetention</span></span>
<span data-ttu-id="e1d30-127">Die monatliche Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="e1d30-127">The Monthly Retention.</span></span>
<span data-ttu-id="e1d30-128">Wird nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="e1d30-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e1d30-129">Es sind mindestens 7 Tage und maximal 10 Jahre zulässig.</span><span class="sxs-lookup"><span data-stu-id="e1d30-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="e1d30-130">-RemovePolicy</span></span>
<span data-ttu-id="e1d30-131">Sofern angegeben, wird die Richtlinie für die Datenbank gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e1d30-131">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d30-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1d30-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1d30-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="e1d30-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="e1d30-134">-WeeklyRetention</span></span>
<span data-ttu-id="e1d30-135">Die wöchentliche Aufbewahrungszeit.</span><span class="sxs-lookup"><span data-stu-id="e1d30-135">The Weekly Retention.</span></span>
<span data-ttu-id="e1d30-136">Wird nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="e1d30-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e1d30-137">Es sind mindestens 7 Tage und maximal 10 Jahre zulässig.</span><span class="sxs-lookup"><span data-stu-id="e1d30-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="e1d30-138">-WeekOfYear</span></span>
<span data-ttu-id="e1d30-139">Die Jahreswoche, 1 bis 52, zum Speichern der jährlichen Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="e1d30-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="e1d30-140">-YearlyRetention</span></span>
<span data-ttu-id="e1d30-141">Die Jahresaufbewahrungsdauer.</span><span class="sxs-lookup"><span data-stu-id="e1d30-141">The Yearly Retention.</span></span>
<span data-ttu-id="e1d30-142">Wird nur eine Zahl anstelle einer ISO 8601-Zeichenfolge übergeben, werden Tage als Einheiten angenommen.</span><span class="sxs-lookup"><span data-stu-id="e1d30-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="e1d30-143">Es sind mindestens 7 Tage und maximal 10 Jahre zulässig.</span><span class="sxs-lookup"><span data-stu-id="e1d30-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1d30-144">-Confirm</span></span>
<span data-ttu-id="e1d30-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1d30-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1d30-146">-WhatIf</span></span>
<span data-ttu-id="e1d30-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1d30-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d30-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1d30-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d30-149">CommonParameters</span></span>
<span data-ttu-id="e1d30-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d30-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d30-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1d30-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d30-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1d30-152">INPUTS</span></span>

### <span data-ttu-id="e1d30-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d30-153">System.String</span></span>

### <span data-ttu-id="e1d30-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e1d30-154">System.Int32</span></span>

## <span data-ttu-id="e1d30-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1d30-155">OUTPUTS</span></span>

### <span data-ttu-id="e1d30-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e1d30-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="e1d30-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1d30-157">NOTES</span></span>

## <span data-ttu-id="e1d30-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1d30-158">RELATED LINKS</span></span>

[<span data-ttu-id="e1d30-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d30-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e1d30-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e1d30-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e1d30-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e1d30-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e1d30-162">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="e1d30-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)