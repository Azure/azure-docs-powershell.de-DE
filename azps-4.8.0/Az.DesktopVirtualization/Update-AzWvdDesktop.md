---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009863"
---
# <span data-ttu-id="07ef3-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="07ef3-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="07ef3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="07ef3-103">Aktualisieren eines Desktops</span><span class="sxs-lookup"><span data-stu-id="07ef3-103">Update a desktop.</span></span>

## <span data-ttu-id="07ef3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07ef3-104">SYNTAX</span></span>

### <span data-ttu-id="07ef3-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="07ef3-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07ef3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="07ef3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="07ef3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07ef3-107">DESCRIPTION</span></span>
<span data-ttu-id="07ef3-108">Aktualisieren eines Desktops</span><span class="sxs-lookup"><span data-stu-id="07ef3-108">Update a desktop.</span></span>

## <span data-ttu-id="07ef3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07ef3-109">EXAMPLES</span></span>

### <span data-ttu-id="07ef3-110">Beispiel 1: Aktualisieren eines virtuellen Windows-Desktop Desktops</span><span class="sxs-lookup"><span data-stu-id="07ef3-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="07ef3-111">Dieser Befehl aktualisiert einen virtuellen Windows-Desktop-Desktop in einer Applicaton-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="07ef3-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="07ef3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="07ef3-112">PARAMETERS</span></span>

### <span data-ttu-id="07ef3-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="07ef3-113">-ApplicationGroupName</span></span>
<span data-ttu-id="07ef3-114">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="07ef3-114">The name of the application group</span></span>

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

### <span data-ttu-id="07ef3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ef3-115">-DefaultProfile</span></span>
<span data-ttu-id="07ef3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07ef3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ef3-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07ef3-117">-Description</span></span>
<span data-ttu-id="07ef3-118">Beschreibung des Desktops</span><span class="sxs-lookup"><span data-stu-id="07ef3-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="07ef3-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="07ef3-119">-FriendlyName</span></span>
<span data-ttu-id="07ef3-120">Anzeigename des Desktops.</span><span class="sxs-lookup"><span data-stu-id="07ef3-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="07ef3-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="07ef3-121">-InputObject</span></span>
<span data-ttu-id="07ef3-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="07ef3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="07ef3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="07ef3-123">-Name</span></span>
<span data-ttu-id="07ef3-124">Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="07ef3-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="07ef3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ef3-125">-ResourceGroupName</span></span>
<span data-ttu-id="07ef3-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07ef3-126">The name of the resource group.</span></span>
<span data-ttu-id="07ef3-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="07ef3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="07ef3-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="07ef3-128">-SubscriptionId</span></span>
<span data-ttu-id="07ef3-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="07ef3-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="07ef3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="07ef3-130">-Tag</span></span>
<span data-ttu-id="07ef3-131">Tags, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="07ef3-131">tags to be updated</span></span>

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

### <span data-ttu-id="07ef3-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07ef3-132">-Confirm</span></span>
<span data-ttu-id="07ef3-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07ef3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ef3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ef3-134">-WhatIf</span></span>
<span data-ttu-id="07ef3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07ef3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ef3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07ef3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ef3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ef3-137">CommonParameters</span></span>
<span data-ttu-id="07ef3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ef3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ef3-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07ef3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ef3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07ef3-140">INPUTS</span></span>

### <span data-ttu-id="07ef3-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="07ef3-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="07ef3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07ef3-142">OUTPUTS</span></span>

### <span data-ttu-id="07ef3-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="07ef3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="07ef3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="07ef3-144">NOTES</span></span>

<span data-ttu-id="07ef3-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="07ef3-145">ALIASES</span></span>

<span data-ttu-id="07ef3-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07ef3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07ef3-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07ef3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07ef3-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="07ef3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07ef3-149">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="07ef3-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07ef3-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="07ef3-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="07ef3-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="07ef3-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="07ef3-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="07ef3-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="07ef3-153">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="07ef3-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="07ef3-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="07ef3-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07ef3-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07ef3-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="07ef3-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="07ef3-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="07ef3-157">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="07ef3-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="07ef3-158">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="07ef3-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="07ef3-159">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="07ef3-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="07ef3-160">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="07ef3-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="07ef3-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07ef3-161">RELATED LINKS</span></span>

