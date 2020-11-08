---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005557"
---
# <span data-ttu-id="c835d-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c835d-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="c835d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c835d-102">SYNOPSIS</span></span>
<span data-ttu-id="c835d-103">Aktualisieren eines Sicherungsspeicherorts</span><span class="sxs-lookup"><span data-stu-id="c835d-103">Update a backup location.</span></span>

## <span data-ttu-id="c835d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c835d-104">SYNTAX</span></span>

### <span data-ttu-id="c835d-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c835d-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c835d-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c835d-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c835d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c835d-107">DESCRIPTION</span></span>
<span data-ttu-id="c835d-108">Aktualisieren eines Sicherungsspeicherorts</span><span class="sxs-lookup"><span data-stu-id="c835d-108">Update a backup location.</span></span>

## <span data-ttu-id="c835d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c835d-109">EXAMPLES</span></span>

### <span data-ttu-id="c835d-110">Beispiel 1: Einrichten der Sicherungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="c835d-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="c835d-111">Konfigurieren Sie die Azure Stack-Sicherungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c835d-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="c835d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c835d-112">PARAMETERS</span></span>

### <span data-ttu-id="c835d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c835d-113">-AsJob</span></span>
<span data-ttu-id="c835d-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c835d-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="c835d-115">-Backup</span></span>
<span data-ttu-id="c835d-116">Informationen zum Sicherungsspeicherort.</span><span class="sxs-lookup"><span data-stu-id="c835d-116">Information about the backup location.</span></span>
<span data-ttu-id="c835d-117">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Sicherungseigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c835d-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="c835d-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="c835d-119">Das Intervall in Stunden für die Häufigkeit, mit der der Planer eine Sicherung ausführt.</span><span class="sxs-lookup"><span data-stu-id="c835d-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c835d-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="c835d-121">Der Aufbewahrungszeitraum in Tagen für backs am Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c835d-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c835d-122">-DefaultProfile</span></span>
<span data-ttu-id="c835d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c835d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="c835d-124">-EncryptionCertPath</span></span>
<span data-ttu-id="c835d-125">Pfad zur Verschlüsselungs-CERT-Datei mit öffentlichem Schlüssel (. cer).</span><span class="sxs-lookup"><span data-stu-id="c835d-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="c835d-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="c835d-127">"True", wenn der Sicherungsplaner aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c835d-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="c835d-128">-Location</span></span>
<span data-ttu-id="c835d-129">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="c835d-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c835d-130">-NoWait</span></span>
<span data-ttu-id="c835d-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c835d-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-132">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="c835d-132">-Password</span></span>
<span data-ttu-id="c835d-133">Kennwort für den Zugriff auf den Standort.</span><span class="sxs-lookup"><span data-stu-id="c835d-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-134">-Path</span><span class="sxs-lookup"><span data-stu-id="c835d-134">-Path</span></span>
<span data-ttu-id="c835d-135">Pfad zum Aktualisierungsspeicherort</span><span class="sxs-lookup"><span data-stu-id="c835d-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c835d-136">-ResourceGroupName</span></span>
<span data-ttu-id="c835d-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c835d-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c835d-138">-SubscriptionId</span></span>
<span data-ttu-id="c835d-139">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c835d-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c835d-140">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c835d-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="c835d-141">-Tag</span></span>
<span data-ttu-id="c835d-142">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="c835d-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="c835d-143">-UserName</span></span>
<span data-ttu-id="c835d-144">Benutzername für den Zugriff auf den Standort.</span><span class="sxs-lookup"><span data-stu-id="c835d-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c835d-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c835d-145">-Confirm</span></span>
<span data-ttu-id="c835d-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c835d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c835d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c835d-147">-WhatIf</span></span>
<span data-ttu-id="c835d-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c835d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c835d-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c835d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c835d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c835d-150">CommonParameters</span></span>
<span data-ttu-id="c835d-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c835d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c835d-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c835d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c835d-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c835d-153">INPUTS</span></span>

### <span data-ttu-id="c835d-154">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="c835d-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="c835d-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c835d-155">OUTPUTS</span></span>

### <span data-ttu-id="c835d-156">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="c835d-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="c835d-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="c835d-157">NOTES</span></span>

<span data-ttu-id="c835d-158">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c835d-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c835d-159">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c835d-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c835d-160">Sicherung <IBackupLocation> : Informationen zum Sicherungsspeicherort.</span><span class="sxs-lookup"><span data-stu-id="c835d-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="c835d-161">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c835d-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c835d-162">`[Tag <IResourceTags>]`: Liste von Schlüsselwert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="c835d-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="c835d-163">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c835d-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c835d-164">`[BackupFrequencyInHours <Int32?>]`: Das Intervall in Stunden für die Häufigkeit, mit der der Planer eine Sicherung ausführt.</span><span class="sxs-lookup"><span data-stu-id="c835d-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="c835d-165">`[BackupRetentionPeriodInDays <Int32?>]`: Der Aufbewahrungszeitraum in Tagen für backs am Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c835d-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="c835d-166">`[EncryptionCertBase64 <String>]`: Die Base64-Rohdaten für das Sicherungs Verschlüsselungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="c835d-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="c835d-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True, wenn der Sicherungsplaner aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c835d-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="c835d-168">`[Password <String>]`: Kennwort für den Zugriff auf den Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c835d-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="c835d-169">`[Path <String>]`: Pfad zum Aktualisierungsspeicherort</span><span class="sxs-lookup"><span data-stu-id="c835d-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="c835d-170">`[UserName <String>]`: Username für den Zugriff auf den Standort.</span><span class="sxs-lookup"><span data-stu-id="c835d-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="c835d-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c835d-171">RELATED LINKS</span></span>

