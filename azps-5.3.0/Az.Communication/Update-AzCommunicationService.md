---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473155"
---
# <span data-ttu-id="88aa1-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="88aa1-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="88aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="88aa1-103">Vorgang zum Aktualisieren eines vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="88aa1-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="88aa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88aa1-104">SYNTAX</span></span>

### <span data-ttu-id="88aa1-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="88aa1-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88aa1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="88aa1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88aa1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88aa1-107">DESCRIPTION</span></span>
<span data-ttu-id="88aa1-108">Vorgang zum Aktualisieren eines vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="88aa1-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="88aa1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88aa1-109">EXAMPLES</span></span>

### <span data-ttu-id="88aa1-110">Beispiel 1: Aktualisieren einer vorhandenen RESSOURCENA0 für Tags</span><span class="sxs-lookup"><span data-stu-id="88aa1-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="88aa1-111">Fügt die angegebenen Tags an die angegebene Ressource "ACS" an.</span><span class="sxs-lookup"><span data-stu-id="88aa1-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="88aa1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88aa1-112">PARAMETERS</span></span>

### <span data-ttu-id="88aa1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88aa1-113">-DefaultProfile</span></span>
<span data-ttu-id="88aa1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88aa1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88aa1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88aa1-115">-InputObject</span></span>
<span data-ttu-id="88aa1-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="88aa1-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88aa1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="88aa1-117">-Name</span></span>
<span data-ttu-id="88aa1-118">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="88aa1-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88aa1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88aa1-119">-ResourceGroupName</span></span>
<span data-ttu-id="88aa1-120">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="88aa1-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="88aa1-121">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="88aa1-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="88aa1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88aa1-122">-SubscriptionId</span></span>
<span data-ttu-id="88aa1-123">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="88aa1-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="88aa1-124">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="88aa1-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88aa1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="88aa1-125">-Tag</span></span>
<span data-ttu-id="88aa1-126">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="88aa1-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="88aa1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88aa1-127">-Confirm</span></span>
<span data-ttu-id="88aa1-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88aa1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88aa1-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="88aa1-129">-WhatIf</span></span>
<span data-ttu-id="88aa1-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88aa1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88aa1-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88aa1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88aa1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88aa1-132">CommonParameters</span></span>
<span data-ttu-id="88aa1-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88aa1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88aa1-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88aa1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88aa1-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88aa1-135">INPUTS</span></span>

### <span data-ttu-id="88aa1-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="88aa1-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="88aa1-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88aa1-137">OUTPUTS</span></span>

### <span data-ttu-id="88aa1-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="88aa1-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="88aa1-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="88aa1-139">NOTES</span></span>

<span data-ttu-id="88aa1-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="88aa1-140">ALIASES</span></span>

<span data-ttu-id="88aa1-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="88aa1-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88aa1-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88aa1-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88aa1-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88aa1-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88aa1-144">INPUTOBJECT <ICommunicationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="88aa1-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88aa1-145">`[CommunicationServiceName <String>]`: Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="88aa1-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="88aa1-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="88aa1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88aa1-147">`[Location <String>]`: Die Region Azure</span><span class="sxs-lookup"><span data-stu-id="88aa1-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="88aa1-148">`[OperationId <String>]`: Die ID eines laufenden asynchronen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="88aa1-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="88aa1-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="88aa1-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="88aa1-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="88aa1-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="88aa1-151">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="88aa1-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="88aa1-152">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="88aa1-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="88aa1-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="88aa1-153">RELATED LINKS</span></span>

