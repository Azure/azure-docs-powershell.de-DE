---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290284"
---
# <span data-ttu-id="a885f-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a885f-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="a885f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a885f-102">SYNOPSIS</span></span>
<span data-ttu-id="a885f-103">Löscht den angegebenen Azure Dedicated HSM.</span><span class="sxs-lookup"><span data-stu-id="a885f-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="a885f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a885f-104">SYNTAX</span></span>

### <span data-ttu-id="a885f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a885f-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a885f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a885f-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a885f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a885f-107">DESCRIPTION</span></span>
<span data-ttu-id="a885f-108">Löscht den angegebenen Azure Dedicated HSM.</span><span class="sxs-lookup"><span data-stu-id="a885f-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="a885f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a885f-109">EXAMPLES</span></span>

### <span data-ttu-id="a885f-110">Beispiel 1: Entfernen eines dedizierten HSM nach Name</span><span class="sxs-lookup"><span data-stu-id="a885f-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="a885f-111">Mit diesem Komma wird ein Hardwaresicherheitsmodul (Hardware Security Module, HSM) nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="a885f-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="a885f-112">Beispiel 2: Entfernen eines dedizierten HSM nach Objekt</span><span class="sxs-lookup"><span data-stu-id="a885f-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="a885f-113">Mit diesem Komma wird ein dediziertes HSM nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a885f-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="a885f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a885f-114">PARAMETERS</span></span>

### <span data-ttu-id="a885f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a885f-115">-AsJob</span></span>
<span data-ttu-id="a885f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a885f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a885f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a885f-117">-DefaultProfile</span></span>
<span data-ttu-id="a885f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a885f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a885f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a885f-119">-InputObject</span></span>
<span data-ttu-id="a885f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a885f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a885f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a885f-121">-Name</span></span>
<span data-ttu-id="a885f-122">Der Name des dedizierten HSM, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="a885f-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="a885f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a885f-123">-NoWait</span></span>
<span data-ttu-id="a885f-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a885f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a885f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a885f-125">-PassThru</span></span>
<span data-ttu-id="a885f-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a885f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a885f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a885f-127">-ResourceGroupName</span></span>
<span data-ttu-id="a885f-128">Der Name der Ressourcengruppe, zu der der dedizierte HSM gehört.</span><span class="sxs-lookup"><span data-stu-id="a885f-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="a885f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a885f-129">-SubscriptionId</span></span>
<span data-ttu-id="a885f-130">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a885f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a885f-131">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a885f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a885f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a885f-132">-Confirm</span></span>
<span data-ttu-id="a885f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a885f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a885f-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a885f-134">-WhatIf</span></span>
<span data-ttu-id="a885f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a885f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a885f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a885f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a885f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a885f-137">CommonParameters</span></span>
<span data-ttu-id="a885f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a885f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a885f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a885f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a885f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a885f-140">INPUTS</span></span>

### <span data-ttu-id="a885f-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="a885f-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="a885f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a885f-142">OUTPUTS</span></span>

### <span data-ttu-id="a885f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a885f-143">System.Boolean</span></span>

## <span data-ttu-id="a885f-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a885f-144">NOTES</span></span>

<span data-ttu-id="a885f-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a885f-145">ALIASES</span></span>

<span data-ttu-id="a885f-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a885f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a885f-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a885f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a885f-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a885f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a885f-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a885f-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a885f-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a885f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a885f-151">`[Name <String>]`: Name des dedizierten Hsm</span><span class="sxs-lookup"><span data-stu-id="a885f-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="a885f-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="a885f-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="a885f-153">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a885f-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a885f-154">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a885f-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a885f-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a885f-155">RELATED LINKS</span></span>

