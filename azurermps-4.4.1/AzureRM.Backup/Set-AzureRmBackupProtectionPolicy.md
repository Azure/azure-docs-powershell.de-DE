---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 70e6cf359f81911d8dff2e96944e93c388cfc80e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497909"
---
# <span data-ttu-id="24ae4-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ae4-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="24ae4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="24ae4-103">Ändert eine vorhandene Schutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="24ae4-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ae4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24ae4-104">SYNTAX</span></span>

### <span data-ttu-id="24ae4-105">NoScheduleParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="24ae4-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24ae4-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="24ae4-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24ae4-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="24ae4-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24ae4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24ae4-108">DESCRIPTION</span></span>
<span data-ttu-id="24ae4-109">Mit dem Cmdlet " **festlegen-AzureRmBackupProtectionPolicy** " wird eine vorhandene Schutzrichtlinie in Azure Backup geändert.</span><span class="sxs-lookup"><span data-stu-id="24ae4-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="24ae4-110">Sie können die folgenden Schutzrichtlinien Komponenten ändern:</span><span class="sxs-lookup"><span data-stu-id="24ae4-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="24ae4-111">Namen</span><span class="sxs-lookup"><span data-stu-id="24ae4-111">Name</span></span>
- <span data-ttu-id="24ae4-112">Sicherungszeitplan</span><span class="sxs-lookup"><span data-stu-id="24ae4-112">Backup schedule</span></span>
- <span data-ttu-id="24ae4-113">Aufbewahrungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="24ae4-113">Retention policies</span></span>

<span data-ttu-id="24ae4-114">Jede Änderung kann sich auf die Sicherung und Aufbewahrung der mit der Richtlinie verknüpften Elemente auswirken.</span><span class="sxs-lookup"><span data-stu-id="24ae4-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="24ae4-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24ae4-115">EXAMPLES</span></span>

## <span data-ttu-id="24ae4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="24ae4-116">PARAMETERS</span></span>

### <span data-ttu-id="24ae4-117">-Backup-Daten</span><span class="sxs-lookup"><span data-stu-id="24ae4-117">-BackupTime</span></span>
<span data-ttu-id="24ae4-118">Gibt die neue Sicherungszeit des Tages als **DateTime** -Objekt für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="24ae4-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="24ae4-119">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="24ae4-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="24ae4-120">Für Informationen zu **DateTime** -Objekten geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="24ae4-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-121">-Täglich</span><span class="sxs-lookup"><span data-stu-id="24ae4-121">-Daily</span></span>
<span data-ttu-id="24ae4-122">Gibt an, dass der Sicherungsvorgang nach einem täglichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24ae4-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="24ae4-123">-DaysOfWeek</span></span>
<span data-ttu-id="24ae4-124">Gibt ein Array von Wochentagen an.</span><span class="sxs-lookup"><span data-stu-id="24ae4-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="24ae4-125">Diese Richtlinie führt Sicherungen an den Tagen durch, die durch diesen Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24ae4-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="24ae4-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="24ae4-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24ae4-127">Montag</span><span class="sxs-lookup"><span data-stu-id="24ae4-127">Monday</span></span> 
- <span data-ttu-id="24ae4-128">Dienstag</span><span class="sxs-lookup"><span data-stu-id="24ae4-128">Tuesday</span></span> 
- <span data-ttu-id="24ae4-129">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="24ae4-129">Wednesday</span></span> 
- <span data-ttu-id="24ae4-130">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="24ae4-130">Thursday</span></span> 
- <span data-ttu-id="24ae4-131">Freitag</span><span class="sxs-lookup"><span data-stu-id="24ae4-131">Friday</span></span> 
- <span data-ttu-id="24ae4-132">Samstag</span><span class="sxs-lookup"><span data-stu-id="24ae4-132">Saturday</span></span> 
- <span data-ttu-id="24ae4-133">Sonntag</span><span class="sxs-lookup"><span data-stu-id="24ae4-133">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="24ae4-134">-NewName</span></span>
<span data-ttu-id="24ae4-135">Gibt den neuen Namen für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="24ae4-135">Specifies the new name for the policy.</span></span>
<span data-ttu-id="24ae4-136">Dieser Name muss in einem Tresor eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="24ae4-136">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-137">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ae4-137">-ProtectionPolicy</span></span>
<span data-ttu-id="24ae4-138">Gibt Schutzrichtlinien an, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="24ae4-138">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="24ae4-139">Verwenden Sie das Get-AzureRmBackupProtectionPolicy-Cmdlet, um ein **AzureRmBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="24ae4-139">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-140">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ae4-140">-RetentionPolicy</span></span>
<span data-ttu-id="24ae4-141">Gibt ein Array von Aufbewahrungsrichtlinien für die Sicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="24ae4-141">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="24ae4-142">Verwenden Sie zum Abrufen von **AzureRmBackupRetentionPolicy** -Objekten das New-AzureRmBackupRetentionPolicyObject-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24ae4-142">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-143">– Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="24ae4-143">-Weekly</span></span>
<span data-ttu-id="24ae4-144">Gibt an, dass der Sicherungsvorgang nach einem wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24ae4-144">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ae4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ae4-145">-DefaultProfile</span></span>
<span data-ttu-id="24ae4-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24ae4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24ae4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ae4-147">CommonParameters</span></span>
<span data-ttu-id="24ae4-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ae4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ae4-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ae4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ae4-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24ae4-150">INPUTS</span></span>

### <span data-ttu-id="24ae4-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ae4-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="24ae4-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24ae4-152">OUTPUTS</span></span>

### <span data-ttu-id="24ae4-153">Keine</span><span class="sxs-lookup"><span data-stu-id="24ae4-153">None</span></span>

## <span data-ttu-id="24ae4-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="24ae4-154">NOTES</span></span>

## <span data-ttu-id="24ae4-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24ae4-155">RELATED LINKS</span></span>

[<span data-ttu-id="24ae4-156">Neu – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="24ae4-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


