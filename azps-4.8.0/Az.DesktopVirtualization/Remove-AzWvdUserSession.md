---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166959"
---
# <span data-ttu-id="a7e20-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="a7e20-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="a7e20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7e20-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e20-103">Entfernen eines userSession</span><span class="sxs-lookup"><span data-stu-id="a7e20-103">Remove a userSession.</span></span>

## <span data-ttu-id="a7e20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7e20-104">SYNTAX</span></span>

### <span data-ttu-id="a7e20-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7e20-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7e20-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e20-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7e20-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7e20-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e20-108">Entfernen eines userSession</span><span class="sxs-lookup"><span data-stu-id="a7e20-108">Remove a userSession.</span></span>

## <span data-ttu-id="a7e20-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7e20-109">EXAMPLES</span></span>

### <span data-ttu-id="a7e20-110">Beispiel 1: Löschen eines virtuellen Windows-Desktop-UserSession nach Name</span><span class="sxs-lookup"><span data-stu-id="a7e20-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="a7e20-111">Dieser Befehl löscht einen virtuellen Windows-Desktop-UserSession in einem Sitzungs Host.</span><span class="sxs-lookup"><span data-stu-id="a7e20-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="a7e20-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7e20-112">PARAMETERS</span></span>

### <span data-ttu-id="a7e20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e20-113">-DefaultProfile</span></span>
<span data-ttu-id="a7e20-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7e20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7e20-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a7e20-115">-Force</span></span>
<span data-ttu-id="a7e20-116">Flag erzwingen, um sich bei userSession anzumelden.</span><span class="sxs-lookup"><span data-stu-id="a7e20-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="a7e20-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a7e20-117">-HostPoolName</span></span>
<span data-ttu-id="a7e20-118">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7e20-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a7e20-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a7e20-119">-Id</span></span>
<span data-ttu-id="a7e20-120">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="a7e20-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e20-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7e20-121">-InputObject</span></span>
<span data-ttu-id="a7e20-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a7e20-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7e20-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7e20-123">-PassThru</span></span>
<span data-ttu-id="a7e20-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="a7e20-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a7e20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e20-125">-ResourceGroupName</span></span>
<span data-ttu-id="a7e20-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7e20-126">The name of the resource group.</span></span>
<span data-ttu-id="a7e20-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a7e20-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a7e20-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="a7e20-128">-SessionHostName</span></span>
<span data-ttu-id="a7e20-129">Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="a7e20-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="a7e20-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a7e20-130">-SubscriptionId</span></span>
<span data-ttu-id="a7e20-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a7e20-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a7e20-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7e20-132">-Confirm</span></span>
<span data-ttu-id="a7e20-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7e20-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e20-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e20-134">-WhatIf</span></span>
<span data-ttu-id="a7e20-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7e20-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7e20-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e20-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e20-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e20-137">CommonParameters</span></span>
<span data-ttu-id="a7e20-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e20-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e20-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7e20-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e20-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7e20-140">INPUTS</span></span>

### <span data-ttu-id="a7e20-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e20-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a7e20-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7e20-142">OUTPUTS</span></span>

### <span data-ttu-id="a7e20-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7e20-143">System.Boolean</span></span>

## <span data-ttu-id="a7e20-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7e20-144">NOTES</span></span>

<span data-ttu-id="a7e20-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="a7e20-145">ALIASES</span></span>

<span data-ttu-id="a7e20-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7e20-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7e20-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a7e20-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7e20-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a7e20-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7e20-149">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a7e20-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7e20-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a7e20-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a7e20-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a7e20-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a7e20-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="a7e20-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a7e20-153">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a7e20-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a7e20-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a7e20-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7e20-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7e20-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a7e20-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a7e20-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a7e20-157">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="a7e20-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a7e20-158">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a7e20-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a7e20-159">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="a7e20-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a7e20-160">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a7e20-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a7e20-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7e20-161">RELATED LINKS</span></span>

