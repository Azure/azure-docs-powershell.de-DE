---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c2604531014283b3599adb94c4a12d70761e1533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297004"
---
# <span data-ttu-id="01f88-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="01f88-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="01f88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01f88-102">SYNOPSIS</span></span>
<span data-ttu-id="01f88-103">Entfernen einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="01f88-103">Remove an application.</span></span>

## <span data-ttu-id="01f88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f88-104">SYNTAX</span></span>

### <span data-ttu-id="01f88-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="01f88-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01f88-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01f88-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01f88-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01f88-107">DESCRIPTION</span></span>
<span data-ttu-id="01f88-108">Entfernen einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="01f88-108">Remove an application.</span></span>

## <span data-ttu-id="01f88-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01f88-109">EXAMPLES</span></span>

### <span data-ttu-id="01f88-110">Beispiel 1: Löschen einer virtuellen Windows-Desktop Anwendung nach Namen</span><span class="sxs-lookup"><span data-stu-id="01f88-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="01f88-111">Dieser Befehl löscht eine virtuelle Windows-Desktop Anwendung in einer Applicaton-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="01f88-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="01f88-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f88-112">PARAMETERS</span></span>

### <span data-ttu-id="01f88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f88-113">-DefaultProfile</span></span>
<span data-ttu-id="01f88-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01f88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01f88-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="01f88-115">-GroupName</span></span>
<span data-ttu-id="01f88-116">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="01f88-116">The name of the application group</span></span>

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

### <span data-ttu-id="01f88-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="01f88-117">-InputObject</span></span>
<span data-ttu-id="01f88-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="01f88-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="01f88-119">-Name</span><span class="sxs-lookup"><span data-stu-id="01f88-119">-Name</span></span>
<span data-ttu-id="01f88-120">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="01f88-120">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="01f88-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01f88-121">-PassThru</span></span>
<span data-ttu-id="01f88-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="01f88-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="01f88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f88-123">-ResourceGroupName</span></span>
<span data-ttu-id="01f88-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01f88-124">The name of the resource group.</span></span>
<span data-ttu-id="01f88-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="01f88-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="01f88-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="01f88-126">-SubscriptionId</span></span>
<span data-ttu-id="01f88-127">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="01f88-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="01f88-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01f88-128">-Confirm</span></span>
<span data-ttu-id="01f88-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01f88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f88-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f88-130">-WhatIf</span></span>
<span data-ttu-id="01f88-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01f88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f88-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01f88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f88-133">CommonParameters</span></span>
<span data-ttu-id="01f88-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f88-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01f88-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f88-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01f88-136">INPUTS</span></span>

### <span data-ttu-id="01f88-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="01f88-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="01f88-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01f88-138">OUTPUTS</span></span>

### <span data-ttu-id="01f88-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01f88-139">System.Boolean</span></span>

## <span data-ttu-id="01f88-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="01f88-140">NOTES</span></span>

<span data-ttu-id="01f88-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="01f88-141">ALIASES</span></span>

<span data-ttu-id="01f88-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01f88-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01f88-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01f88-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01f88-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="01f88-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01f88-145">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="01f88-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01f88-146">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="01f88-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="01f88-147">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="01f88-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="01f88-148">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="01f88-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="01f88-149">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="01f88-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="01f88-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="01f88-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01f88-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01f88-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="01f88-152">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="01f88-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="01f88-153">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="01f88-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="01f88-154">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="01f88-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="01f88-155">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="01f88-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="01f88-156">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="01f88-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="01f88-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01f88-157">RELATED LINKS</span></span>

