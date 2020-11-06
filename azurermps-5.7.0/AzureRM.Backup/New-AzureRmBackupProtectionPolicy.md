---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501514"
---
# <span data-ttu-id="8b82c-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b82c-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="8b82c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b82c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b82c-103">Erstellt eine Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8b82c-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b82c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b82c-104">SYNTAX</span></span>

### <span data-ttu-id="8b82c-105">NoScheduleParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b82c-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b82c-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="8b82c-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b82c-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="8b82c-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b82c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b82c-108">DESCRIPTION</span></span>
<span data-ttu-id="8b82c-109">Das Cmdlet **New-AzureRmBackupProtectionPolicy** erstellt eine Azure-Sicherungsrichtlinie als Azure PowerShell-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b82c-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="8b82c-110">Eine Sicherungsrichtlinie definiert, wann und wie oft Backups ein Element sichern.</span><span class="sxs-lookup"><span data-stu-id="8b82c-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="8b82c-111">Das Enable-AzureRmBackupProtection-Cmdlet verwendet eine Sicherungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8b82c-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="8b82c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b82c-112">EXAMPLES</span></span>

### <span data-ttu-id="8b82c-113">Beispiel 1: Erstellen einer täglichen Backup-Richtlinie mit täglicher und monatlicher Aufbewahrung</span><span class="sxs-lookup"><span data-stu-id="8b82c-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="8b82c-114">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="8b82c-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="8b82c-115">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="8b82c-116">Der zweite Befehl erstellt eine Aufbewahrungsrichtlinie für 30 Tage tägliche Aufbewahrung und speichert Sie dann in der $Daily-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="8b82c-117">Der dritte Befehl erstellt eine Aufbewahrungsrichtlinie, die die Sicherung auf dem zehnten und dem zwanzigsten Monat für zwölf Monate aufrecht erhält.</span><span class="sxs-lookup"><span data-stu-id="8b82c-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="8b82c-118">Der Befehl speichert die Aufbewahrungsrichtlinie in der $Monthly Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="8b82c-119">Der endgültige Befehl erstellt eine Sicherungsrichtlinie für den Tresor in $Vault, die eine tägliche Sicherungszeit von 3:00 Uhr aufweist.</span><span class="sxs-lookup"><span data-stu-id="8b82c-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="8b82c-120">Der Befehl weist die Aufbewahrungsrichtlinien zu, die in $Daily und $Monthly gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8b82c-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="8b82c-121">Der Befehl speichert das Ergebnis in der $ProtectionPolicy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8b82c-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="8b82c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b82c-122">PARAMETERS</span></span>

### <span data-ttu-id="8b82c-123">-Backup-Daten</span><span class="sxs-lookup"><span data-stu-id="8b82c-123">-BackupTime</span></span>
<span data-ttu-id="8b82c-124">Gibt die Tageszeit als **DateTime** -Objekt für den Sicherungsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="8b82c-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="8b82c-125">Verwenden Sie zum Abrufen eines **DateTime** -Cmdlets das Get-Date-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b82c-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8b82c-126">Für Informationen zu **DateTime** -Objekten geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8b82c-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-127">-Täglich</span><span class="sxs-lookup"><span data-stu-id="8b82c-127">-Daily</span></span>
<span data-ttu-id="8b82c-128">Gibt an, dass der Sicherungsvorgang nach einem täglichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b82c-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="8b82c-129">-DaysOfWeek</span></span>
<span data-ttu-id="8b82c-130">Gibt ein Array von Wochentagen an.</span><span class="sxs-lookup"><span data-stu-id="8b82c-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="8b82c-131">Diese Richtlinie führt Sicherungen an den Tagen durch, die durch diesen Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b82c-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="8b82c-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8b82c-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b82c-133">Montag</span><span class="sxs-lookup"><span data-stu-id="8b82c-133">Monday</span></span> 
- <span data-ttu-id="8b82c-134">Dienstag</span><span class="sxs-lookup"><span data-stu-id="8b82c-134">Tuesday</span></span> 
- <span data-ttu-id="8b82c-135">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="8b82c-135">Wednesday</span></span> 
- <span data-ttu-id="8b82c-136">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="8b82c-136">Thursday</span></span> 
- <span data-ttu-id="8b82c-137">Freitag</span><span class="sxs-lookup"><span data-stu-id="8b82c-137">Friday</span></span> 
- <span data-ttu-id="8b82c-138">Samstag</span><span class="sxs-lookup"><span data-stu-id="8b82c-138">Saturday</span></span> 
- <span data-ttu-id="8b82c-139">Sonntag</span><span class="sxs-lookup"><span data-stu-id="8b82c-139">Sunday</span></span>

<span data-ttu-id="8b82c-140">Wenn Sie den Parameter *Weekly* angeben, geben Sie diesen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="8b82c-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b82c-141">-DefaultProfile</span></span>
<span data-ttu-id="8b82c-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b82c-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-143">-Name</span><span class="sxs-lookup"><span data-stu-id="8b82c-143">-Name</span></span>
<span data-ttu-id="8b82c-144">Gibt einen Namen für die Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="8b82c-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="8b82c-145">Wählen Sie einen Namen aus, der im Tresor eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="8b82c-145">Select a name that is unique in the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b82c-146">-RetentionPolicy</span></span>
<span data-ttu-id="8b82c-147">Gibt ein Array von Aufbewahrungsrichtlinien für die Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="8b82c-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="8b82c-148">Verwenden Sie zum Abrufen eines **AzureRmBackupRetentionPolicy** das New-AzureRmBackupRetentionPolicyObject-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b82c-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-149">-Typ</span><span class="sxs-lookup"><span data-stu-id="8b82c-149">-Type</span></span>
<span data-ttu-id="8b82c-150">Gibt den Typ des sicherungselements an, auf das die Richtlinie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b82c-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="8b82c-151">Derzeit ist der einzige unterstützte Wert AzureVM.</span><span class="sxs-lookup"><span data-stu-id="8b82c-151">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-152">-Vault</span><span class="sxs-lookup"><span data-stu-id="8b82c-152">-Vault</span></span>
<span data-ttu-id="8b82c-153">Gibt den Azure-sicherungstresor an, zu dem die Sicherungsrichtlinie gehört.</span><span class="sxs-lookup"><span data-stu-id="8b82c-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="8b82c-154">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8b82c-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-155">– Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="8b82c-155">-Weekly</span></span>
<span data-ttu-id="8b82c-156">Gibt an, dass die Sicherungsrichtlinie wöchentlich an einem oder mehreren Wochentagen ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8b82c-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b82c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b82c-157">CommonParameters</span></span>
<span data-ttu-id="8b82c-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b82c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b82c-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b82c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b82c-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b82c-160">INPUTS</span></span>

### <span data-ttu-id="8b82c-161">Keine</span><span class="sxs-lookup"><span data-stu-id="8b82c-161">None</span></span>

## <span data-ttu-id="8b82c-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b82c-162">OUTPUTS</span></span>

### <span data-ttu-id="8b82c-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b82c-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="8b82c-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b82c-164">NOTES</span></span>
* <span data-ttu-id="8b82c-165">Keine</span><span class="sxs-lookup"><span data-stu-id="8b82c-165">None</span></span>

## <span data-ttu-id="8b82c-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b82c-166">RELATED LINKS</span></span>

[<span data-ttu-id="8b82c-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8b82c-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="8b82c-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b82c-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="8b82c-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8b82c-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="8b82c-170">Neu – AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8b82c-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="8b82c-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b82c-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="8b82c-172">Satz-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b82c-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


