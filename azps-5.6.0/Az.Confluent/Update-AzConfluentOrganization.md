---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948896"
---
# <span data-ttu-id="c12a1-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="c12a1-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="c12a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c12a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c12a1-103">Aktualisieren der Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="c12a1-103">Update Organization resource</span></span>

## <span data-ttu-id="c12a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c12a1-104">SYNTAX</span></span>

### <span data-ttu-id="c12a1-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c12a1-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c12a1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c12a1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c12a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c12a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c12a1-108">Aktualisieren der Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="c12a1-108">Update Organization resource</span></span>

## <span data-ttu-id="c12a1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c12a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c12a1-110">Beispiel 1: Aktualisieren einer kongenenten Organisation nach Name</span><span class="sxs-lookup"><span data-stu-id="c12a1-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="c12a1-111">Mit diesem Befehl wird eine konfluente Organisation nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c12a1-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="c12a1-112">Beispiel 2: Aktualisieren einer kongenenten Organisation per Pipeline</span><span class="sxs-lookup"><span data-stu-id="c12a1-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="c12a1-113">Mit diesem Befehl wird eine kongenente Organisation per Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c12a1-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="c12a1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c12a1-114">PARAMETERS</span></span>

### <span data-ttu-id="c12a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12a1-115">-DefaultProfile</span></span>
<span data-ttu-id="c12a1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c12a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c12a1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c12a1-117">-InputObject</span></span>
<span data-ttu-id="c12a1-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c12a1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c12a1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c12a1-119">-Name</span></span>
<span data-ttu-id="c12a1-120">Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="c12a1-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c12a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c12a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="c12a1-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c12a1-122">Resource group name</span></span>

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

### <span data-ttu-id="c12a1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c12a1-123">-SubscriptionId</span></span>
<span data-ttu-id="c12a1-124">Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="c12a1-124">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="c12a1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c12a1-125">-Tag</span></span>
<span data-ttu-id="c12a1-126">ARM Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="c12a1-126">ARM resource tags</span></span>

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

### <span data-ttu-id="c12a1-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c12a1-127">-Confirm</span></span>
<span data-ttu-id="c12a1-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c12a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12a1-129">-WhatIf</span></span>
<span data-ttu-id="c12a1-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c12a1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c12a1-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c12a1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12a1-132">CommonParameters</span></span>
<span data-ttu-id="c12a1-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12a1-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c12a1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12a1-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c12a1-135">INPUTS</span></span>

### <span data-ttu-id="c12a1-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="c12a1-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="c12a1-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c12a1-137">OUTPUTS</span></span>

### <span data-ttu-id="c12a1-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="c12a1-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="c12a1-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c12a1-139">NOTES</span></span>

<span data-ttu-id="c12a1-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c12a1-140">ALIASES</span></span>

<span data-ttu-id="c12a1-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c12a1-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c12a1-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c12a1-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c12a1-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c12a1-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c12a1-144">INPUTOBJECT <IConfluentIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="c12a1-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c12a1-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c12a1-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c12a1-146">`[OrganizationName <String>]`: Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="c12a1-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="c12a1-147">`[ResourceGroupName <String>]`: Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c12a1-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="c12a1-148">`[SubscriptionId <String>]`: Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="c12a1-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="c12a1-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c12a1-149">RELATED LINKS</span></span>

