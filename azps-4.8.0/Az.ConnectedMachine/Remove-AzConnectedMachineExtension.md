---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009302"
---
# <span data-ttu-id="2f2aa-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2f2aa-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="2f2aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2aa-103">Der Vorgang zum Löschen der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="2f2aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f2aa-104">SYNTAX</span></span>

### <span data-ttu-id="2f2aa-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f2aa-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2f2aa-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2f2aa-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f2aa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f2aa-107">DESCRIPTION</span></span>
<span data-ttu-id="2f2aa-108">Der Vorgang zum Löschen der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="2f2aa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f2aa-109">EXAMPLES</span></span>

### <span data-ttu-id="2f2aa-110">Beispiel 1: Entfernen einer Computererweiterung</span><span class="sxs-lookup"><span data-stu-id="2f2aa-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="2f2aa-111">Löscht die Erweiterung auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="2f2aa-112">Beispiel 2: Entfernen der Erweiterung über die Pipeline</span><span class="sxs-lookup"><span data-stu-id="2f2aa-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="2f2aa-113">Entfernt alle Erweiterungen auf dem angegebenen Computer.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="2f2aa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f2aa-114">PARAMETERS</span></span>

### <span data-ttu-id="2f2aa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f2aa-115">-AsJob</span></span>
<span data-ttu-id="2f2aa-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f2aa-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2f2aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2aa-117">-DefaultProfile</span></span>
<span data-ttu-id="2f2aa-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f2aa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f2aa-119">-InputObject</span></span>
<span data-ttu-id="2f2aa-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2aa-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="2f2aa-121">-MachineName</span></span>
<span data-ttu-id="2f2aa-122">Der Name des Computers, auf dem die Erweiterung gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="2f2aa-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2f2aa-123">-Name</span></span>
<span data-ttu-id="2f2aa-124">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="2f2aa-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2f2aa-125">-NoWait</span></span>
<span data-ttu-id="2f2aa-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2f2aa-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2f2aa-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f2aa-127">-PassThru</span></span>
<span data-ttu-id="2f2aa-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2f2aa-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2f2aa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2aa-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f2aa-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f2aa-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2f2aa-131">-SubscriptionId</span></span>
<span data-ttu-id="2f2aa-132">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2f2aa-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2f2aa-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f2aa-134">-Confirm</span></span>
<span data-ttu-id="2f2aa-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f2aa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f2aa-136">-WhatIf</span></span>
<span data-ttu-id="2f2aa-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f2aa-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f2aa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2aa-139">CommonParameters</span></span>
<span data-ttu-id="2f2aa-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2aa-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f2aa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2aa-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f2aa-142">INPUTS</span></span>

### <span data-ttu-id="2f2aa-143">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="2f2aa-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="2f2aa-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f2aa-144">OUTPUTS</span></span>

### <span data-ttu-id="2f2aa-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f2aa-145">System.Boolean</span></span>

## <span data-ttu-id="2f2aa-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f2aa-146">NOTES</span></span>

<span data-ttu-id="2f2aa-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="2f2aa-147">ALIASES</span></span>

<span data-ttu-id="2f2aa-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f2aa-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f2aa-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f2aa-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f2aa-151">Inputobject <IConnectedMachineIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2f2aa-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f2aa-152">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="2f2aa-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2f2aa-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f2aa-154">`[Name <String>]`: Der Name der hybridmaschine.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="2f2aa-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2f2aa-156">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2f2aa-157">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2f2aa-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2f2aa-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f2aa-158">RELATED LINKS</span></span>

