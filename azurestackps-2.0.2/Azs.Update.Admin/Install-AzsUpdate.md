---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007130"
---
# <span data-ttu-id="fabe4-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="fabe4-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="fabe4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fabe4-102">SYNOPSIS</span></span>
<span data-ttu-id="fabe4-103">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="fabe4-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="fabe4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fabe4-104">SYNTAX</span></span>

### <span data-ttu-id="fabe4-105">Übernehmen (Standard)</span><span class="sxs-lookup"><span data-stu-id="fabe4-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fabe4-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fabe4-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fabe4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fabe4-107">DESCRIPTION</span></span>
<span data-ttu-id="fabe4-108">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="fabe4-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="fabe4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fabe4-109">EXAMPLES</span></span>

### <span data-ttu-id="fabe4-110">Beispiel 1: Install-AzsUpdate nach Name</span><span class="sxs-lookup"><span data-stu-id="fabe4-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="fabe4-111">Unifiedgroup ermöglicht es Ihnen, bestimmte Updates nach Namen zu installieren.</span><span class="sxs-lookup"><span data-stu-id="fabe4-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="fabe4-112">Beachten Sie, dass die Update Version unbedingt größer als die aktuelle Version ist.</span><span class="sxs-lookup"><span data-stu-id="fabe4-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="fabe4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fabe4-113">PARAMETERS</span></span>

### <span data-ttu-id="fabe4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fabe4-114">-AsJob</span></span>
<span data-ttu-id="fabe4-115">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fabe4-115">Run the command as a job</span></span>

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

### <span data-ttu-id="fabe4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabe4-116">-DefaultProfile</span></span>
<span data-ttu-id="fabe4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fabe4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fabe4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fabe4-118">-InputObject</span></span>
<span data-ttu-id="fabe4-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fabe4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fabe4-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="fabe4-120">-Location</span></span>
<span data-ttu-id="fabe4-121">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="fabe4-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fabe4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fabe4-122">-Name</span></span>
<span data-ttu-id="fabe4-123">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="fabe4-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fabe4-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fabe4-124">-NoWait</span></span>
<span data-ttu-id="fabe4-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fabe4-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fabe4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fabe4-126">-ResourceGroupName</span></span>
<span data-ttu-id="fabe4-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fabe4-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fabe4-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fabe4-128">-SubscriptionId</span></span>
<span data-ttu-id="fabe4-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fabe4-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fabe4-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fabe4-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fabe4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fabe4-131">-Confirm</span></span>
<span data-ttu-id="fabe4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fabe4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fabe4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fabe4-133">-WhatIf</span></span>
<span data-ttu-id="fabe4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fabe4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fabe4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fabe4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fabe4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabe4-136">CommonParameters</span></span>
<span data-ttu-id="fabe4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fabe4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabe4-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fabe4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabe4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fabe4-139">INPUTS</span></span>

### <span data-ttu-id="fabe4-140">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fabe4-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="fabe4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fabe4-141">OUTPUTS</span></span>

### <span data-ttu-id="fabe4-142">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="fabe4-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="fabe4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="fabe4-143">NOTES</span></span>

<span data-ttu-id="fabe4-144">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fabe4-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fabe4-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="fabe4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fabe4-146">Inputobject <IUpdateAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="fabe4-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fabe4-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="fabe4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fabe4-148">`[ResourceGroupName <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fabe4-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="fabe4-149">`[RunName <String>]`: Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="fabe4-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="fabe4-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fabe4-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="fabe4-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fabe4-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fabe4-152">`[UpdateLocation <String>]`: Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="fabe4-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="fabe4-153">`[UpdateName <String>]`: Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="fabe4-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="fabe4-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fabe4-154">RELATED LINKS</span></span>

