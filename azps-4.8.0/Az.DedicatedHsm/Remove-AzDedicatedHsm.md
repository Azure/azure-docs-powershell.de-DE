---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174759"
---
# <span data-ttu-id="a9465-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a9465-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="a9465-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9465-102">SYNOPSIS</span></span>
<span data-ttu-id="a9465-103">Löscht das angegebene Azure dedizierte HSM.</span><span class="sxs-lookup"><span data-stu-id="a9465-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="a9465-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9465-104">SYNTAX</span></span>

### <span data-ttu-id="a9465-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9465-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9465-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9465-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9465-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9465-107">DESCRIPTION</span></span>
<span data-ttu-id="a9465-108">Löscht das angegebene Azure dedizierte HSM.</span><span class="sxs-lookup"><span data-stu-id="a9465-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="a9465-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9465-109">EXAMPLES</span></span>

### <span data-ttu-id="a9465-110">Beispiel 1: Entfernen eines dedizierten HSM nach Namen</span><span class="sxs-lookup"><span data-stu-id="a9465-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="a9465-111">Dieser commnad entfernt ein Hardwaresicherheitsmodul (HSM) nach Namen.</span><span class="sxs-lookup"><span data-stu-id="a9465-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="a9465-112">Beispiel 2: Entfernen eines dedizierten HSM nach Objekt</span><span class="sxs-lookup"><span data-stu-id="a9465-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="a9465-113">Diese commnad entfernt ein dediziertes HSM nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="a9465-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="a9465-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9465-114">PARAMETERS</span></span>

### <span data-ttu-id="a9465-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9465-115">-AsJob</span></span>
<span data-ttu-id="a9465-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a9465-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a9465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9465-117">-DefaultProfile</span></span>
<span data-ttu-id="a9465-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9465-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9465-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9465-119">-InputObject</span></span>
<span data-ttu-id="a9465-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a9465-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9465-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a9465-121">-Name</span></span>
<span data-ttu-id="a9465-122">Der Name des zu löschenden dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="a9465-122">The name of the dedicated HSM to delete</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9465-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a9465-123">-NoWait</span></span>
<span data-ttu-id="a9465-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a9465-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a9465-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9465-125">-PassThru</span></span>
<span data-ttu-id="a9465-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="a9465-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a9465-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9465-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9465-128">Der Name der Ressourcengruppe, zu der das dedizierte HSM gehört.</span><span class="sxs-lookup"><span data-stu-id="a9465-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9465-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a9465-129">-SubscriptionId</span></span>
<span data-ttu-id="a9465-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a9465-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a9465-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a9465-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9465-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9465-132">-Confirm</span></span>
<span data-ttu-id="a9465-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9465-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9465-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9465-134">-WhatIf</span></span>
<span data-ttu-id="a9465-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9465-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9465-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9465-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9465-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9465-137">CommonParameters</span></span>
<span data-ttu-id="a9465-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9465-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9465-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9465-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9465-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9465-140">INPUTS</span></span>

### <span data-ttu-id="a9465-141">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="a9465-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="a9465-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9465-142">OUTPUTS</span></span>

### <span data-ttu-id="a9465-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9465-143">System.Boolean</span></span>

## <span data-ttu-id="a9465-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9465-144">NOTES</span></span>

<span data-ttu-id="a9465-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="a9465-145">ALIASES</span></span>

<span data-ttu-id="a9465-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9465-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9465-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9465-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9465-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a9465-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9465-149">Inputobject <IDedicatedHsmIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9465-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9465-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a9465-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9465-151">`[Name <String>]`: Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="a9465-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="a9465-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="a9465-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="a9465-153">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a9465-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a9465-154">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a9465-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a9465-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9465-155">RELATED LINKS</span></span>

