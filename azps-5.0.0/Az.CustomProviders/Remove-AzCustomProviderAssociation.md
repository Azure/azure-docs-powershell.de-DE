---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298923"
---
# <span data-ttu-id="7e047-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="7e047-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="7e047-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e047-102">SYNOPSIS</span></span>
<span data-ttu-id="7e047-103">Löschen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7e047-103">Delete an association.</span></span>

## <span data-ttu-id="7e047-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e047-104">SYNTAX</span></span>

### <span data-ttu-id="7e047-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e047-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7e047-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7e047-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e047-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e047-107">DESCRIPTION</span></span>
<span data-ttu-id="7e047-108">Löschen einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7e047-108">Delete an association.</span></span>

## <span data-ttu-id="7e047-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e047-109">EXAMPLES</span></span>

### <span data-ttu-id="7e047-110">Beispiel 1: Entfernen einer benutzerdefinierten Anbieter Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7e047-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="7e047-111">Entfernen einer benutzerdefinierten Anbieter Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7e047-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="7e047-112">Beispiel 2: Entfernen einer benutzerdefinierten Anbieter Zuordnung mit Piping</span><span class="sxs-lookup"><span data-stu-id="7e047-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="7e047-113">Entfernen Sie eine benutzerdefinierte Anbieter Zuordnung mithilfe von Piping und der passthru-Funktion, um Erfolg oder Misserfolg anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7e047-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="7e047-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e047-114">PARAMETERS</span></span>

### <span data-ttu-id="7e047-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e047-115">-AsJob</span></span>
<span data-ttu-id="7e047-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7e047-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7e047-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e047-117">-DefaultProfile</span></span>
<span data-ttu-id="7e047-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e047-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e047-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e047-119">-InputObject</span></span>
<span data-ttu-id="7e047-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7e047-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7e047-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e047-121">-Name</span></span>
<span data-ttu-id="7e047-122">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="7e047-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e047-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7e047-123">-NoWait</span></span>
<span data-ttu-id="7e047-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7e047-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7e047-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e047-125">-PassThru</span></span>
<span data-ttu-id="7e047-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="7e047-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7e047-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="7e047-127">-Scope</span></span>
<span data-ttu-id="7e047-128">Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="7e047-128">The scope of the association.</span></span>

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

### <span data-ttu-id="7e047-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e047-129">-Confirm</span></span>
<span data-ttu-id="7e047-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e047-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e047-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e047-131">-WhatIf</span></span>
<span data-ttu-id="7e047-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e047-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e047-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e047-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e047-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e047-134">CommonParameters</span></span>
<span data-ttu-id="7e047-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e047-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e047-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e047-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e047-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e047-137">INPUTS</span></span>

### <span data-ttu-id="7e047-138">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="7e047-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="7e047-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e047-139">OUTPUTS</span></span>

### <span data-ttu-id="7e047-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e047-140">System.Boolean</span></span>

## <span data-ttu-id="7e047-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e047-141">NOTES</span></span>

<span data-ttu-id="7e047-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="7e047-142">ALIASES</span></span>

<span data-ttu-id="7e047-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e047-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e047-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e047-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e047-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7e047-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e047-146">Inputobject <ICustomProvidersIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7e047-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7e047-147">`[AssociationName <String>]`: Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="7e047-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="7e047-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7e047-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7e047-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e047-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7e047-150">`[ResourceProviderName <String>]`: Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="7e047-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="7e047-151">`[Scope <String>]`: Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="7e047-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="7e047-152">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7e047-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7e047-153">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="7e047-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7e047-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e047-154">RELATED LINKS</span></span>

