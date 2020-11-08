---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006951"
---
# <span data-ttu-id="a8d2e-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="a8d2e-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="a8d2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d2e-103">Fortsetzen einer fehlgeschlagenen Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="a8d2e-103">Resume a failed update.</span></span>

## <span data-ttu-id="a8d2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8d2e-104">SYNTAX</span></span>

### <span data-ttu-id="a8d2e-105">Erneut ausführen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8d2e-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a8d2e-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a8d2e-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8d2e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="a8d2e-108">Fortsetzen einer fehlgeschlagenen Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="a8d2e-108">Resume a failed update.</span></span>

## <span data-ttu-id="a8d2e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8d2e-109">EXAMPLES</span></span>

### <span data-ttu-id="a8d2e-110">Beispiel 1: Resume-AzsUpdateRun nach Name und Updatename</span><span class="sxs-lookup"><span data-stu-id="a8d2e-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="a8d2e-111">Mit Unifiedgroup können Sie eine bestimmte Fehlgeschlagene Aktualisierung erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="a8d2e-112">Beachten Sie, dass die Update Version unbedingt größer als die aktuelle Version ist.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="a8d2e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8d2e-113">PARAMETERS</span></span>

### <span data-ttu-id="a8d2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d2e-114">-DefaultProfile</span></span>
<span data-ttu-id="a8d2e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d2e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a8d2e-116">-InputObject</span></span>
<span data-ttu-id="a8d2e-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a8d2e-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="a8d2e-118">-Location</span></span>
<span data-ttu-id="a8d2e-119">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8d2e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a8d2e-120">-Name</span></span>
<span data-ttu-id="a8d2e-121">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8d2e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8d2e-122">-PassThru</span></span>
<span data-ttu-id="a8d2e-123">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="a8d2e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a8d2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8d2e-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8d2e-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a8d2e-126">-SubscriptionId</span></span>
<span data-ttu-id="a8d2e-127">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a8d2e-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8d2e-129">-Updatename</span><span class="sxs-lookup"><span data-stu-id="a8d2e-129">-UpdateName</span></span>
<span data-ttu-id="a8d2e-130">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8d2e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8d2e-131">-Confirm</span></span>
<span data-ttu-id="a8d2e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8d2e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d2e-133">-WhatIf</span></span>
<span data-ttu-id="a8d2e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8d2e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8d2e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d2e-136">CommonParameters</span></span>
<span data-ttu-id="a8d2e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d2e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8d2e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d2e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8d2e-139">INPUTS</span></span>

### <span data-ttu-id="a8d2e-140">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a8d2e-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="a8d2e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8d2e-141">OUTPUTS</span></span>

### <span data-ttu-id="a8d2e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8d2e-142">System.Boolean</span></span>



## <span data-ttu-id="a8d2e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8d2e-143">NOTES</span></span>

<span data-ttu-id="a8d2e-144">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8d2e-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a8d2e-146">Inputobject <IUpdateAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a8d2e-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8d2e-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a8d2e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8d2e-148">`[ResourceGroupName <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="a8d2e-149">`[RunName <String>]`: Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="a8d2e-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="a8d2e-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a8d2e-152">`[UpdateLocation <String>]`: Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="a8d2e-153">`[UpdateName <String>]`: Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="a8d2e-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="a8d2e-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8d2e-154">RELATED LINKS</span></span>

