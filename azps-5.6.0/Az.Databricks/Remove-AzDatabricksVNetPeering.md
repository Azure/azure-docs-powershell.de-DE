---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932995"
---
# <span data-ttu-id="b3e4c-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="b3e4c-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="b3e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e4c-103">Löscht den Arbeitsbereich vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="b3e4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3e4c-104">SYNTAX</span></span>

### <span data-ttu-id="b3e4c-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3e4c-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b3e4c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3e4c-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3e4c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3e4c-107">DESCRIPTION</span></span>
<span data-ttu-id="b3e4c-108">Löscht den Arbeitsbereich vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="b3e4c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3e4c-109">EXAMPLES</span></span>

### <span data-ttu-id="b3e4c-110">Beispiel 1: Entfernen eines Vnet-Peerings von Databricks nach Name</span><span class="sxs-lookup"><span data-stu-id="b3e4c-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="b3e4c-111">Mit diesem Befehl wird ein vnet-Peering von Databricks nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="b3e4c-112">Beispiel 2: Entfernen eines Vnet-Peerings von Databricks nach Objekt</span><span class="sxs-lookup"><span data-stu-id="b3e4c-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="b3e4c-113">Mit diesem Befehl wird ein vnet-Peering von Databricks nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="b3e4c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b3e4c-114">PARAMETERS</span></span>

### <span data-ttu-id="b3e4c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3e4c-115">-AsJob</span></span>
<span data-ttu-id="b3e4c-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3e4c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3e4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e4c-117">-DefaultProfile</span></span>
<span data-ttu-id="b3e4c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e4c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e4c-119">-InputObject</span></span>
<span data-ttu-id="b3e4c-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e4c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b3e4c-121">-Name</span></span>
<span data-ttu-id="b3e4c-122">Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="b3e4c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3e4c-123">-NoWait</span></span>
<span data-ttu-id="b3e4c-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b3e4c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3e4c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3e4c-125">-PassThru</span></span>
<span data-ttu-id="b3e4c-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3e4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3e4c-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-128">The name of the resource group.</span></span>
<span data-ttu-id="b3e4c-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b3e4c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3e4c-130">-SubscriptionId</span></span>
<span data-ttu-id="b3e4c-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b3e4c-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b3e4c-132">-WorkspaceName</span></span>
<span data-ttu-id="b3e4c-133">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="b3e4c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3e4c-134">-Confirm</span></span>
<span data-ttu-id="b3e4c-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e4c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e4c-136">-WhatIf</span></span>
<span data-ttu-id="b3e4c-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e4c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e4c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e4c-139">CommonParameters</span></span>
<span data-ttu-id="b3e4c-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e4c-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e4c-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3e4c-142">INPUTS</span></span>

### <span data-ttu-id="b3e4c-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="b3e4c-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b3e4c-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3e4c-144">OUTPUTS</span></span>

### <span data-ttu-id="b3e4c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3e4c-145">System.Boolean</span></span>

## <span data-ttu-id="b3e4c-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b3e4c-146">NOTES</span></span>

<span data-ttu-id="b3e4c-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b3e4c-147">ALIASES</span></span>

<span data-ttu-id="b3e4c-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b3e4c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3e4c-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3e4c-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3e4c-151">INPUTOBJECT <IDatabricksIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b3e4c-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3e4c-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b3e4c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3e4c-153">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b3e4c-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b3e4c-155">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="b3e4c-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b3e4c-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b3e4c-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b3e4c-158">RELATED LINKS</span></span>

