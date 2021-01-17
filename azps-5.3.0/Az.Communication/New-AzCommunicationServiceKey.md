---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470958"
---
# <span data-ttu-id="d85f7-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="d85f7-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="d85f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d85f7-103">Enerieren Sie den Access Key für CommunicationService erneut.</span><span class="sxs-lookup"><span data-stu-id="d85f7-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="d85f7-104">PrimaryKey und SecondaryKey können nicht gleichzeitig neu generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d85f7-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="d85f7-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d85f7-105">SYNTAX</span></span>

### <span data-ttu-id="d85f7-106">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d85f7-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d85f7-107">Regenerieren</span><span class="sxs-lookup"><span data-stu-id="d85f7-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d85f7-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d85f7-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d85f7-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d85f7-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d85f7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d85f7-110">DESCRIPTION</span></span>
<span data-ttu-id="d85f7-111">Enerieren Sie den Access Key für CommunicationService erneut.</span><span class="sxs-lookup"><span data-stu-id="d85f7-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="d85f7-112">PrimaryKey und SecondaryKey können nicht gleichzeitig neu generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d85f7-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="d85f7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d85f7-113">EXAMPLES</span></span>

### <span data-ttu-id="d85f7-114">Beispiel 1: Generiert den Primärschlüssel mithilfe einer IRegenerateKeyParameters-Hashtable erneut.</span><span class="sxs-lookup"><span data-stu-id="d85f7-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="d85f7-115">Er kann den vorherigen Primärschlüssel ungültig machen, einen neuen Primärschlüssel erneut generiert und zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d85f7-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="d85f7-116">Beispiel 2: Neuinteratieren des sekundären Schlüssels mit einem KeyType</span><span class="sxs-lookup"><span data-stu-id="d85f7-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="d85f7-117">Er kann den vorherigen sekundären Schlüssel ungültig machen, einen neuen Schlüssel erneut generiert und zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d85f7-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="d85f7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d85f7-118">PARAMETERS</span></span>

### <span data-ttu-id="d85f7-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="d85f7-119">-CommunicationServiceName</span></span>
<span data-ttu-id="d85f7-120">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d85f7-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85f7-121">-DefaultProfile</span></span>
<span data-ttu-id="d85f7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d85f7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d85f7-123">-InputObject</span></span>
<span data-ttu-id="d85f7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d85f7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d85f7-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d85f7-125">-KeyType</span></span>
<span data-ttu-id="d85f7-126">Der keyType, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d85f7-126">The keyType to regenerate.</span></span>
<span data-ttu-id="d85f7-127">Muss entweder "primär" oder "sekundär" sein (groß-/kleinschreibung wird nicht beachtet).</span><span class="sxs-lookup"><span data-stu-id="d85f7-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85f7-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d85f7-128">-Parameter</span></span>
<span data-ttu-id="d85f7-129">Parameter beschreiben die Anforderung zum erneuten Generieren von Zugriffstasten zum Erstellen. Informationen zu #A0 und zum Erstellen einer Hashtabelle finden Sie im Abschnitt NOTES.</span><span class="sxs-lookup"><span data-stu-id="d85f7-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d85f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="d85f7-131">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d85f7-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d85f7-132">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d85f7-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85f7-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d85f7-133">-SubscriptionId</span></span>
<span data-ttu-id="d85f7-134">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d85f7-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d85f7-135">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d85f7-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85f7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d85f7-136">-Confirm</span></span>
<span data-ttu-id="d85f7-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d85f7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85f7-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d85f7-138">-WhatIf</span></span>
<span data-ttu-id="d85f7-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d85f7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85f7-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d85f7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85f7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85f7-141">CommonParameters</span></span>
<span data-ttu-id="d85f7-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85f7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85f7-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d85f7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85f7-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d85f7-144">INPUTS</span></span>

### <span data-ttu-id="d85f7-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="d85f7-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="d85f7-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="d85f7-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="d85f7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d85f7-147">OUTPUTS</span></span>

### <span data-ttu-id="d85f7-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d85f7-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="d85f7-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d85f7-149">NOTES</span></span>

<span data-ttu-id="d85f7-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d85f7-150">ALIASES</span></span>

<span data-ttu-id="d85f7-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d85f7-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d85f7-152">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d85f7-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d85f7-153">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d85f7-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d85f7-154">INPUTOBJECT <ICommunicationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d85f7-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d85f7-155">`[CommunicationServiceName <String>]`: Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d85f7-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="d85f7-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d85f7-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d85f7-157">`[Location <String>]`: Die Region Azure</span><span class="sxs-lookup"><span data-stu-id="d85f7-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="d85f7-158">`[OperationId <String>]`: Die ID eines laufenden asynchronen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d85f7-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="d85f7-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d85f7-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d85f7-160">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d85f7-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d85f7-161">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d85f7-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d85f7-162">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="d85f7-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d85f7-163">PARAMETER: <IRegenerateKeyParameters> Parameter beschreiben die Anforderung zum erneuten Generieren von Zugriffstasten.</span><span class="sxs-lookup"><span data-stu-id="d85f7-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="d85f7-164">`[KeyType <KeyType?>]`: Der keyType, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d85f7-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="d85f7-165">Muss entweder "primär" oder "sekundär" sein (Groß-/Kleinschreibung wird nicht beachtet).</span><span class="sxs-lookup"><span data-stu-id="d85f7-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="d85f7-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d85f7-166">RELATED LINKS</span></span>

