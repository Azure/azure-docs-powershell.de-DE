---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008521"
---
# <span data-ttu-id="953f8-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="953f8-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="953f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="953f8-102">SYNOPSIS</span></span>
<span data-ttu-id="953f8-103">Senden Sie eine Nachricht an einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="953f8-103">Send a message to a user.</span></span>

## <span data-ttu-id="953f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="953f8-104">SYNTAX</span></span>

### <span data-ttu-id="953f8-105">SendExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="953f8-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="953f8-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="953f8-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="953f8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="953f8-107">DESCRIPTION</span></span>
<span data-ttu-id="953f8-108">Senden Sie eine Nachricht an einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="953f8-108">Send a message to a user.</span></span>

## <span data-ttu-id="953f8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="953f8-109">EXAMPLES</span></span>

### <span data-ttu-id="953f8-110">Beispiel 1: Senden einer Nachricht an UserSession</span><span class="sxs-lookup"><span data-stu-id="953f8-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="953f8-111">Dieser Befehl sendet eine Nachricht an eine UserSession.</span><span class="sxs-lookup"><span data-stu-id="953f8-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="953f8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="953f8-112">PARAMETERS</span></span>

### <span data-ttu-id="953f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953f8-113">-DefaultProfile</span></span>
<span data-ttu-id="953f8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="953f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="953f8-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="953f8-115">-HostPoolName</span></span>
<span data-ttu-id="953f8-116">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="953f8-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="953f8-117">-InputObject</span></span>
<span data-ttu-id="953f8-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="953f8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="953f8-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="953f8-119">-MessageBody</span></span>
<span data-ttu-id="953f8-120">Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="953f8-120">Body of message.</span></span>

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

### <span data-ttu-id="953f8-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="953f8-121">-MessageTitle</span></span>
<span data-ttu-id="953f8-122">Titel der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="953f8-122">Title of message.</span></span>

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

### <span data-ttu-id="953f8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="953f8-123">-PassThru</span></span>
<span data-ttu-id="953f8-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="953f8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="953f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="953f8-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="953f8-126">The name of the resource group.</span></span>
<span data-ttu-id="953f8-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="953f8-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f8-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="953f8-128">-SessionHostName</span></span>
<span data-ttu-id="953f8-129">Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="953f8-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f8-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="953f8-130">-SubscriptionId</span></span>
<span data-ttu-id="953f8-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="953f8-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f8-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="953f8-132">-UserSessionId</span></span>
<span data-ttu-id="953f8-133">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="953f8-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f8-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="953f8-134">-Confirm</span></span>
<span data-ttu-id="953f8-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="953f8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953f8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953f8-136">-WhatIf</span></span>
<span data-ttu-id="953f8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="953f8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953f8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="953f8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="953f8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953f8-139">CommonParameters</span></span>
<span data-ttu-id="953f8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953f8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953f8-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="953f8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953f8-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="953f8-142">INPUTS</span></span>

### <span data-ttu-id="953f8-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="953f8-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="953f8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="953f8-144">OUTPUTS</span></span>

### <span data-ttu-id="953f8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="953f8-145">System.Boolean</span></span>

## <span data-ttu-id="953f8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="953f8-146">NOTES</span></span>

<span data-ttu-id="953f8-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="953f8-147">ALIASES</span></span>

<span data-ttu-id="953f8-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="953f8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="953f8-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="953f8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="953f8-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="953f8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="953f8-151">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="953f8-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="953f8-152">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="953f8-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="953f8-153">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="953f8-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="953f8-154">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="953f8-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="953f8-155">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="953f8-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="953f8-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="953f8-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="953f8-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="953f8-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="953f8-158">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="953f8-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="953f8-159">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="953f8-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="953f8-160">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="953f8-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="953f8-161">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="953f8-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="953f8-162">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="953f8-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="953f8-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="953f8-163">RELATED LINKS</span></span>

