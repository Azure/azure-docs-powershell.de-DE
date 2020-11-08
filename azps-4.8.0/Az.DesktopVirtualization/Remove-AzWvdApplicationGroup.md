---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 6c885f4962734bf1034256843258f4755a9b3b44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175213"
---
# <span data-ttu-id="066ef-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="066ef-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="066ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="066ef-102">SYNOPSIS</span></span>
<span data-ttu-id="066ef-103">Entfernen Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="066ef-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="066ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="066ef-104">SYNTAX</span></span>

### <span data-ttu-id="066ef-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="066ef-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="066ef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="066ef-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="066ef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="066ef-107">DESCRIPTION</span></span>
<span data-ttu-id="066ef-108">Entfernen Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="066ef-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="066ef-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="066ef-109">EXAMPLES</span></span>

### <span data-ttu-id="066ef-110">Beispiel 1: Löschen eines Windows-virtuellen Desktops mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="066ef-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="066ef-111">Mit diesem Befehl wird eine Windows Virtual Desktop-Anwendungsgruppe in einer Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="066ef-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="066ef-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="066ef-112">PARAMETERS</span></span>

### <span data-ttu-id="066ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066ef-113">-DefaultProfile</span></span>
<span data-ttu-id="066ef-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="066ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="066ef-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="066ef-115">-InputObject</span></span>
<span data-ttu-id="066ef-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="066ef-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="066ef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="066ef-117">-Name</span></span>
<span data-ttu-id="066ef-118">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="066ef-118">The name of the application group</span></span>

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

### <span data-ttu-id="066ef-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="066ef-119">-PassThru</span></span>
<span data-ttu-id="066ef-120">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="066ef-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="066ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="066ef-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="066ef-122">The name of the resource group.</span></span>
<span data-ttu-id="066ef-123">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="066ef-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="066ef-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="066ef-124">-SubscriptionId</span></span>
<span data-ttu-id="066ef-125">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="066ef-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="066ef-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="066ef-126">-Confirm</span></span>
<span data-ttu-id="066ef-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="066ef-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066ef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066ef-128">-WhatIf</span></span>
<span data-ttu-id="066ef-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="066ef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="066ef-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="066ef-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066ef-131">CommonParameters</span></span>
<span data-ttu-id="066ef-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066ef-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="066ef-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066ef-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="066ef-134">INPUTS</span></span>

### <span data-ttu-id="066ef-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="066ef-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="066ef-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="066ef-136">OUTPUTS</span></span>

### <span data-ttu-id="066ef-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="066ef-137">System.Boolean</span></span>

## <span data-ttu-id="066ef-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="066ef-138">NOTES</span></span>

<span data-ttu-id="066ef-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="066ef-139">ALIASES</span></span>

<span data-ttu-id="066ef-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="066ef-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="066ef-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="066ef-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="066ef-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="066ef-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="066ef-143">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="066ef-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="066ef-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="066ef-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="066ef-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="066ef-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="066ef-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="066ef-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="066ef-147">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="066ef-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="066ef-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="066ef-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="066ef-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="066ef-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="066ef-150">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="066ef-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="066ef-151">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="066ef-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="066ef-152">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="066ef-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="066ef-153">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="066ef-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="066ef-154">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="066ef-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="066ef-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="066ef-155">RELATED LINKS</span></span>

