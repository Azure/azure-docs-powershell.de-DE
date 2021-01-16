---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c65fd55599a78bbaa558ba7ec8efa94fdc3b40e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296981"
---
# <span data-ttu-id="0570c-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="0570c-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="0570c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0570c-102">SYNOPSIS</span></span>
<span data-ttu-id="0570c-103">Entfernen sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0570c-103">Remove an application.</span></span>

## <span data-ttu-id="0570c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0570c-104">SYNTAX</span></span>

### <span data-ttu-id="0570c-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="0570c-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0570c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0570c-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0570c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0570c-107">DESCRIPTION</span></span>
<span data-ttu-id="0570c-108">Entfernen Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0570c-108">Remove an application.</span></span>

## <span data-ttu-id="0570c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0570c-109">EXAMPLES</span></span>

### <span data-ttu-id="0570c-110">Beispiel 1: Löschen einer virtuellen Windows-Desktopanwendung nach Name</span><span class="sxs-lookup"><span data-stu-id="0570c-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="0570c-111">Mit diesem Befehl wird eine virtuelle Windows-Desktopanwendung in einer Anwendungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0570c-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="0570c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0570c-112">PARAMETERS</span></span>

### <span data-ttu-id="0570c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0570c-113">-DefaultProfile</span></span>
<span data-ttu-id="0570c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0570c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0570c-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="0570c-115">-GroupName</span></span>
<span data-ttu-id="0570c-116">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0570c-116">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0570c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0570c-117">-InputObject</span></span>
<span data-ttu-id="0570c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0570c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0570c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0570c-119">-Name</span></span>
<span data-ttu-id="0570c-120">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0570c-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0570c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0570c-121">-PassThru</span></span>
<span data-ttu-id="0570c-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0570c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0570c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0570c-123">-ResourceGroupName</span></span>
<span data-ttu-id="0570c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0570c-124">The name of the resource group.</span></span>
<span data-ttu-id="0570c-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0570c-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0570c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0570c-126">-SubscriptionId</span></span>
<span data-ttu-id="0570c-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0570c-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0570c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0570c-128">-Confirm</span></span>
<span data-ttu-id="0570c-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0570c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0570c-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0570c-130">-WhatIf</span></span>
<span data-ttu-id="0570c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0570c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0570c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0570c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0570c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0570c-133">CommonParameters</span></span>
<span data-ttu-id="0570c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0570c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0570c-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0570c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0570c-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0570c-136">INPUTS</span></span>

### <span data-ttu-id="0570c-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0570c-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0570c-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0570c-138">OUTPUTS</span></span>

### <span data-ttu-id="0570c-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0570c-139">System.Boolean</span></span>

## <span data-ttu-id="0570c-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0570c-140">NOTES</span></span>

<span data-ttu-id="0570c-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0570c-141">ALIASES</span></span>

<span data-ttu-id="0570c-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0570c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0570c-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0570c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0570c-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0570c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0570c-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0570c-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0570c-146">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0570c-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0570c-147">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0570c-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0570c-148">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="0570c-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0570c-149">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0570c-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0570c-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0570c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0570c-151">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="0570c-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0570c-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0570c-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0570c-153">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0570c-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="0570c-154">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="0570c-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0570c-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0570c-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0570c-156">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="0570c-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0570c-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0570c-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0570c-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0570c-158">RELATED LINKS</span></span>

