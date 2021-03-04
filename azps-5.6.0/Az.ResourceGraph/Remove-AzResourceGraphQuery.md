---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 0253a5fa7cf5ff13c678eb0a6d86c31335239fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943630"
---
# <span data-ttu-id="e329d-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="e329d-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="e329d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e329d-102">SYNOPSIS</span></span>
<span data-ttu-id="e329d-103">Löschen sie eine Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="e329d-103">Delete a graph query.</span></span>

## <span data-ttu-id="e329d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e329d-104">SYNTAX</span></span>

### <span data-ttu-id="e329d-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e329d-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e329d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e329d-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e329d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e329d-107">DESCRIPTION</span></span>
<span data-ttu-id="e329d-108">Löschen sie eine Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="e329d-108">Delete a graph query.</span></span>

## <span data-ttu-id="e329d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e329d-109">EXAMPLES</span></span>

### <span data-ttu-id="e329d-110">Beispiel 1: Entfernen einer Ressourcendiagrammabfrage nach Name</span><span class="sxs-lookup"><span data-stu-id="e329d-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="e329d-111">Mit diesem Befehl wird eine Ressourcendiagrammabfrage nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="e329d-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="e329d-112">Beispiel 2: Entfernen einer Ressourcendiagrammabfrage nach Objekt</span><span class="sxs-lookup"><span data-stu-id="e329d-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="e329d-113">Mit diesem Befehl wird eine Ressourcendiagrammabfrage nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="e329d-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="e329d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e329d-114">PARAMETERS</span></span>

### <span data-ttu-id="e329d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e329d-115">-DefaultProfile</span></span>
<span data-ttu-id="e329d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e329d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e329d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e329d-117">-InputObject</span></span>
<span data-ttu-id="e329d-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e329d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e329d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e329d-119">-Name</span></span>
<span data-ttu-id="e329d-120">Der Name der Graph Query-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e329d-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="e329d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e329d-121">-PassThru</span></span>
<span data-ttu-id="e329d-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e329d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e329d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e329d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e329d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e329d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e329d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e329d-125">-SubscriptionId</span></span>
<span data-ttu-id="e329d-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e329d-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="e329d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e329d-127">-Confirm</span></span>
<span data-ttu-id="e329d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e329d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e329d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e329d-129">-WhatIf</span></span>
<span data-ttu-id="e329d-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e329d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e329d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e329d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e329d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e329d-132">CommonParameters</span></span>
<span data-ttu-id="e329d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e329d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e329d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e329d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e329d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e329d-135">INPUTS</span></span>

### <span data-ttu-id="e329d-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="e329d-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="e329d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e329d-137">OUTPUTS</span></span>

### <span data-ttu-id="e329d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e329d-138">System.Boolean</span></span>

## <span data-ttu-id="e329d-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e329d-139">NOTES</span></span>

<span data-ttu-id="e329d-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e329d-140">ALIASES</span></span>

<span data-ttu-id="e329d-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e329d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e329d-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e329d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e329d-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e329d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e329d-144">INPUTOBJECT <IResourceGraphIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="e329d-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e329d-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e329d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e329d-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e329d-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e329d-147">`[ResourceName <String>]`: Der Name der Graph Query-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e329d-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="e329d-148">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e329d-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="e329d-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e329d-149">RELATED LINKS</span></span>

