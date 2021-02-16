---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148372"
---
# <span data-ttu-id="73474-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="73474-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="73474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73474-102">SYNOPSIS</span></span>
<span data-ttu-id="73474-103">Aktualisiert einen vorhandenen benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="73474-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="73474-104">Der einzige Wert, der über PATCH aktualisiert werden kann, sind die Tags.</span><span class="sxs-lookup"><span data-stu-id="73474-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="73474-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73474-105">SYNTAX</span></span>

### <span data-ttu-id="73474-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="73474-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="73474-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="73474-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73474-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73474-108">DESCRIPTION</span></span>
<span data-ttu-id="73474-109">Aktualisiert einen vorhandenen benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="73474-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="73474-110">Der einzige Wert, der über PATCH aktualisiert werden kann, sind die Tags.</span><span class="sxs-lookup"><span data-stu-id="73474-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="73474-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73474-111">EXAMPLES</span></span>

### <span data-ttu-id="73474-112">Beispiel 1: Hinzufügen von Tags zu einem benutzerdefinierten Anbieter</span><span class="sxs-lookup"><span data-stu-id="73474-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="73474-113">Aktualisieren Sie die Tags eines benutzerdefinierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="73474-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="73474-114">Beispiel 2: Aktualisieren eines benutzerdefinierten Anbieters mit Piping</span><span class="sxs-lookup"><span data-stu-id="73474-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="73474-115">Aktualisieren Sie einen benutzerdefinierten Anbieter mithilfe der Piping.</span><span class="sxs-lookup"><span data-stu-id="73474-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="73474-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73474-116">PARAMETERS</span></span>

### <span data-ttu-id="73474-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73474-117">-DefaultProfile</span></span>
<span data-ttu-id="73474-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73474-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73474-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73474-119">-InputObject</span></span>
<span data-ttu-id="73474-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="73474-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73474-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73474-121">-Name</span></span>
<span data-ttu-id="73474-122">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="73474-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73474-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73474-123">-ResourceGroupName</span></span>
<span data-ttu-id="73474-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73474-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73474-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73474-125">-SubscriptionId</span></span>
<span data-ttu-id="73474-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="73474-126">The Azure subscription ID.</span></span>
<span data-ttu-id="73474-127">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="73474-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73474-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="73474-128">-Tag</span></span>
<span data-ttu-id="73474-129">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="73474-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73474-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73474-130">-Confirm</span></span>
<span data-ttu-id="73474-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73474-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73474-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73474-132">-WhatIf</span></span>
<span data-ttu-id="73474-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73474-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73474-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73474-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73474-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73474-135">CommonParameters</span></span>
<span data-ttu-id="73474-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73474-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73474-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73474-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73474-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73474-138">INPUTS</span></span>

### <span data-ttu-id="73474-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="73474-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="73474-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73474-140">OUTPUTS</span></span>

### <span data-ttu-id="73474-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="73474-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="73474-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73474-142">NOTES</span></span>

<span data-ttu-id="73474-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="73474-143">ALIASES</span></span>

<span data-ttu-id="73474-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="73474-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73474-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73474-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73474-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73474-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73474-147">INPUTOBJECT <ICustomProvidersIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="73474-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73474-148">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="73474-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="73474-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="73474-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73474-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73474-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="73474-151">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="73474-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="73474-152">`[Scope <String>]`: Der Umfang der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="73474-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="73474-153">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="73474-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="73474-154">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="73474-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="73474-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73474-155">RELATED LINKS</span></span>

