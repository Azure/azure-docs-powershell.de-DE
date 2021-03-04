---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 1976c5750b5372cedce8ccf237fe8a444fa1feee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925619"
---
# <span data-ttu-id="aa6cf-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="aa6cf-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="aa6cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6cf-103">Senden sie eine Nachricht an einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-103">Send a message to a user.</span></span>

## <span data-ttu-id="aa6cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa6cf-104">SYNTAX</span></span>

### <span data-ttu-id="aa6cf-105">SendExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa6cf-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa6cf-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aa6cf-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa6cf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa6cf-107">DESCRIPTION</span></span>
<span data-ttu-id="aa6cf-108">Senden sie eine Nachricht an einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-108">Send a message to a user.</span></span>

## <span data-ttu-id="aa6cf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa6cf-109">EXAMPLES</span></span>

### <span data-ttu-id="aa6cf-110">Beispiel 1: Senden einer Nachricht an UserSession</span><span class="sxs-lookup"><span data-stu-id="aa6cf-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="aa6cf-111">Dieser Befehl sendet eine Nachricht an eine UserSession.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="aa6cf-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa6cf-112">PARAMETERS</span></span>

### <span data-ttu-id="aa6cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6cf-113">-DefaultProfile</span></span>
<span data-ttu-id="aa6cf-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa6cf-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="aa6cf-115">-HostPoolName</span></span>
<span data-ttu-id="aa6cf-116">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aa6cf-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="aa6cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa6cf-117">-InputObject</span></span>
<span data-ttu-id="aa6cf-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa6cf-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="aa6cf-119">-MessageBody</span></span>
<span data-ttu-id="aa6cf-120">Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-120">Body of message.</span></span>

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

### <span data-ttu-id="aa6cf-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="aa6cf-121">-MessageTitle</span></span>
<span data-ttu-id="aa6cf-122">Titel der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-122">Title of message.</span></span>

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

### <span data-ttu-id="aa6cf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa6cf-123">-PassThru</span></span>
<span data-ttu-id="aa6cf-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aa6cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa6cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa6cf-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-126">The name of the resource group.</span></span>
<span data-ttu-id="aa6cf-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aa6cf-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="aa6cf-128">-SessionHostName</span></span>
<span data-ttu-id="aa6cf-129">Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="aa6cf-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="aa6cf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa6cf-130">-SubscriptionId</span></span>
<span data-ttu-id="aa6cf-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aa6cf-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="aa6cf-132">-UserSessionId</span></span>
<span data-ttu-id="aa6cf-133">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="aa6cf-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="aa6cf-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa6cf-134">-Confirm</span></span>
<span data-ttu-id="aa6cf-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa6cf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa6cf-136">-WhatIf</span></span>
<span data-ttu-id="aa6cf-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa6cf-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa6cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6cf-139">CommonParameters</span></span>
<span data-ttu-id="aa6cf-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6cf-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa6cf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6cf-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa6cf-142">INPUTS</span></span>

### <span data-ttu-id="aa6cf-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="aa6cf-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="aa6cf-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa6cf-144">OUTPUTS</span></span>

### <span data-ttu-id="aa6cf-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa6cf-145">System.Boolean</span></span>

## <span data-ttu-id="aa6cf-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aa6cf-146">NOTES</span></span>

<span data-ttu-id="aa6cf-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="aa6cf-147">ALIASES</span></span>

<span data-ttu-id="aa6cf-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="aa6cf-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa6cf-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa6cf-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa6cf-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="aa6cf-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa6cf-152">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="aa6cf-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="aa6cf-153">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="aa6cf-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="aa6cf-154">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="aa6cf-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="aa6cf-155">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aa6cf-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="aa6cf-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="aa6cf-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa6cf-157">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="aa6cf-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="aa6cf-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aa6cf-159">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="aa6cf-160">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="aa6cf-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="aa6cf-161">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="aa6cf-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="aa6cf-162">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="aa6cf-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="aa6cf-163">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="aa6cf-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="aa6cf-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aa6cf-164">RELATED LINKS</span></span>

