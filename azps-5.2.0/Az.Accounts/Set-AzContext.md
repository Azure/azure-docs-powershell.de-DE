---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: f7d6c1fcfe4a74601a8a27e85bd1520912b26350
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293464"
---
# <span data-ttu-id="7ef8b-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="7ef8b-101">Set-AzContext</span></span>

## <span data-ttu-id="7ef8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ef8b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef8b-103">Legt den Mandanten, das Abonnement und die Umgebung für Cmdlets fest, die in der aktuellen Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="7ef8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ef8b-104">SYNTAX</span></span>

### <span data-ttu-id="7ef8b-105">Kontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ef8b-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ef8b-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="7ef8b-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ef8b-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="7ef8b-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ef8b-108">Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ef8b-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ef8b-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="7ef8b-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ef8b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ef8b-110">DESCRIPTION</span></span>
<span data-ttu-id="7ef8b-111">Das Set-AzContext A0 legt Authentifizierungsinformationen für Cmdlets fest, die Sie in der aktuellen Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="7ef8b-112">Der Kontext enthält Mandanten-, Abonnement- und Umgebungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="7ef8b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ef8b-113">EXAMPLES</span></span>

### <span data-ttu-id="7ef8b-114">Beispiel 1: Festlegen des Abonnementkontexts</span><span class="sxs-lookup"><span data-stu-id="7ef8b-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="7ef8b-115">Mit diesem Befehl wird der Kontext auf die Verwendung des angegebenen Abonnements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="7ef8b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ef8b-116">PARAMETERS</span></span>

### <span data-ttu-id="7ef8b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="7ef8b-117">-Context</span></span>
<span data-ttu-id="7ef8b-118">Gibt den Kontext für die aktuelle Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef8b-119">-DefaultProfile</span></span>
<span data-ttu-id="7ef8b-120">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="7ef8b-121">-ExtendedProperty</span></span>
<span data-ttu-id="7ef8b-122">Zusätzliche Kontexteigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ef8b-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7ef8b-123">-Force</span></span>
<span data-ttu-id="7ef8b-124">Überschreiben Sie den vorhandenen Kontext, sofern vorhanden, mit demselben Namen.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="7ef8b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7ef8b-125">-Name</span></span>
<span data-ttu-id="7ef8b-126">Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="7ef8b-126">Name of the context</span></span>

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

### <span data-ttu-id="7ef8b-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="7ef8b-127">-Scope</span></span>
<span data-ttu-id="7ef8b-128">Bestimmt den Umfang der Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="7ef8b-129">-Subscription</span></span>
<span data-ttu-id="7ef8b-130">Der Name oder die ID des Abonnements, auf das der Kontext festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="7ef8b-131">Dieser Parameter verfügt über Aliase für "-SubscriptionName" und "-SubscriptionId". Aus Gründen der Übersichtlichkeit können beide Parameter anstelle von "-Subscription" verwendet werden, wenn Name bzw. ID angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="7ef8b-132">-SubscriptionObject</span></span>
<span data-ttu-id="7ef8b-133">Ein Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="7ef8b-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-134">-Mandant</span><span class="sxs-lookup"><span data-stu-id="7ef8b-134">-Tenant</span></span>
<span data-ttu-id="7ef8b-135">Name oder ID des Mandanten</span><span class="sxs-lookup"><span data-stu-id="7ef8b-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="7ef8b-136">-TenantObject</span></span>
<span data-ttu-id="7ef8b-137">Ein Mandantenobjekt</span><span class="sxs-lookup"><span data-stu-id="7ef8b-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ef8b-138">-Confirm</span></span>
<span data-ttu-id="7ef8b-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7ef8b-140">-WhatIf</span></span>
<span data-ttu-id="7ef8b-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ef8b-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef8b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef8b-143">CommonParameters</span></span>
<span data-ttu-id="7ef8b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef8b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef8b-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef8b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef8b-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ef8b-146">INPUTS</span></span>

### <span data-ttu-id="7ef8b-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7ef8b-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="7ef8b-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="7ef8b-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="7ef8b-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7ef8b-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="7ef8b-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ef8b-150">OUTPUTS</span></span>

### <span data-ttu-id="7ef8b-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7ef8b-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="7ef8b-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ef8b-152">NOTES</span></span>

## <span data-ttu-id="7ef8b-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ef8b-153">RELATED LINKS</span></span>

[<span data-ttu-id="7ef8b-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="7ef8b-154">Get-AzContext</span></span>](./Get-AzContext.md)

