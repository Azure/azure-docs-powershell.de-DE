---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171317"
---
# <span data-ttu-id="485cf-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="485cf-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="485cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="485cf-102">SYNOPSIS</span></span>
<span data-ttu-id="485cf-103">Vorgang zum Aktualisieren eines vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="485cf-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="485cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="485cf-104">SYNTAX</span></span>

### <span data-ttu-id="485cf-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="485cf-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="485cf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="485cf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="485cf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="485cf-107">DESCRIPTION</span></span>
<span data-ttu-id="485cf-108">Vorgang zum Aktualisieren eines vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="485cf-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="485cf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="485cf-109">EXAMPLES</span></span>

### <span data-ttu-id="485cf-110">Beispiel 1: Aktualisieren einer vorhandenen AcS-Ressource, um Tags zu erhalten</span><span class="sxs-lookup"><span data-stu-id="485cf-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="485cf-111">Fügt die angegebenen Tags an die angegebene AcS-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="485cf-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="485cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="485cf-112">PARAMETERS</span></span>

### <span data-ttu-id="485cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485cf-113">-DefaultProfile</span></span>
<span data-ttu-id="485cf-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="485cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="485cf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="485cf-115">-InputObject</span></span>
<span data-ttu-id="485cf-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="485cf-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="485cf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="485cf-117">-Name</span></span>
<span data-ttu-id="485cf-118">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="485cf-118">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="485cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="485cf-120">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="485cf-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="485cf-121">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="485cf-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="485cf-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="485cf-122">-SubscriptionId</span></span>
<span data-ttu-id="485cf-123">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="485cf-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="485cf-124">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="485cf-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="485cf-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="485cf-125">-Tag</span></span>
<span data-ttu-id="485cf-126">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="485cf-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="485cf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="485cf-127">-Confirm</span></span>
<span data-ttu-id="485cf-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="485cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="485cf-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="485cf-129">-WhatIf</span></span>
<span data-ttu-id="485cf-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="485cf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="485cf-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="485cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="485cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485cf-132">CommonParameters</span></span>
<span data-ttu-id="485cf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485cf-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="485cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485cf-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="485cf-135">INPUTS</span></span>

### <span data-ttu-id="485cf-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="485cf-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="485cf-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="485cf-137">OUTPUTS</span></span>

### <span data-ttu-id="485cf-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="485cf-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="485cf-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="485cf-139">NOTES</span></span>

<span data-ttu-id="485cf-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="485cf-140">ALIASES</span></span>

<span data-ttu-id="485cf-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="485cf-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="485cf-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="485cf-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="485cf-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="485cf-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="485cf-144">INPUTOBJECT <ICommunicationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="485cf-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="485cf-145">`[CommunicationServiceName <String>]`: Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="485cf-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="485cf-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="485cf-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="485cf-147">`[Location <String>]`: Die Region Azure</span><span class="sxs-lookup"><span data-stu-id="485cf-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="485cf-148">`[OperationId <String>]`: Die ID eines laufenden asynchronen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="485cf-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="485cf-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="485cf-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="485cf-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="485cf-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="485cf-151">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="485cf-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="485cf-152">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="485cf-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="485cf-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="485cf-153">RELATED LINKS</span></span>

