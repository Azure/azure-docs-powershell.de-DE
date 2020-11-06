---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479934"
---
# <span data-ttu-id="387d7-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="387d7-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="387d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="387d7-102">SYNOPSIS</span></span>
<span data-ttu-id="387d7-103">Erstellt eine Aufbewahrungsrichtlinie für Backups.</span><span class="sxs-lookup"><span data-stu-id="387d7-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="387d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="387d7-104">SYNTAX</span></span>

### <span data-ttu-id="387d7-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="387d7-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="387d7-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="387d7-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="387d7-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="387d7-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="387d7-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="387d7-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="387d7-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="387d7-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="387d7-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="387d7-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="387d7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="387d7-111">DESCRIPTION</span></span>
<span data-ttu-id="387d7-112">Das Cmdlet **New-AzureRmBackupRetentionPolicyObject** erstellt eine Azure Backup-Aufbewahrungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="387d7-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="387d7-113">Eine Aufbewahrungsrichtlinie definiert, wie lange die Sicherung einen Wiederherstellungspunkt aufrecht erhält.</span><span class="sxs-lookup"><span data-stu-id="387d7-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="387d7-114">Die Aufbewahrungsarten sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="387d7-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="387d7-115">Täglich</span><span class="sxs-lookup"><span data-stu-id="387d7-115">Daily</span></span> 
- <span data-ttu-id="387d7-116">Wochen</span><span class="sxs-lookup"><span data-stu-id="387d7-116">Weekly</span></span> 
- <span data-ttu-id="387d7-117">Monatliche</span><span class="sxs-lookup"><span data-stu-id="387d7-117">Monthly</span></span> 
- <span data-ttu-id="387d7-118">Jahres</span><span class="sxs-lookup"><span data-stu-id="387d7-118">Yearly</span></span> 

<span data-ttu-id="387d7-119">Erstellen Sie eine Aufbewahrungsrichtlinie für jede Art von Aufbewahrung, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="387d7-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="387d7-120">Eine Sicherungsrichtlinie ist mit mindestens einer Aufbewahrungsrichtlinie verbunden.</span><span class="sxs-lookup"><span data-stu-id="387d7-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="387d7-121">Verwenden Sie zum Erstellen einer Sicherungsrichtlinie das New-AzureRmBackupProtectionPolicy-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="387d7-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="387d7-122">Sie können stattdessen eine Aufbewahrungsrichtlinie für das Enable-AzureRmBackupProtection-Cmdlet bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="387d7-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="387d7-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="387d7-123">EXAMPLES</span></span>

### <span data-ttu-id="387d7-124">Beispiel 1: Erstellen einer Aufbewahrungsrichtlinie für die tägliche Aufbewahrung</span><span class="sxs-lookup"><span data-stu-id="387d7-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="387d7-125">Der erste Befehl erstellt eine Aufbewahrungsrichtlinie für 30 Tage tägliche Aufbewahrung und speichert Sie dann in der $Daily-Variablen.</span><span class="sxs-lookup"><span data-stu-id="387d7-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="387d7-126">Der zweite Befehl zeigt den Inhalt von $Daily an.</span><span class="sxs-lookup"><span data-stu-id="387d7-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="387d7-127">Beispiel 2: Erstellen einer monatlichen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="387d7-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="387d7-128">Mit dem ersten Befehl wird eine Aufbewahrungsrichtlinie erstellt, die die Sicherung auf dem zehnten und dem zwanzigsten Monat für zwölf Monate aufrecht erhält.</span><span class="sxs-lookup"><span data-stu-id="387d7-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="387d7-129">Der Befehl speichert die Aufbewahrungsrichtlinie in der $Monthly Variablen.</span><span class="sxs-lookup"><span data-stu-id="387d7-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="387d7-130">Der zweite Befehl zeigt den Inhalt von $Monthly an.</span><span class="sxs-lookup"><span data-stu-id="387d7-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="387d7-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="387d7-131">PARAMETERS</span></span>

### <span data-ttu-id="387d7-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="387d7-132">-DailyRetention</span></span>
<span data-ttu-id="387d7-133">Gibt an, dass mit diesem Cmdlet eine tägliche Aufbewahrungsrichtlinie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="387d7-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="387d7-134">-DaysOfMonth</span></span>
<span data-ttu-id="387d7-135">Gibt die Tage des Monats an, die ermitteln, welche Wiederherstellungspunkte gesichert werden und wie lange.</span><span class="sxs-lookup"><span data-stu-id="387d7-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="387d7-136">Die zulässigen Werte für diesen Parameter sind: ganze Zahlen von 1 bis 28 und zuletzt.</span><span class="sxs-lookup"><span data-stu-id="387d7-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="387d7-137">Geben Sie diesen Parameter an, wenn Sie die *DailyRetention* -, *MonthlyRetentionInDailyFormat* -und *YearlyRetentionInDailyFormat* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="387d7-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="387d7-138">-DaysOfWeek</span></span>
<span data-ttu-id="387d7-139">Gibt ein Array von Wochentagen an.</span><span class="sxs-lookup"><span data-stu-id="387d7-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="387d7-140">Die Tage, die dieses Cmdlet angibt, geben an, welche Wiederherstellungspunkte von der Sicherung beibehalten werden und wie lange.</span><span class="sxs-lookup"><span data-stu-id="387d7-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="387d7-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="387d7-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="387d7-142">Montag</span><span class="sxs-lookup"><span data-stu-id="387d7-142">Monday</span></span> 
- <span data-ttu-id="387d7-143">Dienstag</span><span class="sxs-lookup"><span data-stu-id="387d7-143">Tuesday</span></span> 
- <span data-ttu-id="387d7-144">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="387d7-144">Wednesday</span></span> 
- <span data-ttu-id="387d7-145">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="387d7-145">Thursday</span></span> 
- <span data-ttu-id="387d7-146">Freitag</span><span class="sxs-lookup"><span data-stu-id="387d7-146">Friday</span></span> 
- <span data-ttu-id="387d7-147">Samstag</span><span class="sxs-lookup"><span data-stu-id="387d7-147">Saturday</span></span> 
- <span data-ttu-id="387d7-148">Sonntag</span><span class="sxs-lookup"><span data-stu-id="387d7-148">Sunday</span></span>

<span data-ttu-id="387d7-149">Geben Sie diesen Parameter an, wenn Sie die *WeeklyRetention* -, *MonthlyRetentionInWeeklyFormat* -und *YearlyRetentionInWeeklyFormat* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="387d7-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="387d7-150">Achten Sie darauf, dass die Wochentage, die Sie für die Sicherung und für die Aufbewahrung auswählen, ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="387d7-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="387d7-151">Wenn Ihre Sicherung beispielsweise für samstags eingestellt ist, müssen die Aufbewahrungsrichtlinien auch Saturday verwenden.</span><span class="sxs-lookup"><span data-stu-id="387d7-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="387d7-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="387d7-153">Gibt an, dass dieses Cmdlet eine monatliche Richtlinie im Tagesformat erstellt.</span><span class="sxs-lookup"><span data-stu-id="387d7-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="387d7-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="387d7-155">Gibt an, dass dieses Cmdlet eine monatliche Richtlinie im Wochenformat erstellt.</span><span class="sxs-lookup"><span data-stu-id="387d7-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="387d7-156">-MonthsOfYear</span></span>
<span data-ttu-id="387d7-157">Gibt an, welche Monate des Jahres die Wiederherstellungspunkte aufweisen, die von der Sicherung jährlich aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="387d7-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="387d7-158">Die zulässigen Werte für diesen Parameter sind: Namen von Monaten wie Januar oder Februar.</span><span class="sxs-lookup"><span data-stu-id="387d7-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-159">-Aufbewahrung</span><span class="sxs-lookup"><span data-stu-id="387d7-159">-Retention</span></span>
<span data-ttu-id="387d7-160">Gibt den Aufbewahrungszeitraum in Tagen, Monaten oder Jahren an, für den Backup einen Sicherungspunkt speichert.</span><span class="sxs-lookup"><span data-stu-id="387d7-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="387d7-161">Die Einheit hängt davon ab, ob dieses Cmdlet eine Tages-, Monats-oder Jahres Aufbewahrungs Option auswählt.</span><span class="sxs-lookup"><span data-stu-id="387d7-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="387d7-162">Wenn Sie beispielsweise den *DailyRetention* -Parameter angeben, interpretiert das Cmdlet den aktuellen Parameter als Anzahl von Tagen.</span><span class="sxs-lookup"><span data-stu-id="387d7-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="387d7-163">-WeeklyRetention</span></span>
<span data-ttu-id="387d7-164">Gibt an, dass mit diesem Cmdlet eine wöchentliche Aufbewahrungsrichtlinie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="387d7-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="387d7-165">-WeekNumber</span></span>
<span data-ttu-id="387d7-166">Gibt die Wochen des Monats an, die ermitteln, welche Wiederherstellungspunkte gesichert werden und wie lange.</span><span class="sxs-lookup"><span data-stu-id="387d7-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="387d7-167">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="387d7-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="387d7-168">Ersten</span><span class="sxs-lookup"><span data-stu-id="387d7-168">First</span></span> 
- <span data-ttu-id="387d7-169">Zweiten</span><span class="sxs-lookup"><span data-stu-id="387d7-169">Second</span></span> 
- <span data-ttu-id="387d7-170">Dritt</span><span class="sxs-lookup"><span data-stu-id="387d7-170">Third</span></span> 
- <span data-ttu-id="387d7-171">Vierten</span><span class="sxs-lookup"><span data-stu-id="387d7-171">Fourth</span></span> 
- <span data-ttu-id="387d7-172">Letzten</span><span class="sxs-lookup"><span data-stu-id="387d7-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="387d7-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="387d7-174">Gibt an, dass dieses Cmdlet eine jährliche Aufbewahrungsrichtlinie im Tagesformat erstellt.</span><span class="sxs-lookup"><span data-stu-id="387d7-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="387d7-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="387d7-176">Gibt an, dass dieses Cmdlet eine jährliche Aufbewahrungsrichtlinie im wöchentlichen Format erstellt.</span><span class="sxs-lookup"><span data-stu-id="387d7-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387d7-177">-DefaultProfile</span></span>
<span data-ttu-id="387d7-178">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="387d7-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="387d7-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387d7-179">CommonParameters</span></span>
<span data-ttu-id="387d7-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387d7-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387d7-181">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387d7-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387d7-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="387d7-182">INPUTS</span></span>

### <span data-ttu-id="387d7-183">Keine</span><span class="sxs-lookup"><span data-stu-id="387d7-183">None</span></span>

## <span data-ttu-id="387d7-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="387d7-184">OUTPUTS</span></span>

### <span data-ttu-id="387d7-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="387d7-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="387d7-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="387d7-186">NOTES</span></span>
* <span data-ttu-id="387d7-187">Keine</span><span class="sxs-lookup"><span data-stu-id="387d7-187">None</span></span>

## <span data-ttu-id="387d7-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="387d7-188">RELATED LINKS</span></span>

[<span data-ttu-id="387d7-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="387d7-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="387d7-190">Neu – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="387d7-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


