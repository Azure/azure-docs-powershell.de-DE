---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296980"
---
# <span data-ttu-id="a1ce4-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1ce4-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="a1ce4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ce4-103">Entfernen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a1ce4-103">Remove a workspace.</span></span>

## <span data-ttu-id="a1ce4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1ce4-104">SYNTAX</span></span>

### <span data-ttu-id="a1ce4-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1ce4-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1ce4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1ce4-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1ce4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="a1ce4-108">Entfernen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a1ce4-108">Remove a workspace.</span></span>

## <span data-ttu-id="a1ce4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1ce4-109">EXAMPLES</span></span>

### <span data-ttu-id="a1ce4-110">Beispiel 1: Löschen eines virtuellen Windows-Desktop-Worksapce nach Name</span><span class="sxs-lookup"><span data-stu-id="a1ce4-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="a1ce4-111">Dieser Befehl löscht einen virtuellen Windows-Desktop Arbeitsbereich in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="a1ce4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1ce4-112">PARAMETERS</span></span>

### <span data-ttu-id="a1ce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ce4-113">-DefaultProfile</span></span>
<span data-ttu-id="a1ce4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1ce4-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1ce4-115">-InputObject</span></span>
<span data-ttu-id="a1ce4-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1ce4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a1ce4-117">-Name</span></span>
<span data-ttu-id="a1ce4-118">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a1ce4-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ce4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1ce4-119">-PassThru</span></span>
<span data-ttu-id="a1ce4-120">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="a1ce4-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a1ce4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ce4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1ce4-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-122">The name of the resource group.</span></span>
<span data-ttu-id="a1ce4-123">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a1ce4-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a1ce4-124">-SubscriptionId</span></span>
<span data-ttu-id="a1ce4-125">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a1ce4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1ce4-126">-Confirm</span></span>
<span data-ttu-id="a1ce4-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1ce4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1ce4-128">-WhatIf</span></span>
<span data-ttu-id="a1ce4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1ce4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1ce4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ce4-131">CommonParameters</span></span>
<span data-ttu-id="a1ce4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ce4-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1ce4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ce4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1ce4-134">INPUTS</span></span>

### <span data-ttu-id="a1ce4-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a1ce4-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a1ce4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1ce4-136">OUTPUTS</span></span>

### <span data-ttu-id="a1ce4-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1ce4-137">System.Boolean</span></span>

## <span data-ttu-id="a1ce4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1ce4-138">NOTES</span></span>

<span data-ttu-id="a1ce4-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="a1ce4-139">ALIASES</span></span>

<span data-ttu-id="a1ce4-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1ce4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1ce4-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1ce4-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1ce4-143">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a1ce4-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1ce4-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a1ce4-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a1ce4-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a1ce4-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a1ce4-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="a1ce4-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a1ce4-147">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a1ce4-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a1ce4-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a1ce4-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1ce4-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a1ce4-150">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="a1ce4-151">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="a1ce4-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a1ce4-152">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a1ce4-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a1ce4-153">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="a1ce4-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a1ce4-154">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a1ce4-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a1ce4-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1ce4-155">RELATED LINKS</span></span>

