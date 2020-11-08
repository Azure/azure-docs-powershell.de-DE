---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175303"
---
# <span data-ttu-id="5e3df-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="5e3df-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="5e3df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e3df-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3df-103">Der Vorgang zum Entfernen einer Hybrid Computeridentität in Azure.</span><span class="sxs-lookup"><span data-stu-id="5e3df-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="5e3df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e3df-104">SYNTAX</span></span>

### <span data-ttu-id="5e3df-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e3df-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e3df-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3df-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e3df-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e3df-107">DESCRIPTION</span></span>
<span data-ttu-id="5e3df-108">Der Vorgang zum Entfernen einer Hybrid Computeridentität in Azure.</span><span class="sxs-lookup"><span data-stu-id="5e3df-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="5e3df-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e3df-109">EXAMPLES</span></span>

### <span data-ttu-id="5e3df-110">Beispiel 1: Entfernen eines verbundenen Computers</span><span class="sxs-lookup"><span data-stu-id="5e3df-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="5e3df-111">Löscht den verbundenen Computer.</span><span class="sxs-lookup"><span data-stu-id="5e3df-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="5e3df-112">Beispiel 2: Entfernen von verbundenen Computern über die Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e3df-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="5e3df-113">Entfernt alle Computer in der `contoso-connected-machines` Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e3df-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="5e3df-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e3df-114">PARAMETERS</span></span>

### <span data-ttu-id="5e3df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e3df-115">-DefaultProfile</span></span>
<span data-ttu-id="5e3df-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e3df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e3df-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e3df-117">-InputObject</span></span>
<span data-ttu-id="5e3df-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5e3df-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e3df-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5e3df-119">-Name</span></span>
<span data-ttu-id="5e3df-120">Der Name der hybridmaschine.</span><span class="sxs-lookup"><span data-stu-id="5e3df-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="5e3df-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e3df-121">-PassThru</span></span>
<span data-ttu-id="5e3df-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="5e3df-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e3df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e3df-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e3df-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e3df-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e3df-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5e3df-125">-SubscriptionId</span></span>
<span data-ttu-id="5e3df-126">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5e3df-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5e3df-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5e3df-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5e3df-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e3df-128">-Confirm</span></span>
<span data-ttu-id="5e3df-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e3df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e3df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e3df-130">-WhatIf</span></span>
<span data-ttu-id="5e3df-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e3df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e3df-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e3df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e3df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3df-133">CommonParameters</span></span>
<span data-ttu-id="5e3df-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e3df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3df-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e3df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3df-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e3df-136">INPUTS</span></span>

### <span data-ttu-id="5e3df-137">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="5e3df-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="5e3df-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e3df-138">OUTPUTS</span></span>

### <span data-ttu-id="5e3df-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e3df-139">System.Boolean</span></span>

## <span data-ttu-id="5e3df-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e3df-140">NOTES</span></span>

<span data-ttu-id="5e3df-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="5e3df-141">ALIASES</span></span>

<span data-ttu-id="5e3df-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e3df-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e3df-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e3df-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e3df-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5e3df-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e3df-145">Inputobject <IConnectedMachineIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5e3df-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e3df-146">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="5e3df-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="5e3df-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5e3df-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e3df-148">`[Name <String>]`: Der Name der hybridmaschine.</span><span class="sxs-lookup"><span data-stu-id="5e3df-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="5e3df-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e3df-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5e3df-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5e3df-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5e3df-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5e3df-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5e3df-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e3df-152">RELATED LINKS</span></span>

