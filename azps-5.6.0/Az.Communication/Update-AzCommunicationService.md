---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 53127b970c3c2f588a54eaec3dcd9ea1174a7053
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938915"
---
# <span data-ttu-id="ba955-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="ba955-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="ba955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba955-102">SYNOPSIS</span></span>
<span data-ttu-id="ba955-103">Vorgang zum Aktualisieren eines vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="ba955-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="ba955-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba955-104">SYNTAX</span></span>

### <span data-ttu-id="ba955-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba955-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba955-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ba955-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba955-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba955-107">DESCRIPTION</span></span>
<span data-ttu-id="ba955-108">Vorgang zum Aktualisieren eines vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="ba955-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="ba955-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba955-109">EXAMPLES</span></span>

### <span data-ttu-id="ba955-110">Beispiel 1: Aktualisieren einer vorhandenen ACS-Ressource auf Tags</span><span class="sxs-lookup"><span data-stu-id="ba955-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="ba955-111">Fügt die angegebenen Tags an die angegebene ACS-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="ba955-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="ba955-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba955-112">PARAMETERS</span></span>

### <span data-ttu-id="ba955-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba955-113">-DefaultProfile</span></span>
<span data-ttu-id="ba955-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba955-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba955-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba955-115">-InputObject</span></span>
<span data-ttu-id="ba955-116">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ba955-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba955-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ba955-117">-Name</span></span>
<span data-ttu-id="ba955-118">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ba955-118">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="ba955-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba955-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba955-120">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ba955-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ba955-121">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ba955-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ba955-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba955-122">-SubscriptionId</span></span>
<span data-ttu-id="ba955-123">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba955-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba955-124">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="ba955-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba955-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba955-125">-Tag</span></span>
<span data-ttu-id="ba955-126">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ba955-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="ba955-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba955-127">-Confirm</span></span>
<span data-ttu-id="ba955-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba955-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba955-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba955-129">-WhatIf</span></span>
<span data-ttu-id="ba955-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba955-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba955-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba955-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba955-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba955-132">CommonParameters</span></span>
<span data-ttu-id="ba955-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba955-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba955-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba955-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba955-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba955-135">INPUTS</span></span>

### <span data-ttu-id="ba955-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="ba955-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="ba955-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba955-137">OUTPUTS</span></span>

### <span data-ttu-id="ba955-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="ba955-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="ba955-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba955-139">NOTES</span></span>

<span data-ttu-id="ba955-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ba955-140">ALIASES</span></span>

<span data-ttu-id="ba955-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ba955-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba955-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ba955-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba955-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba955-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba955-144">INPUTOBJECT <ICommunicationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="ba955-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba955-145">`[CommunicationServiceName <String>]`: Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ba955-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="ba955-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ba955-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba955-147">`[Location <String>]`: Die Azure-Region</span><span class="sxs-lookup"><span data-stu-id="ba955-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="ba955-148">`[OperationId <String>]`: Die ID eines laufenden asynchronen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ba955-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="ba955-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ba955-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ba955-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ba955-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ba955-151">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba955-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ba955-152">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="ba955-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba955-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba955-153">RELATED LINKS</span></span>

