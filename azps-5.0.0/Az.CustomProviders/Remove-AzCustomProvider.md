---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298929"
---
# <span data-ttu-id="b00a4-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="b00a4-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="b00a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b00a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b00a4-103">Löscht den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="b00a4-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="b00a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b00a4-104">SYNTAX</span></span>

### <span data-ttu-id="b00a4-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b00a4-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b00a4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b00a4-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b00a4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b00a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b00a4-108">Löscht den benutzerdefinierten Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="b00a4-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="b00a4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b00a4-109">EXAMPLES</span></span>

### <span data-ttu-id="b00a4-110">Beispiel 1: Entfernen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="b00a4-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="b00a4-111">Entfernen eines benutzerdefinierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="b00a4-111">Remove a custom provider</span></span>

### <span data-ttu-id="b00a4-112">Beispiel 2: Entfernen eines benutzerdefinierten Anbieters mit passthru</span><span class="sxs-lookup"><span data-stu-id="b00a4-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="b00a4-113">Entfernen Sie einen benutzerdefinierten Anbieter, und verwenden Sie die passthru-Funktion, um Erfolg oder Misserfolg anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b00a4-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="b00a4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b00a4-114">PARAMETERS</span></span>

### <span data-ttu-id="b00a4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b00a4-115">-AsJob</span></span>
<span data-ttu-id="b00a4-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b00a4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b00a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00a4-117">-DefaultProfile</span></span>
<span data-ttu-id="b00a4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b00a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b00a4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b00a4-119">-InputObject</span></span>
<span data-ttu-id="b00a4-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b00a4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00a4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b00a4-121">-Name</span></span>
<span data-ttu-id="b00a4-122">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="b00a4-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a4-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b00a4-123">-NoWait</span></span>
<span data-ttu-id="b00a4-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b00a4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b00a4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b00a4-125">-PassThru</span></span>
<span data-ttu-id="b00a4-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="b00a4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b00a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="b00a4-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b00a4-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b00a4-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b00a4-129">-SubscriptionId</span></span>
<span data-ttu-id="b00a4-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b00a4-130">The Azure subscription ID.</span></span>
<span data-ttu-id="b00a4-131">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="b00a4-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="b00a4-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b00a4-132">-Confirm</span></span>
<span data-ttu-id="b00a4-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b00a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00a4-134">-WhatIf</span></span>
<span data-ttu-id="b00a4-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b00a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00a4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b00a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00a4-137">CommonParameters</span></span>
<span data-ttu-id="b00a4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00a4-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b00a4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00a4-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b00a4-140">INPUTS</span></span>

### <span data-ttu-id="b00a4-141">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="b00a4-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b00a4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b00a4-142">OUTPUTS</span></span>

### <span data-ttu-id="b00a4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b00a4-143">System.Boolean</span></span>

## <span data-ttu-id="b00a4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b00a4-144">NOTES</span></span>

<span data-ttu-id="b00a4-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="b00a4-145">ALIASES</span></span>

<span data-ttu-id="b00a4-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b00a4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b00a4-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b00a4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b00a4-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b00a4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b00a4-149">Inputobject <ICustomProvidersIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="b00a4-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b00a4-150">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b00a4-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b00a4-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b00a4-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b00a4-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b00a4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b00a4-153">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="b00a4-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b00a4-154">`[Scope <String>]`: Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b00a4-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b00a4-155">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b00a4-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b00a4-156">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="b00a4-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b00a4-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b00a4-157">RELATED LINKS</span></span>

