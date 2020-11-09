---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 7b0cdf0cbe0aecdb2e1b6829ed1ec22b1e485e92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297003"
---
# <span data-ttu-id="94378-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="94378-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="94378-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94378-102">SYNOPSIS</span></span>
<span data-ttu-id="94378-103">Entfernen eines Host Pools</span><span class="sxs-lookup"><span data-stu-id="94378-103">Remove a host pool.</span></span>

## <span data-ttu-id="94378-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94378-104">SYNTAX</span></span>

### <span data-ttu-id="94378-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="94378-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94378-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94378-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94378-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94378-107">DESCRIPTION</span></span>
<span data-ttu-id="94378-108">Entfernen eines Host Pools</span><span class="sxs-lookup"><span data-stu-id="94378-108">Remove a host pool.</span></span>

## <span data-ttu-id="94378-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94378-109">EXAMPLES</span></span>

### <span data-ttu-id="94378-110">Beispiel 1: Löschen eines virtuellen Windows-Desktop-HostPool nach Name</span><span class="sxs-lookup"><span data-stu-id="94378-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="94378-111">Mit diesem Befehl wird ein Windows Virtual Desktop-HostPool in einer Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="94378-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="94378-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="94378-112">PARAMETERS</span></span>

### <span data-ttu-id="94378-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94378-113">-DefaultProfile</span></span>
<span data-ttu-id="94378-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94378-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94378-115">-Force</span><span class="sxs-lookup"><span data-stu-id="94378-115">-Force</span></span>
<span data-ttu-id="94378-116">Flag erzwingen, um sessionHost zu löschen.</span><span class="sxs-lookup"><span data-stu-id="94378-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="94378-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94378-117">-InputObject</span></span>
<span data-ttu-id="94378-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="94378-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94378-119">-Name</span><span class="sxs-lookup"><span data-stu-id="94378-119">-Name</span></span>
<span data-ttu-id="94378-120">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94378-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94378-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94378-121">-PassThru</span></span>
<span data-ttu-id="94378-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="94378-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94378-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94378-123">-ResourceGroupName</span></span>
<span data-ttu-id="94378-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94378-124">The name of the resource group.</span></span>
<span data-ttu-id="94378-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="94378-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="94378-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="94378-126">-SubscriptionId</span></span>
<span data-ttu-id="94378-127">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="94378-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="94378-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94378-128">-Confirm</span></span>
<span data-ttu-id="94378-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94378-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94378-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94378-130">-WhatIf</span></span>
<span data-ttu-id="94378-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94378-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94378-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94378-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94378-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94378-133">CommonParameters</span></span>
<span data-ttu-id="94378-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94378-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94378-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94378-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94378-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94378-136">INPUTS</span></span>

### <span data-ttu-id="94378-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="94378-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="94378-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94378-138">OUTPUTS</span></span>

### <span data-ttu-id="94378-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94378-139">System.Boolean</span></span>

## <span data-ttu-id="94378-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="94378-140">NOTES</span></span>

<span data-ttu-id="94378-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="94378-141">ALIASES</span></span>

<span data-ttu-id="94378-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94378-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94378-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="94378-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94378-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="94378-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94378-145">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="94378-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94378-146">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="94378-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="94378-147">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="94378-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="94378-148">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="94378-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="94378-149">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="94378-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="94378-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="94378-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94378-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94378-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="94378-152">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="94378-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="94378-153">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="94378-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="94378-154">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="94378-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="94378-155">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="94378-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="94378-156">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="94378-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="94378-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94378-157">RELATED LINKS</span></span>

