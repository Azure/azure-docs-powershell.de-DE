---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008015"
---
# <span data-ttu-id="d85f1-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d85f1-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d85f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d85f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d85f1-103">Löscht den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="d85f1-103">Deletes the workspace.</span></span>

## <span data-ttu-id="d85f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d85f1-104">SYNTAX</span></span>

### <span data-ttu-id="d85f1-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d85f1-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d85f1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d85f1-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d85f1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d85f1-107">DESCRIPTION</span></span>
<span data-ttu-id="d85f1-108">Löscht den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="d85f1-108">Deletes the workspace.</span></span>

## <span data-ttu-id="d85f1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d85f1-109">EXAMPLES</span></span>

### <span data-ttu-id="d85f1-110">Beispiel 1: Entfernen eines Arbeitsbereichs von databricks</span><span class="sxs-lookup"><span data-stu-id="d85f1-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="d85f1-111">Mit diesem Befehl wird ein databricks-Arbeitsbereich aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="d85f1-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="d85f1-112">Beispiel 2: Entfernen eines Arbeitsbereichs "databricks" nach Objekt</span><span class="sxs-lookup"><span data-stu-id="d85f1-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="d85f1-113">Mit diesem Befehl wird ein databricks-Arbeitsbereich aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="d85f1-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="d85f1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d85f1-114">PARAMETERS</span></span>

### <span data-ttu-id="d85f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d85f1-115">-AsJob</span></span>
<span data-ttu-id="d85f1-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d85f1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d85f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85f1-117">-DefaultProfile</span></span>
<span data-ttu-id="d85f1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d85f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85f1-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d85f1-119">-InputObject</span></span>
<span data-ttu-id="d85f1-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d85f1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d85f1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d85f1-121">-Name</span></span>
<span data-ttu-id="d85f1-122">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d85f1-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85f1-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d85f1-123">-NoWait</span></span>
<span data-ttu-id="d85f1-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d85f1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d85f1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d85f1-125">-PassThru</span></span>
<span data-ttu-id="d85f1-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="d85f1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d85f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="d85f1-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d85f1-128">The name of the resource group.</span></span>
<span data-ttu-id="d85f1-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d85f1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d85f1-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d85f1-130">-SubscriptionId</span></span>
<span data-ttu-id="d85f1-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d85f1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d85f1-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d85f1-132">-Confirm</span></span>
<span data-ttu-id="d85f1-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d85f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85f1-134">-WhatIf</span></span>
<span data-ttu-id="d85f1-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d85f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85f1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d85f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85f1-137">CommonParameters</span></span>
<span data-ttu-id="d85f1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85f1-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d85f1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85f1-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d85f1-140">INPUTS</span></span>

### <span data-ttu-id="d85f1-141">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d85f1-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d85f1-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d85f1-142">OUTPUTS</span></span>

### <span data-ttu-id="d85f1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d85f1-143">System.Boolean</span></span>

## <span data-ttu-id="d85f1-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d85f1-144">NOTES</span></span>

<span data-ttu-id="d85f1-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="d85f1-145">ALIASES</span></span>

<span data-ttu-id="d85f1-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d85f1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d85f1-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d85f1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d85f1-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d85f1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d85f1-149">Inputobject <IDatabricksIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d85f1-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d85f1-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d85f1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d85f1-151">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="d85f1-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d85f1-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d85f1-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d85f1-153">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d85f1-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d85f1-154">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d85f1-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d85f1-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d85f1-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d85f1-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d85f1-156">RELATED LINKS</span></span>

