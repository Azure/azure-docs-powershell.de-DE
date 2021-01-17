---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470651"
---
# <span data-ttu-id="69324-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="69324-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="69324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69324-102">SYNOPSIS</span></span>
<span data-ttu-id="69324-103">Löschen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="69324-103">Delete an association.</span></span>

## <span data-ttu-id="69324-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69324-104">SYNTAX</span></span>

### <span data-ttu-id="69324-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="69324-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69324-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="69324-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69324-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69324-107">DESCRIPTION</span></span>
<span data-ttu-id="69324-108">Löschen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="69324-108">Delete an association.</span></span>

## <span data-ttu-id="69324-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69324-109">EXAMPLES</span></span>

### <span data-ttu-id="69324-110">Beispiel 1: Entfernen einer benutzerdefinierten Anbieter zuordnung.</span><span class="sxs-lookup"><span data-stu-id="69324-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="69324-111">Entfernen einer benutzerdefinierten Anbieter zuordnung</span><span class="sxs-lookup"><span data-stu-id="69324-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="69324-112">Beispiel 2: Entfernen einer benutzerdefinierten Anbieter zuordnung zu Piping</span><span class="sxs-lookup"><span data-stu-id="69324-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="69324-113">Entfernen Einer benutzerdefinierten Anbieter zuordnung mit Piping und dem Feature "PassThru", um Erfolg oder Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="69324-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="69324-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69324-114">PARAMETERS</span></span>

### <span data-ttu-id="69324-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69324-115">-AsJob</span></span>
<span data-ttu-id="69324-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="69324-116">Run the command as a job</span></span>

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

### <span data-ttu-id="69324-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69324-117">-DefaultProfile</span></span>
<span data-ttu-id="69324-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69324-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69324-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69324-119">-InputObject</span></span>
<span data-ttu-id="69324-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="69324-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="69324-121">-Name</span><span class="sxs-lookup"><span data-stu-id="69324-121">-Name</span></span>
<span data-ttu-id="69324-122">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="69324-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69324-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69324-123">-NoWait</span></span>
<span data-ttu-id="69324-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="69324-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69324-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69324-125">-PassThru</span></span>
<span data-ttu-id="69324-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="69324-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69324-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="69324-127">-Scope</span></span>
<span data-ttu-id="69324-128">Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="69324-128">The scope of the association.</span></span>

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

### <span data-ttu-id="69324-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69324-129">-Confirm</span></span>
<span data-ttu-id="69324-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69324-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69324-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="69324-131">-WhatIf</span></span>
<span data-ttu-id="69324-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69324-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69324-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69324-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69324-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69324-134">CommonParameters</span></span>
<span data-ttu-id="69324-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69324-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69324-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69324-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69324-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69324-137">INPUTS</span></span>

### <span data-ttu-id="69324-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="69324-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="69324-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69324-139">OUTPUTS</span></span>

### <span data-ttu-id="69324-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69324-140">System.Boolean</span></span>

## <span data-ttu-id="69324-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69324-141">NOTES</span></span>

<span data-ttu-id="69324-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="69324-142">ALIASES</span></span>

<span data-ttu-id="69324-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="69324-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69324-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69324-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69324-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69324-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69324-146">INPUTOBJECT <ICustomProvidersIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="69324-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69324-147">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="69324-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="69324-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="69324-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69324-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69324-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="69324-150">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="69324-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="69324-151">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="69324-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="69324-152">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="69324-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="69324-153">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="69324-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="69324-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69324-154">RELATED LINKS</span></span>

