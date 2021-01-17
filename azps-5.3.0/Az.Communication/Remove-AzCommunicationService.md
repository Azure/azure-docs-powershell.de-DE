---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473160"
---
# <span data-ttu-id="425e6-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="425e6-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="425e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="425e6-102">SYNOPSIS</span></span>
<span data-ttu-id="425e6-103">Vorgang zum Löschen eines CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="425e6-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="425e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="425e6-104">SYNTAX</span></span>

### <span data-ttu-id="425e6-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="425e6-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="425e6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="425e6-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="425e6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="425e6-107">DESCRIPTION</span></span>
<span data-ttu-id="425e6-108">Vorgang zum Löschen eines CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="425e6-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="425e6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="425e6-109">EXAMPLES</span></span>

### <span data-ttu-id="425e6-110">Beispiel 1: Entfernen der angegebenen Azure-Kommunikationsressource</span><span class="sxs-lookup"><span data-stu-id="425e6-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="425e6-111">Entfernen/Löschen Sie die Azure-Kommunikationsressource.</span><span class="sxs-lookup"><span data-stu-id="425e6-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="425e6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="425e6-112">PARAMETERS</span></span>

### <span data-ttu-id="425e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="425e6-113">-AsJob</span></span>
<span data-ttu-id="425e6-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="425e6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="425e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425e6-115">-DefaultProfile</span></span>
<span data-ttu-id="425e6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="425e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425e6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="425e6-117">-InputObject</span></span>
<span data-ttu-id="425e6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="425e6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="425e6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="425e6-119">-Name</span></span>
<span data-ttu-id="425e6-120">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="425e6-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="425e6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="425e6-121">-NoWait</span></span>
<span data-ttu-id="425e6-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="425e6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="425e6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="425e6-123">-PassThru</span></span>
<span data-ttu-id="425e6-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="425e6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="425e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="425e6-125">-ResourceGroupName</span></span>
<span data-ttu-id="425e6-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="425e6-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="425e6-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="425e6-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="425e6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="425e6-128">-SubscriptionId</span></span>
<span data-ttu-id="425e6-129">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="425e6-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="425e6-130">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="425e6-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="425e6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="425e6-131">-Confirm</span></span>
<span data-ttu-id="425e6-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="425e6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="425e6-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="425e6-133">-WhatIf</span></span>
<span data-ttu-id="425e6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="425e6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="425e6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="425e6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="425e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425e6-136">CommonParameters</span></span>
<span data-ttu-id="425e6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425e6-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="425e6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425e6-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="425e6-139">INPUTS</span></span>

### <span data-ttu-id="425e6-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="425e6-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="425e6-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="425e6-141">OUTPUTS</span></span>

### <span data-ttu-id="425e6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="425e6-142">System.Boolean</span></span>

## <span data-ttu-id="425e6-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="425e6-143">NOTES</span></span>

<span data-ttu-id="425e6-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="425e6-144">ALIASES</span></span>

<span data-ttu-id="425e6-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="425e6-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="425e6-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="425e6-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="425e6-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="425e6-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="425e6-148">INPUTOBJECT <ICommunicationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="425e6-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="425e6-149">`[CommunicationServiceName <String>]`: Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="425e6-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="425e6-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="425e6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="425e6-151">`[Location <String>]`: Die Region Azure</span><span class="sxs-lookup"><span data-stu-id="425e6-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="425e6-152">`[OperationId <String>]`: Die ID eines laufenden asynchronen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="425e6-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="425e6-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="425e6-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="425e6-154">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="425e6-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="425e6-155">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="425e6-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="425e6-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="425e6-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="425e6-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="425e6-157">RELATED LINKS</span></span>

