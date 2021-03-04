---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 6d3a6863044722be49efb78a71e3e0fbe82db5e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943019"
---
# <span data-ttu-id="2ebc9-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="2ebc9-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="2ebc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ebc9-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebc9-103">Löschen sie eine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-103">Delete an association.</span></span>

## <span data-ttu-id="2ebc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ebc9-104">SYNTAX</span></span>

### <span data-ttu-id="2ebc9-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ebc9-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ebc9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ebc9-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ebc9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ebc9-107">DESCRIPTION</span></span>
<span data-ttu-id="2ebc9-108">Löschen sie eine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-108">Delete an association.</span></span>

## <span data-ttu-id="2ebc9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ebc9-109">EXAMPLES</span></span>

### <span data-ttu-id="2ebc9-110">Beispiel 1: Entfernen einer benutzerdefinierten Anbieter zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="2ebc9-111">Entfernen sie eine benutzerdefinierte Anbieter zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="2ebc9-112">Beispiel 2: Entfernen einer benutzerdefinierten Anbieter-Zuordnung mit Piping</span><span class="sxs-lookup"><span data-stu-id="2ebc9-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="2ebc9-113">Entfernen Sie eine benutzerdefinierte Anbieter zuordnung, indem Sie Piping und das PassThru-Feature verwenden, um Erfolg oder Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="2ebc9-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ebc9-114">PARAMETERS</span></span>

### <span data-ttu-id="2ebc9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ebc9-115">-AsJob</span></span>
<span data-ttu-id="2ebc9-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2ebc9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2ebc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebc9-117">-DefaultProfile</span></span>
<span data-ttu-id="2ebc9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebc9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ebc9-119">-InputObject</span></span>
<span data-ttu-id="2ebc9-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ebc9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ebc9-121">-Name</span></span>
<span data-ttu-id="2ebc9-122">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-122">The name of the association.</span></span>

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

### <span data-ttu-id="2ebc9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ebc9-123">-NoWait</span></span>
<span data-ttu-id="2ebc9-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2ebc9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ebc9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ebc9-125">-PassThru</span></span>
<span data-ttu-id="2ebc9-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2ebc9-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="2ebc9-127">-Scope</span></span>
<span data-ttu-id="2ebc9-128">Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-128">The scope of the association.</span></span>

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

### <span data-ttu-id="2ebc9-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ebc9-129">-Confirm</span></span>
<span data-ttu-id="2ebc9-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ebc9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebc9-131">-WhatIf</span></span>
<span data-ttu-id="2ebc9-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ebc9-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ebc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebc9-134">CommonParameters</span></span>
<span data-ttu-id="2ebc9-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebc9-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ebc9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebc9-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ebc9-137">INPUTS</span></span>

### <span data-ttu-id="2ebc9-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="2ebc9-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="2ebc9-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ebc9-139">OUTPUTS</span></span>

### <span data-ttu-id="2ebc9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ebc9-140">System.Boolean</span></span>

## <span data-ttu-id="2ebc9-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ebc9-141">NOTES</span></span>

<span data-ttu-id="2ebc9-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2ebc9-142">ALIASES</span></span>

<span data-ttu-id="2ebc9-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2ebc9-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ebc9-144">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ebc9-145">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ebc9-146">INPUTOBJECT <ICustomProvidersIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2ebc9-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ebc9-147">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="2ebc9-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2ebc9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ebc9-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2ebc9-150">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="2ebc9-151">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="2ebc9-152">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2ebc9-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2ebc9-153">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="2ebc9-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2ebc9-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ebc9-154">RELATED LINKS</span></span>

