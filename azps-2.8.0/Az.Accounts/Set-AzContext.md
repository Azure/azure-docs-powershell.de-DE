---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 541306c8216168143e97bff84548e1c8e2a0ee47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658433"
---
# <span data-ttu-id="ba102-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="ba102-101">Set-AzContext</span></span>

## <span data-ttu-id="ba102-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba102-102">SYNOPSIS</span></span>
<span data-ttu-id="ba102-103">Legt den Mandanten, das Abonnement und die Umgebung für Cmdlets fest, die in der aktuellen Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba102-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="ba102-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba102-104">SYNTAX</span></span>

### <span data-ttu-id="ba102-105">Kontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba102-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba102-106">Mandantobject</span><span class="sxs-lookup"><span data-stu-id="ba102-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba102-107">Abonnementobject</span><span class="sxs-lookup"><span data-stu-id="ba102-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba102-108">Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba102-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba102-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="ba102-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba102-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba102-110">DESCRIPTION</span></span>
<span data-ttu-id="ba102-111">Das Set-AzContext-Cmdlet legt Authentifizierungsinformationen für Cmdlets fest, die Sie in der aktuellen Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba102-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="ba102-112">Der Kontext umfasst Mandanten-, Abonnement-und Umgebungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="ba102-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="ba102-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba102-113">EXAMPLES</span></span>

### <span data-ttu-id="ba102-114">Beispiel 1: Einrichten des Abonnement Kontexts</span><span class="sxs-lookup"><span data-stu-id="ba102-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="ba102-115">Mit diesem Befehl wird der Kontext für die Verwendung des angegebenen Abonnements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba102-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="ba102-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba102-116">PARAMETERS</span></span>

### <span data-ttu-id="ba102-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ba102-117">-Context</span></span>
<span data-ttu-id="ba102-118">Gibt den Kontext für die aktuelle Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="ba102-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="ba102-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba102-119">-DefaultProfile</span></span>
<span data-ttu-id="ba102-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ba102-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba102-121">-Extended</span><span class="sxs-lookup"><span data-stu-id="ba102-121">-ExtendedProperty</span></span>
<span data-ttu-id="ba102-122">Zusätzliche Kontexteigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba102-122">Additional context properties</span></span>

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

### <span data-ttu-id="ba102-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ba102-123">-Force</span></span>
<span data-ttu-id="ba102-124">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="ba102-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="ba102-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ba102-125">-Name</span></span>
<span data-ttu-id="ba102-126">Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="ba102-126">Name of the context</span></span>

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

### <span data-ttu-id="ba102-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="ba102-127">-Scope</span></span>
<span data-ttu-id="ba102-128">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="ba102-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ba102-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba102-129">-Subscription</span></span>
<span data-ttu-id="ba102-130">Der Name oder die ID des Abonnements, auf das der Kontext festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba102-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="ba102-131">Dieser Parameter verfügt über Aliase zu-subscriptionname und-Abonnement-ID, daher können Sie aus Gründen der Übersichtlichkeit eine dieser Methoden anstelle von-Subscription verwenden, wenn Sie Name und ID angeben.</span><span class="sxs-lookup"><span data-stu-id="ba102-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="ba102-132">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="ba102-132">-SubscriptionObject</span></span>
<span data-ttu-id="ba102-133">Ein Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="ba102-133">A subscription object</span></span>

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

### <span data-ttu-id="ba102-134">-Mandant</span><span class="sxs-lookup"><span data-stu-id="ba102-134">-Tenant</span></span>
<span data-ttu-id="ba102-135">Mandantenname oder-ID</span><span class="sxs-lookup"><span data-stu-id="ba102-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="ba102-136">-Mandantobject</span><span class="sxs-lookup"><span data-stu-id="ba102-136">-TenantObject</span></span>
<span data-ttu-id="ba102-137">Ein Mandanten Objekt</span><span class="sxs-lookup"><span data-stu-id="ba102-137">A Tenant Object</span></span>

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

### <span data-ttu-id="ba102-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba102-138">-Confirm</span></span>
<span data-ttu-id="ba102-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba102-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba102-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba102-140">-WhatIf</span></span>
<span data-ttu-id="ba102-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba102-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba102-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba102-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba102-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba102-143">CommonParameters</span></span>
<span data-ttu-id="ba102-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba102-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba102-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba102-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba102-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba102-146">INPUTS</span></span>

### <span data-ttu-id="ba102-147">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ba102-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="ba102-148">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ba102-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="ba102-149">Microsoft. Azure. Commands. profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ba102-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ba102-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba102-150">OUTPUTS</span></span>

### <span data-ttu-id="ba102-151">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ba102-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ba102-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba102-152">NOTES</span></span>

## <span data-ttu-id="ba102-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba102-153">RELATED LINKS</span></span>

[<span data-ttu-id="ba102-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="ba102-154">Get-AzContext</span></span>](./Get-AzContext.md)

