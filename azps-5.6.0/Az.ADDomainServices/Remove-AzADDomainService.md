---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: 68631f106b795f42fa8ead1a6379ff9dbaa0f4ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934504"
---
# <span data-ttu-id="cb8a7-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="cb8a7-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="cb8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8a7-103">Der Vorgang "Domänendienst löschen" löscht einen vorhandenen Domänendienst.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="cb8a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb8a7-104">SYNTAX</span></span>

### <span data-ttu-id="cb8a7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb8a7-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb8a7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb8a7-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb8a7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb8a7-107">DESCRIPTION</span></span>
<span data-ttu-id="cb8a7-108">Der Vorgang "Domänendienst löschen" löscht einen vorhandenen Domänendienst.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="cb8a7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb8a7-109">EXAMPLES</span></span>

### <span data-ttu-id="cb8a7-110">Beispiel 1: Löschen der AzADDomain nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="cb8a7-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="cb8a7-111">Löschen der AzADDomain nach ResourceGroupName und Name</span><span class="sxs-lookup"><span data-stu-id="cb8a7-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="cb8a7-112">Beispiel 2: Löschen der AzADDomain nach InputObject</span><span class="sxs-lookup"><span data-stu-id="cb8a7-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="cb8a7-113">Löschen der AzADDomain von InputObject</span><span class="sxs-lookup"><span data-stu-id="cb8a7-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="cb8a7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cb8a7-114">PARAMETERS</span></span>

### <span data-ttu-id="cb8a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb8a7-115">-AsJob</span></span>
<span data-ttu-id="cb8a7-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="cb8a7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cb8a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8a7-117">-DefaultProfile</span></span>
<span data-ttu-id="cb8a7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb8a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb8a7-119">-InputObject</span></span>
<span data-ttu-id="cb8a7-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb8a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cb8a7-121">-Name</span></span>
<span data-ttu-id="cb8a7-122">Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb8a7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cb8a7-123">-NoWait</span></span>
<span data-ttu-id="cb8a7-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="cb8a7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb8a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb8a7-125">-PassThru</span></span>
<span data-ttu-id="cb8a7-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb8a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb8a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb8a7-128">Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="cb8a7-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cb8a7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb8a7-130">-SubscriptionId</span></span>
<span data-ttu-id="cb8a7-131">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb8a7-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb8a7-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb8a7-133">-Confirm</span></span>
<span data-ttu-id="cb8a7-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb8a7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb8a7-135">-WhatIf</span></span>
<span data-ttu-id="cb8a7-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb8a7-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb8a7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8a7-138">CommonParameters</span></span>
<span data-ttu-id="cb8a7-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8a7-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb8a7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8a7-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb8a7-141">INPUTS</span></span>

### <span data-ttu-id="cb8a7-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="cb8a7-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="cb8a7-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb8a7-143">OUTPUTS</span></span>

### <span data-ttu-id="cb8a7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb8a7-144">System.Boolean</span></span>

## <span data-ttu-id="cb8a7-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cb8a7-145">NOTES</span></span>

<span data-ttu-id="cb8a7-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cb8a7-146">ALIASES</span></span>

<span data-ttu-id="cb8a7-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cb8a7-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb8a7-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb8a7-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb8a7-150">INPUTOBJECT <IAdDomainServicesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="cb8a7-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb8a7-151">`[DomainServiceName <String>]`: Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="cb8a7-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cb8a7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb8a7-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="cb8a7-154">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="cb8a7-155">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cb8a7-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="cb8a7-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cb8a7-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cb8a7-157">RELATED LINKS</span></span>

