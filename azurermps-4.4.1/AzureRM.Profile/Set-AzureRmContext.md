---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 99adb0cb38cd5c1e43dbd9f7dd5f81a4bef26beb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663549"
---
# <span data-ttu-id="42e5a-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="42e5a-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="42e5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="42e5a-103">Legt den Mandanten, das Abonnement und die Umgebung für Cmdlets fest, die in der aktuellen Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42e5a-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42e5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42e5a-104">SYNTAX</span></span>

### <span data-ttu-id="42e5a-105">Kontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="42e5a-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42e5a-106">Mandantobject</span><span class="sxs-lookup"><span data-stu-id="42e5a-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42e5a-107">Abonnementobject</span><span class="sxs-lookup"><span data-stu-id="42e5a-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42e5a-108">Abonnement</span><span class="sxs-lookup"><span data-stu-id="42e5a-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42e5a-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="42e5a-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42e5a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42e5a-110">DESCRIPTION</span></span>
<span data-ttu-id="42e5a-111">Das Set-AzureRmContext-Cmdlet legt Authentifizierungsinformationen für Cmdlets fest, die Sie in der aktuellen Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="42e5a-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="42e5a-112">Der Kontext umfasst Mandanten-, Abonnement-und Umgebungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="42e5a-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="42e5a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42e5a-113">EXAMPLES</span></span>

### <span data-ttu-id="42e5a-114">Beispiel 1: Einrichten des Abonnement Kontexts</span><span class="sxs-lookup"><span data-stu-id="42e5a-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="42e5a-115">Mit diesem Befehl wird der Kontext für die Verwendung des angegebenen Abonnements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42e5a-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="42e5a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="42e5a-116">PARAMETERS</span></span>

### <span data-ttu-id="42e5a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="42e5a-117">-Context</span></span>
<span data-ttu-id="42e5a-118">Gibt den Kontext für die aktuelle Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="42e5a-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="42e5a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e5a-119">-DefaultProfile</span></span>
<span data-ttu-id="42e5a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="42e5a-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e5a-121">-Extended</span><span class="sxs-lookup"><span data-stu-id="42e5a-121">-ExtendedProperty</span></span>
<span data-ttu-id="42e5a-122">Zusätzliche Kontexteigenschaften</span><span class="sxs-lookup"><span data-stu-id="42e5a-122">Additional context properties</span></span>

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

### <span data-ttu-id="42e5a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="42e5a-123">-Force</span></span>
<span data-ttu-id="42e5a-124">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="42e5a-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="42e5a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="42e5a-125">-Name</span></span>
<span data-ttu-id="42e5a-126">Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="42e5a-126">Name of the context</span></span>

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

### <span data-ttu-id="42e5a-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="42e5a-127">-Scope</span></span>
<span data-ttu-id="42e5a-128">Bestimmt den Bereich von Kontextänderungen, beispielsweise wheher Änderungen gelten nur für den cusrrent-Prozess oder für alle von diesem Benutzer gestarteten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="42e5a-128">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="42e5a-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="42e5a-129">-Subscription</span></span>
<span data-ttu-id="42e5a-130">Name oder ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="42e5a-130">Subscription Name or Id</span></span>

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

### <span data-ttu-id="42e5a-131">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="42e5a-131">-SubscriptionObject</span></span>
<span data-ttu-id="42e5a-132">Ein Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="42e5a-132">A subscription object</span></span>

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

### <span data-ttu-id="42e5a-133">-Mandant</span><span class="sxs-lookup"><span data-stu-id="42e5a-133">-Tenant</span></span>
<span data-ttu-id="42e5a-134">Mandantenname oder-ID</span><span class="sxs-lookup"><span data-stu-id="42e5a-134">Tenant name or ID</span></span>

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

### <span data-ttu-id="42e5a-135">-Mandantobject</span><span class="sxs-lookup"><span data-stu-id="42e5a-135">-TenantObject</span></span>
<span data-ttu-id="42e5a-136">Ein Mandanten Objekt</span><span class="sxs-lookup"><span data-stu-id="42e5a-136">A Tenant Object</span></span>

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

### <span data-ttu-id="42e5a-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42e5a-137">-Confirm</span></span>
<span data-ttu-id="42e5a-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42e5a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e5a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e5a-139">-WhatIf</span></span>
<span data-ttu-id="42e5a-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42e5a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42e5a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42e5a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e5a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e5a-142">CommonParameters</span></span>
<span data-ttu-id="42e5a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e5a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e5a-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e5a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e5a-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42e5a-145">INPUTS</span></span>

### <span data-ttu-id="42e5a-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="42e5a-146">PSAzureContext</span></span>
<span data-ttu-id="42e5a-147">Der Parameter "Context" akzeptiert den Wert vom Typ "PSAzureContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="42e5a-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="42e5a-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42e5a-148">OUTPUTS</span></span>

### <span data-ttu-id="42e5a-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="42e5a-149">PSAzureContext</span></span>

## <span data-ttu-id="42e5a-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="42e5a-150">NOTES</span></span>

## <span data-ttu-id="42e5a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42e5a-151">RELATED LINKS</span></span>

[<span data-ttu-id="42e5a-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="42e5a-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

