---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: fbc61ec485be94eacb0267a9698a861f962c61a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944183"
---
# <span data-ttu-id="62670-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="62670-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="62670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62670-102">SYNOPSIS</span></span>
<span data-ttu-id="62670-103">Aktualisieren eines Desktops</span><span class="sxs-lookup"><span data-stu-id="62670-103">Update a desktop.</span></span>

## <span data-ttu-id="62670-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62670-104">SYNTAX</span></span>

### <span data-ttu-id="62670-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="62670-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62670-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="62670-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="62670-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62670-107">DESCRIPTION</span></span>
<span data-ttu-id="62670-108">Aktualisieren eines Desktops</span><span class="sxs-lookup"><span data-stu-id="62670-108">Update a desktop.</span></span>

## <span data-ttu-id="62670-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62670-109">EXAMPLES</span></span>

### <span data-ttu-id="62670-110">Beispiel 1: Aktualisieren eines virtuellen Windows-Desktopdesktops</span><span class="sxs-lookup"><span data-stu-id="62670-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="62670-111">Mit diesem Befehl wird ein virtueller Windows-Desktopdesktop in einer applicaton-Gruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="62670-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="62670-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="62670-112">PARAMETERS</span></span>

### <span data-ttu-id="62670-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="62670-113">-ApplicationGroupName</span></span>
<span data-ttu-id="62670-114">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="62670-114">The name of the application group</span></span>

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

### <span data-ttu-id="62670-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62670-115">-DefaultProfile</span></span>
<span data-ttu-id="62670-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62670-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62670-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62670-117">-Description</span></span>
<span data-ttu-id="62670-118">Beschreibung des Desktops.</span><span class="sxs-lookup"><span data-stu-id="62670-118">Description of Desktop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62670-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62670-119">-FriendlyName</span></span>
<span data-ttu-id="62670-120">Anzeigename des Desktops.</span><span class="sxs-lookup"><span data-stu-id="62670-120">Friendly name of Desktop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62670-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62670-121">-InputObject</span></span>
<span data-ttu-id="62670-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="62670-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62670-123">-Name</span><span class="sxs-lookup"><span data-stu-id="62670-123">-Name</span></span>
<span data-ttu-id="62670-124">Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="62670-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62670-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62670-125">-ResourceGroupName</span></span>
<span data-ttu-id="62670-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="62670-126">The name of the resource group.</span></span>
<span data-ttu-id="62670-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="62670-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="62670-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62670-128">-SubscriptionId</span></span>
<span data-ttu-id="62670-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="62670-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="62670-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="62670-130">-Tag</span></span>
<span data-ttu-id="62670-131">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="62670-131">tags to be updated</span></span>

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

### <span data-ttu-id="62670-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62670-132">-Confirm</span></span>
<span data-ttu-id="62670-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62670-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62670-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62670-134">-WhatIf</span></span>
<span data-ttu-id="62670-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62670-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62670-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62670-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62670-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62670-137">CommonParameters</span></span>
<span data-ttu-id="62670-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62670-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62670-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62670-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62670-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62670-140">INPUTS</span></span>

### <span data-ttu-id="62670-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="62670-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="62670-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62670-142">OUTPUTS</span></span>

### <span data-ttu-id="62670-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="62670-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="62670-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="62670-144">NOTES</span></span>

<span data-ttu-id="62670-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="62670-145">ALIASES</span></span>

<span data-ttu-id="62670-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="62670-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62670-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="62670-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62670-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62670-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62670-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="62670-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62670-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="62670-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="62670-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="62670-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="62670-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="62670-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="62670-153">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="62670-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="62670-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="62670-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62670-155">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="62670-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="62670-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="62670-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="62670-157">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="62670-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="62670-158">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="62670-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="62670-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="62670-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="62670-160">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="62670-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="62670-161">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="62670-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="62670-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="62670-162">RELATED LINKS</span></span>

