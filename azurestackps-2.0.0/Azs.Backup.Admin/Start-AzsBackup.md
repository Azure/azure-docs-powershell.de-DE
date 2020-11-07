---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844892"
---
# <span data-ttu-id="26303-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="26303-101">Start-AzsBackup</span></span>

## <span data-ttu-id="26303-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26303-102">SYNOPSIS</span></span>
<span data-ttu-id="26303-103">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="26303-103">Back up a specific location.</span></span>

## <span data-ttu-id="26303-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26303-104">SYNTAX</span></span>

### <span data-ttu-id="26303-105">Erstellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="26303-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26303-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26303-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26303-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26303-107">DESCRIPTION</span></span>
<span data-ttu-id="26303-108">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="26303-108">Back up a specific location.</span></span>

## <span data-ttu-id="26303-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26303-109">EXAMPLES</span></span>

### <span data-ttu-id="26303-110">Beispiel 1: Starten der azurestack-Sicherung</span><span class="sxs-lookup"><span data-stu-id="26303-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="26303-111">Starten Sie eine Azure Stack-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="26303-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="26303-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="26303-112">PARAMETERS</span></span>

### <span data-ttu-id="26303-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26303-113">-AsJob</span></span>
<span data-ttu-id="26303-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="26303-114">Run the command as a job</span></span>

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

### <span data-ttu-id="26303-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26303-115">-DefaultProfile</span></span>
<span data-ttu-id="26303-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26303-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26303-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26303-117">-InputObject</span></span>
<span data-ttu-id="26303-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="26303-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="26303-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="26303-119">-Location</span></span>
<span data-ttu-id="26303-120">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="26303-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26303-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="26303-121">-NoWait</span></span>
<span data-ttu-id="26303-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="26303-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="26303-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26303-123">-ResourceGroupName</span></span>
<span data-ttu-id="26303-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26303-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26303-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="26303-125">-SubscriptionId</span></span>
<span data-ttu-id="26303-126">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="26303-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="26303-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="26303-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26303-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26303-128">-Confirm</span></span>
<span data-ttu-id="26303-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26303-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26303-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26303-130">-WhatIf</span></span>
<span data-ttu-id="26303-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26303-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26303-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26303-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26303-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26303-133">CommonParameters</span></span>
<span data-ttu-id="26303-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26303-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26303-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26303-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26303-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26303-136">INPUTS</span></span>

### <span data-ttu-id="26303-137">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="26303-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="26303-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26303-138">OUTPUTS</span></span>

### <span data-ttu-id="26303-139">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. ibackup</span><span class="sxs-lookup"><span data-stu-id="26303-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="26303-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="26303-140">NOTES</span></span>

<span data-ttu-id="26303-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26303-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26303-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="26303-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="26303-143">Inputobject <IBackupAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="26303-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26303-144">`[Backup <String>]`: Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="26303-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="26303-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="26303-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26303-146">`[Location <String>]`: Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="26303-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="26303-147">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26303-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="26303-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="26303-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="26303-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="26303-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="26303-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26303-150">RELATED LINKS</span></span>

