---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 42c7e2b632b175ef12f34e04ff682020d634ef74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663343"
---
# <span data-ttu-id="24482-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="24482-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="24482-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24482-102">SYNOPSIS</span></span>
<span data-ttu-id="24482-103">Legt den Mandanten, das Abonnement und die Umgebung für Cmdlets fest, die in der aktuellen Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24482-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24482-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24482-104">SYNTAX</span></span>

### <span data-ttu-id="24482-105">Kontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="24482-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24482-106">Mandantobject</span><span class="sxs-lookup"><span data-stu-id="24482-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24482-107">Abonnementobject</span><span class="sxs-lookup"><span data-stu-id="24482-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24482-108">Abonnement</span><span class="sxs-lookup"><span data-stu-id="24482-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24482-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="24482-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24482-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24482-110">DESCRIPTION</span></span>
<span data-ttu-id="24482-111">Das Set-AzureRmContext-Cmdlet legt Authentifizierungsinformationen für Cmdlets fest, die Sie in der aktuellen Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="24482-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="24482-112">Der Kontext umfasst Mandanten-, Abonnement-und Umgebungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="24482-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="24482-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24482-113">EXAMPLES</span></span>

### <span data-ttu-id="24482-114">Beispiel 1: Einrichten des Abonnement Kontexts</span><span class="sxs-lookup"><span data-stu-id="24482-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="24482-115">Mit diesem Befehl wird der Kontext für die Verwendung des angegebenen Abonnements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24482-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="24482-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="24482-116">PARAMETERS</span></span>

### <span data-ttu-id="24482-117">-Context</span><span class="sxs-lookup"><span data-stu-id="24482-117">-Context</span></span>
<span data-ttu-id="24482-118">Gibt den Kontext für die aktuelle Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="24482-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24482-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24482-119">-DefaultProfile</span></span>
<span data-ttu-id="24482-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="24482-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24482-121">-Extended</span><span class="sxs-lookup"><span data-stu-id="24482-121">-ExtendedProperty</span></span>
<span data-ttu-id="24482-122">Zusätzliche Kontexteigenschaften</span><span class="sxs-lookup"><span data-stu-id="24482-122">Additional context properties</span></span>

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

### <span data-ttu-id="24482-123">-Force</span><span class="sxs-lookup"><span data-stu-id="24482-123">-Force</span></span>
<span data-ttu-id="24482-124">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="24482-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="24482-125">-Name</span><span class="sxs-lookup"><span data-stu-id="24482-125">-Name</span></span>
<span data-ttu-id="24482-126">Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="24482-126">Name of the context</span></span>

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

### <span data-ttu-id="24482-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="24482-127">-Scope</span></span>
<span data-ttu-id="24482-128">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="24482-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="24482-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="24482-129">-Subscription</span></span>
<span data-ttu-id="24482-130">Der Name oder die ID des Abonnements, auf das der Kontext festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="24482-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="24482-131">Dieser Parameter verfügt über Aliase zu-subscriptionname und-Abonnement-ID, daher können Sie aus Gründen der Übersichtlichkeit eine dieser Methoden anstelle von-Subscription verwenden, wenn Sie Name und ID angeben.</span><span class="sxs-lookup"><span data-stu-id="24482-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="24482-132">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="24482-132">-SubscriptionObject</span></span>
<span data-ttu-id="24482-133">Ein Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="24482-133">A subscription object</span></span>

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

### <span data-ttu-id="24482-134">-Mandant</span><span class="sxs-lookup"><span data-stu-id="24482-134">-Tenant</span></span>
<span data-ttu-id="24482-135">Mandantenname oder-ID</span><span class="sxs-lookup"><span data-stu-id="24482-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="24482-136">-Mandantobject</span><span class="sxs-lookup"><span data-stu-id="24482-136">-TenantObject</span></span>
<span data-ttu-id="24482-137">Ein Mandanten Objekt</span><span class="sxs-lookup"><span data-stu-id="24482-137">A Tenant Object</span></span>

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

### <span data-ttu-id="24482-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24482-138">-Confirm</span></span>
<span data-ttu-id="24482-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24482-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24482-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24482-140">-WhatIf</span></span>
<span data-ttu-id="24482-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24482-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24482-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24482-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24482-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24482-143">CommonParameters</span></span>
<span data-ttu-id="24482-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24482-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24482-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24482-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24482-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24482-146">INPUTS</span></span>

### <span data-ttu-id="24482-147">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="24482-147">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="24482-148">Parameter: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24482-148">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="24482-149">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="24482-149">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>
<span data-ttu-id="24482-150">Parameter: tenantobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24482-150">Parameters: TenantObject (ByValue)</span></span>

### <span data-ttu-id="24482-151">Microsoft. Azure. Commands. profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="24482-151">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>
<span data-ttu-id="24482-152">Parameter: subscriptionobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24482-152">Parameters: SubscriptionObject (ByValue)</span></span>

## <span data-ttu-id="24482-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24482-153">OUTPUTS</span></span>

### <span data-ttu-id="24482-154">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="24482-154">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="24482-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="24482-155">NOTES</span></span>

## <span data-ttu-id="24482-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24482-156">RELATED LINKS</span></span>

[<span data-ttu-id="24482-157">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="24482-157">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

