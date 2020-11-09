---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297309"
---
# <span data-ttu-id="15615-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="15615-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="15615-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15615-102">SYNOPSIS</span></span>
<span data-ttu-id="15615-103">Löscht den Arbeitsbereich vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="15615-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="15615-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15615-104">SYNTAX</span></span>

### <span data-ttu-id="15615-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="15615-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="15615-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15615-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15615-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15615-107">DESCRIPTION</span></span>
<span data-ttu-id="15615-108">Löscht den Arbeitsbereich vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="15615-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="15615-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15615-109">EXAMPLES</span></span>

### <span data-ttu-id="15615-110">Beispiel 1: Entfernen eines vnet-Peerings von databricks nach Name</span><span class="sxs-lookup"><span data-stu-id="15615-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="15615-111">Mit diesem Befehl wird ein vnet-Peering von databricks nach Name entfernt</span><span class="sxs-lookup"><span data-stu-id="15615-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="15615-112">Beispiel 2: Entfernen eines vnet-Peerings von databricks nach Objekt</span><span class="sxs-lookup"><span data-stu-id="15615-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="15615-113">Dieser Befehl entfernt ein vnet-Peering von databricks nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="15615-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="15615-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="15615-114">PARAMETERS</span></span>

### <span data-ttu-id="15615-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15615-115">-AsJob</span></span>
<span data-ttu-id="15615-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="15615-116">Run the command as a job</span></span>

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

### <span data-ttu-id="15615-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15615-117">-DefaultProfile</span></span>
<span data-ttu-id="15615-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15615-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15615-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15615-119">-InputObject</span></span>
<span data-ttu-id="15615-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="15615-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15615-121">-Name</span><span class="sxs-lookup"><span data-stu-id="15615-121">-Name</span></span>
<span data-ttu-id="15615-122">Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="15615-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="15615-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="15615-123">-NoWait</span></span>
<span data-ttu-id="15615-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="15615-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15615-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15615-125">-PassThru</span></span>
<span data-ttu-id="15615-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="15615-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15615-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15615-127">-ResourceGroupName</span></span>
<span data-ttu-id="15615-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15615-128">The name of the resource group.</span></span>
<span data-ttu-id="15615-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="15615-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15615-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="15615-130">-SubscriptionId</span></span>
<span data-ttu-id="15615-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="15615-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15615-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15615-132">-WorkspaceName</span></span>
<span data-ttu-id="15615-133">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="15615-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="15615-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15615-134">-Confirm</span></span>
<span data-ttu-id="15615-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15615-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15615-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15615-136">-WhatIf</span></span>
<span data-ttu-id="15615-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15615-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15615-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15615-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15615-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15615-139">CommonParameters</span></span>
<span data-ttu-id="15615-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15615-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15615-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15615-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15615-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15615-142">INPUTS</span></span>

### <span data-ttu-id="15615-143">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="15615-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="15615-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15615-144">OUTPUTS</span></span>

### <span data-ttu-id="15615-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15615-145">System.Boolean</span></span>

## <span data-ttu-id="15615-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="15615-146">NOTES</span></span>

<span data-ttu-id="15615-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="15615-147">ALIASES</span></span>

<span data-ttu-id="15615-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15615-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15615-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15615-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15615-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="15615-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15615-151">Inputobject <IDatabricksIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="15615-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15615-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="15615-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15615-153">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="15615-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="15615-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15615-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15615-155">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="15615-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="15615-156">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="15615-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15615-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="15615-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="15615-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15615-158">RELATED LINKS</span></span>

