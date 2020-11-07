---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664224"
---
# <span data-ttu-id="f97ef-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f97ef-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="f97ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f97ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f97ef-103">Trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte, die diesem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f97ef-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f97ef-104">SYNTAX</span></span>

### <span data-ttu-id="f97ef-105">Contextname (Standard)</span><span class="sxs-lookup"><span data-stu-id="f97ef-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ef-106">UserID</span><span class="sxs-lookup"><span data-stu-id="f97ef-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ef-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f97ef-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ef-108">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="f97ef-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ef-109">Contextobject</span><span class="sxs-lookup"><span data-stu-id="f97ef-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f97ef-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f97ef-110">DESCRIPTION</span></span>
<span data-ttu-id="f97ef-111">Das Disconnect-AzureRmAccount-Cmdlet trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte (Abonnement-und Mandanteninformationen), die diesem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f97ef-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>

<span data-ttu-id="f97ef-112">Nachdem Sie dieses Cmdlet ausgeführt haben, müssen Sie sich mit Connect-AzureRmAccount erneut anmelden.</span><span class="sxs-lookup"><span data-stu-id="f97ef-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="f97ef-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f97ef-113">EXAMPLES</span></span>

### <span data-ttu-id="f97ef-114">Abmelden des aktuellen Kontos</span><span class="sxs-lookup"><span data-stu-id="f97ef-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="f97ef-115">Loggt sich vom Azure-Konto ab, das dem aktuellen Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f97ef-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="f97ef-116">Abmelden des Kontos, das einem bestimmten Kontext zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="f97ef-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="f97ef-117">Loggt das Konto ab, das dem angegebenen Kontext zugeordnet ist ("Arbeit" genannt).</span><span class="sxs-lookup"><span data-stu-id="f97ef-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="f97ef-118">Da dadurch der Bereich "CurrentUser" verwendet wird, werden alle Anmeldeinformationen und Kontexte endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f97ef-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="f97ef-119">Abmelden eines bestimmten Benutzers</span><span class="sxs-lookup"><span data-stu-id="f97ef-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="f97ef-120">Sie user1@contoso.org können die Anmeldeinformationen für "Benutzer" und alle diesem Benutzer zugeordneten Kontexte entfernen.</span><span class="sxs-lookup"><span data-stu-id="f97ef-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="f97ef-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="f97ef-121">PARAMETERS</span></span>

### <span data-ttu-id="f97ef-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f97ef-122">-ApplicationId</span></span>
<span data-ttu-id="f97ef-123">ServicePrincipal-ID (Globally Unique ID)</span><span class="sxs-lookup"><span data-stu-id="f97ef-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-124">-Azurecontext</span><span class="sxs-lookup"><span data-stu-id="f97ef-124">-AzureContext</span></span>
<span data-ttu-id="f97ef-125">Kontext</span><span class="sxs-lookup"><span data-stu-id="f97ef-125">Context</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-126">-Contextname</span><span class="sxs-lookup"><span data-stu-id="f97ef-126">-ContextName</span></span>
<span data-ttu-id="f97ef-127">Name des Kontexts, von dem abgemeldet werden soll</span><span class="sxs-lookup"><span data-stu-id="f97ef-127">Name of the context to log out of</span></span>

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97ef-128">-DefaultProfile</span></span>
<span data-ttu-id="f97ef-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="f97ef-129">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f97ef-130">-InputObject</span></span>
<span data-ttu-id="f97ef-131">Das zu entfernende Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="f97ef-131">The account object to remove</span></span>

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="f97ef-132">-Scope</span></span>
<span data-ttu-id="f97ef-133">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="f97ef-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-134">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="f97ef-134">-TenantId</span></span>
<span data-ttu-id="f97ef-135">Mandanten-ID (Globally Unique ID)</span><span class="sxs-lookup"><span data-stu-id="f97ef-135">Tenant id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-136">-Username</span><span class="sxs-lookup"><span data-stu-id="f97ef-136">-Username</span></span>
<span data-ttu-id="f97ef-137">Benutzername des Formulars ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="f97ef-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f97ef-138">-Confirm</span></span>
<span data-ttu-id="f97ef-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f97ef-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f97ef-140">-WhatIf</span></span>
<span data-ttu-id="f97ef-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f97ef-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f97ef-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f97ef-142">The cmdlet is not executed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97ef-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97ef-143">CommonParameters</span></span>
<span data-ttu-id="f97ef-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f97ef-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97ef-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97ef-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97ef-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f97ef-146">INPUTS</span></span>

### <span data-ttu-id="f97ef-147">Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f97ef-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="f97ef-148">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f97ef-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="f97ef-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f97ef-149">OUTPUTS</span></span>

### <span data-ttu-id="f97ef-150">Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f97ef-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="f97ef-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="f97ef-151">NOTES</span></span>

## <span data-ttu-id="f97ef-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f97ef-152">RELATED LINKS</span></span>
