---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173003"
---
# <span data-ttu-id="cf832-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="cf832-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="cf832-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf832-102">SYNOPSIS</span></span>
<span data-ttu-id="cf832-103">Trennen eines userSession</span><span class="sxs-lookup"><span data-stu-id="cf832-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="cf832-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf832-104">SYNTAX</span></span>

### <span data-ttu-id="cf832-105">Trennen (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf832-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf832-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf832-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf832-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf832-107">DESCRIPTION</span></span>
<span data-ttu-id="cf832-108">Trennen eines userSession</span><span class="sxs-lookup"><span data-stu-id="cf832-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="cf832-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf832-109">EXAMPLES</span></span>

### <span data-ttu-id="cf832-110">Beispiel 1: Trennen einer Windows Virtual Desktop-UserSession nach Namen</span><span class="sxs-lookup"><span data-stu-id="cf832-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="cf832-111">Dieser Befehl trennt die Verbindung mit einem Windows Virtual Desktop-UserSession in einem Sitzungs Host.</span><span class="sxs-lookup"><span data-stu-id="cf832-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="cf832-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf832-112">PARAMETERS</span></span>

### <span data-ttu-id="cf832-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf832-113">-DefaultProfile</span></span>
<span data-ttu-id="cf832-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf832-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf832-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="cf832-115">-HostPoolName</span></span>
<span data-ttu-id="cf832-116">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf832-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf832-117">-ID</span><span class="sxs-lookup"><span data-stu-id="cf832-117">-Id</span></span>
<span data-ttu-id="cf832-118">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="cf832-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf832-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf832-119">-InputObject</span></span>
<span data-ttu-id="cf832-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cf832-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf832-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf832-121">-PassThru</span></span>
<span data-ttu-id="cf832-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="cf832-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cf832-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf832-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf832-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf832-124">The name of the resource group.</span></span>
<span data-ttu-id="cf832-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="cf832-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf832-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="cf832-126">-SessionHostName</span></span>
<span data-ttu-id="cf832-127">Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="cf832-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf832-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="cf832-128">-SubscriptionId</span></span>
<span data-ttu-id="cf832-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cf832-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf832-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf832-130">-Confirm</span></span>
<span data-ttu-id="cf832-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf832-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf832-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf832-132">-WhatIf</span></span>
<span data-ttu-id="cf832-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf832-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf832-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf832-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf832-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf832-135">CommonParameters</span></span>
<span data-ttu-id="cf832-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf832-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf832-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf832-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf832-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf832-138">INPUTS</span></span>

### <span data-ttu-id="cf832-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cf832-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cf832-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf832-140">OUTPUTS</span></span>

### <span data-ttu-id="cf832-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf832-141">System.Boolean</span></span>

## <span data-ttu-id="cf832-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf832-142">NOTES</span></span>

<span data-ttu-id="cf832-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="cf832-143">ALIASES</span></span>

<span data-ttu-id="cf832-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf832-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf832-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf832-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf832-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="cf832-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf832-147">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="cf832-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf832-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf832-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cf832-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf832-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cf832-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="cf832-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cf832-151">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cf832-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cf832-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="cf832-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf832-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf832-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cf832-154">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="cf832-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="cf832-155">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="cf832-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cf832-156">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cf832-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cf832-157">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="cf832-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cf832-158">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cf832-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cf832-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf832-159">RELATED LINKS</span></span>

