---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844904"
---
# <span data-ttu-id="fd26f-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="fd26f-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="fd26f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd26f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd26f-103">Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd26f-103">Restore a backup.</span></span>

## <span data-ttu-id="fd26f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd26f-104">SYNTAX</span></span>

### <span data-ttu-id="fd26f-105">RestoreExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd26f-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fd26f-106">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="fd26f-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fd26f-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fd26f-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fd26f-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fd26f-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd26f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd26f-109">DESCRIPTION</span></span>
<span data-ttu-id="fd26f-110">Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd26f-110">Restore a backup.</span></span>

## <span data-ttu-id="fd26f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd26f-111">EXAMPLES</span></span>

### <span data-ttu-id="fd26f-112">Beispiel 1: Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd26f-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="fd26f-113">Wiederherstellen aus einer Azure Stack-Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd26f-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="fd26f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd26f-114">PARAMETERS</span></span>

### <span data-ttu-id="fd26f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd26f-115">-AsJob</span></span>
<span data-ttu-id="fd26f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fd26f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fd26f-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="fd26f-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="fd26f-118">Das Kennwort für das Entschlüsselungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="fd26f-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="fd26f-119">-DecryptionCertPath</span></span>
<span data-ttu-id="fd26f-120">Pfad zur Entschlüsselungs-CERT-Datei mit privatem Schlüssel (PFX).</span><span class="sxs-lookup"><span data-stu-id="fd26f-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd26f-121">-DefaultProfile</span></span>
<span data-ttu-id="fd26f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd26f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd26f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fd26f-123">-Force</span></span>
<span data-ttu-id="fd26f-124">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="fd26f-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="fd26f-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fd26f-125">-InputObject</span></span>
<span data-ttu-id="fd26f-126">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fd26f-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="fd26f-127">-Location</span></span>
<span data-ttu-id="fd26f-128">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="fd26f-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="fd26f-129">-Name</span></span>
<span data-ttu-id="fd26f-130">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="fd26f-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fd26f-131">-NoWait</span></span>
<span data-ttu-id="fd26f-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fd26f-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd26f-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd26f-133">-PassThru</span></span>
<span data-ttu-id="fd26f-134">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="fd26f-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fd26f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd26f-135">-ResourceGroupName</span></span>
<span data-ttu-id="fd26f-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd26f-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="fd26f-137">-RestoreOption</span></span>
<span data-ttu-id="fd26f-138">Eigenschaften für Wiederherstellungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="fd26f-138">Properties for restore options.</span></span>
<span data-ttu-id="fd26f-139">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für RESTOREOPTION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fd26f-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="fd26f-140">-RoleName</span></span>
<span data-ttu-id="fd26f-141">Der Azure Stack-Rollenname für die Wiederherstellung, legen Sie ihn für die gesamte Infrastruktur Rolle auf "leer".</span><span class="sxs-lookup"><span data-stu-id="fd26f-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fd26f-142">-SubscriptionId</span></span>
<span data-ttu-id="fd26f-143">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd26f-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd26f-144">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fd26f-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fd26f-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd26f-145">-Confirm</span></span>
<span data-ttu-id="fd26f-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd26f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd26f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd26f-147">-WhatIf</span></span>
<span data-ttu-id="fd26f-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd26f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd26f-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd26f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd26f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd26f-150">CommonParameters</span></span>
<span data-ttu-id="fd26f-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd26f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd26f-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd26f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd26f-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd26f-153">INPUTS</span></span>

### <span data-ttu-id="fd26f-154">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fd26f-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="fd26f-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd26f-155">OUTPUTS</span></span>

### <span data-ttu-id="fd26f-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd26f-156">System.Boolean</span></span>



## <span data-ttu-id="fd26f-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd26f-157">NOTES</span></span>

<span data-ttu-id="fd26f-158">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd26f-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd26f-159">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="fd26f-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fd26f-160">Inputobject <IBackupAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="fd26f-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fd26f-161">`[Backup <String>]`: Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="fd26f-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="fd26f-162">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="fd26f-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fd26f-163">`[Location <String>]`: Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="fd26f-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="fd26f-164">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd26f-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="fd26f-165">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd26f-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fd26f-166">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fd26f-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="fd26f-167">RESTOREOPTION <IRestoreOptions> : Eigenschaften für Wiederherstellungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="fd26f-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="fd26f-168">`[DecryptionCertBase64 <String>]`: Die Zertifikatsdatei enthält unformatierte Daten in base64-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fd26f-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="fd26f-169">Dies sollte die PFX-Datei mit dem privaten Schlüssel sein.</span><span class="sxs-lookup"><span data-stu-id="fd26f-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="fd26f-170">`[DecryptionCertPassword <String>]`: Das Kennwort für das Entschlüsselungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="fd26f-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="fd26f-171">`[RoleName <String>]`: Der Azure Stack-Rollenname für die Wiederherstellung, für die gesamte Infrastruktur Rolle auf "leer" setzen</span><span class="sxs-lookup"><span data-stu-id="fd26f-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="fd26f-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd26f-172">RELATED LINKS</span></span>

