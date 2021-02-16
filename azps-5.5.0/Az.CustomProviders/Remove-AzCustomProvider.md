---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148380"
---
# <span data-ttu-id="0dbd7-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="0dbd7-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="0dbd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbd7-103">Löscht den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="0dbd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dbd7-104">SYNTAX</span></span>

### <span data-ttu-id="0dbd7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="0dbd7-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0dbd7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0dbd7-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0dbd7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dbd7-107">DESCRIPTION</span></span>
<span data-ttu-id="0dbd7-108">Löscht den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="0dbd7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dbd7-109">EXAMPLES</span></span>

### <span data-ttu-id="0dbd7-110">Beispiel 1: Entfernen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="0dbd7-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="0dbd7-111">Entfernen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="0dbd7-111">Remove a custom provider</span></span>

### <span data-ttu-id="0dbd7-112">Beispiel 2: Entfernen eines benutzerdefinierten Anbieters mit PassThru</span><span class="sxs-lookup"><span data-stu-id="0dbd7-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="0dbd7-113">Entfernen Sie einen benutzerdefinierten Anbieter, und zeigen Sie mithilfe des Features "PassThru" Erfolg oder Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="0dbd7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-114">PARAMETERS</span></span>

### <span data-ttu-id="0dbd7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dbd7-115">-AsJob</span></span>
<span data-ttu-id="0dbd7-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0dbd7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0dbd7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbd7-117">-DefaultProfile</span></span>
<span data-ttu-id="0dbd7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dbd7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dbd7-119">-InputObject</span></span>
<span data-ttu-id="0dbd7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbd7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0dbd7-121">-Name</span></span>
<span data-ttu-id="0dbd7-122">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbd7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0dbd7-123">-NoWait</span></span>
<span data-ttu-id="0dbd7-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0dbd7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0dbd7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dbd7-125">-PassThru</span></span>
<span data-ttu-id="0dbd7-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0dbd7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbd7-127">-ResourceGroupName</span></span>
<span data-ttu-id="0dbd7-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="0dbd7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0dbd7-129">-SubscriptionId</span></span>
<span data-ttu-id="0dbd7-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-130">The Azure subscription ID.</span></span>
<span data-ttu-id="0dbd7-131">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="0dbd7-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="0dbd7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dbd7-132">-Confirm</span></span>
<span data-ttu-id="0dbd7-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dbd7-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0dbd7-134">-WhatIf</span></span>
<span data-ttu-id="0dbd7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dbd7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dbd7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbd7-137">CommonParameters</span></span>
<span data-ttu-id="0dbd7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbd7-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dbd7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbd7-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dbd7-140">INPUTS</span></span>

### <span data-ttu-id="0dbd7-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="0dbd7-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="0dbd7-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dbd7-142">OUTPUTS</span></span>

### <span data-ttu-id="0dbd7-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0dbd7-143">System.Boolean</span></span>

## <span data-ttu-id="0dbd7-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0dbd7-144">NOTES</span></span>

<span data-ttu-id="0dbd7-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0dbd7-145">ALIASES</span></span>

<span data-ttu-id="0dbd7-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0dbd7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0dbd7-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0dbd7-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0dbd7-149">INPUTOBJECT <ICustomProvidersIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0dbd7-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0dbd7-150">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="0dbd7-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0dbd7-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0dbd7-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0dbd7-153">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="0dbd7-154">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="0dbd7-155">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="0dbd7-156">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="0dbd7-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="0dbd7-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0dbd7-157">RELATED LINKS</span></span>

