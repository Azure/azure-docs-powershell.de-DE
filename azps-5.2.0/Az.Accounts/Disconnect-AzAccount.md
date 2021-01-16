---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294370"
---
# <span data-ttu-id="01966-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="01966-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="01966-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01966-102">SYNOPSIS</span></span>
<span data-ttu-id="01966-103">Trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte, die diesem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="01966-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="01966-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01966-104">SYNTAX</span></span>

### <span data-ttu-id="01966-105">ContextName (Standard)</span><span class="sxs-lookup"><span data-stu-id="01966-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01966-106">UserId</span><span class="sxs-lookup"><span data-stu-id="01966-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01966-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="01966-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01966-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="01966-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01966-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="01966-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01966-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01966-110">DESCRIPTION</span></span>
<span data-ttu-id="01966-111">Das Disconnect-AzAccount-Cmdlet trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte (Abonnement- und Mandanteninformationen), die diesem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="01966-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="01966-112">Nachdem Sie dieses Cmdlet ausgeführt haben, müssen Sie sich erneut mit Connect-AzAccount anmelden.</span><span class="sxs-lookup"><span data-stu-id="01966-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="01966-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01966-113">EXAMPLES</span></span>

### <span data-ttu-id="01966-114">Beispiel 1: Abmelden des aktuellen Kontos</span><span class="sxs-lookup"><span data-stu-id="01966-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="01966-115">Meldet sich bei dem Azure-Konto ab, das dem aktuellen Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01966-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="01966-116">Beispiel 2: Abmelden des Kontos, das einem bestimmten Kontext zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="01966-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="01966-117">Meldet das Konto ab, das dem angegebenen Kontext zugeordnet ist (mit dem Namen "Arbeit").</span><span class="sxs-lookup"><span data-stu-id="01966-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="01966-118">Da hier der Bereich "CurrentUser" verwendet wird, werden alle Anmeldeinformationen und Kontexte dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="01966-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="01966-119">Beispiel 3: Abmelden eines bestimmten Benutzers</span><span class="sxs-lookup"><span data-stu-id="01966-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="01966-120">Meldet den Benutzer '' ab. Alle Anmeldeinformationen und alle diesem Benutzer zugeordneten Kontexte user1@contoso.org werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="01966-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="01966-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01966-121">PARAMETERS</span></span>

### <span data-ttu-id="01966-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="01966-122">-ApplicationId</span></span>
<span data-ttu-id="01966-123">ServicePrincipal id (globally unique id)</span><span class="sxs-lookup"><span data-stu-id="01966-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01966-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="01966-124">-AzureContext</span></span>
<span data-ttu-id="01966-125">Kontext</span><span class="sxs-lookup"><span data-stu-id="01966-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01966-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="01966-126">-ContextName</span></span>
<span data-ttu-id="01966-127">Name des Kontexts, von dem der Abmelden durchgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="01966-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01966-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01966-128">-DefaultProfile</span></span>
<span data-ttu-id="01966-129">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="01966-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01966-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01966-130">-InputObject</span></span>
<span data-ttu-id="01966-131">Das zu entfernende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="01966-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01966-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="01966-132">-Scope</span></span>
<span data-ttu-id="01966-133">Bestimmt den Umfang der Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="01966-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="01966-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="01966-134">-TenantId</span></span>
<span data-ttu-id="01966-135">Mandanten-ID (globally unique id)</span><span class="sxs-lookup"><span data-stu-id="01966-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01966-136">-Username</span><span class="sxs-lookup"><span data-stu-id="01966-136">-Username</span></span>
<span data-ttu-id="01966-137">Benutzername des Formulars ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="01966-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01966-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01966-138">-Confirm</span></span>
<span data-ttu-id="01966-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01966-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01966-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01966-140">-WhatIf</span></span>
<span data-ttu-id="01966-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01966-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01966-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01966-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="01966-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01966-143">CommonParameters</span></span>
<span data-ttu-id="01966-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01966-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01966-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01966-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01966-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01966-146">INPUTS</span></span>

### <span data-ttu-id="01966-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="01966-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="01966-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="01966-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="01966-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01966-149">OUTPUTS</span></span>

### <span data-ttu-id="01966-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="01966-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="01966-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01966-151">NOTES</span></span>

## <span data-ttu-id="01966-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01966-152">RELATED LINKS</span></span>
