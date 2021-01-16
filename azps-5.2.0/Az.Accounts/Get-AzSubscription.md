---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294334"
---
# <span data-ttu-id="16604-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="16604-101">Get-AzSubscription</span></span>

## <span data-ttu-id="16604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16604-102">SYNOPSIS</span></span>
<span data-ttu-id="16604-103">Holen Sie sich Abonnements, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="16604-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="16604-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16604-104">SYNTAX</span></span>

### <span data-ttu-id="16604-105">ListByIdInTenant (Standard)</span><span class="sxs-lookup"><span data-stu-id="16604-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16604-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="16604-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16604-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16604-107">DESCRIPTION</span></span>
<span data-ttu-id="16604-108">Das Get-AzSubscription erhält die Abonnement-ID, den Abonnementnamen und den Home-Mandanten für Abonnements, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="16604-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="16604-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16604-109">EXAMPLES</span></span>

### <span data-ttu-id="16604-110">Beispiel 1: Alle Abonnements in allen Mandanten erhalten</span><span class="sxs-lookup"><span data-stu-id="16604-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="16604-111">Dieser Befehl ruft alle Abonnements in allen Mandanten ab, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="16604-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="16604-112">Beispiel 2: Alle Abonnements für einen bestimmten Mandanten erhalten</span><span class="sxs-lookup"><span data-stu-id="16604-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="16604-113">Listet alle Abonnements im angegebenen Mandanten auf, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="16604-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="16604-114">Beispiel 3: Alle Abonnements im aktuellen Mandanten erhalten</span><span class="sxs-lookup"><span data-stu-id="16604-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="16604-115">Dieser Befehl ruft alle Abonnements im aktuellen Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="16604-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="16604-116">Beispiel 4: Ändern des aktuellen Kontexts zur Verwendung eines bestimmten Abonnements</span><span class="sxs-lookup"><span data-stu-id="16604-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="16604-117">Dieser Befehl ruft das angegebene Abonnement ab und legt dann den aktuellen Kontext auf seine Verwendung fest.</span><span class="sxs-lookup"><span data-stu-id="16604-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="16604-118">Alle nachfolgenden Cmdlets in dieser Sitzung verwenden standardmäßig das neue Abonnement (Contoso-Abonnement 1).</span><span class="sxs-lookup"><span data-stu-id="16604-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="16604-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16604-119">PARAMETERS</span></span>

### <span data-ttu-id="16604-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16604-120">-AsJob</span></span>
<span data-ttu-id="16604-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="16604-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="16604-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16604-122">-DefaultProfile</span></span>
<span data-ttu-id="16604-123">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16604-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16604-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16604-124">-SubscriptionId</span></span>
<span data-ttu-id="16604-125">Gibt die ID des zu erhaltenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="16604-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16604-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="16604-126">-SubscriptionName</span></span>
<span data-ttu-id="16604-127">Gibt den Namen des abonnements an, das Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="16604-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16604-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="16604-128">-TenantId</span></span>
<span data-ttu-id="16604-129">Gibt die ID des Mandanten an, der die zu erhaltenden Abonnements enthält.</span><span class="sxs-lookup"><span data-stu-id="16604-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16604-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16604-130">CommonParameters</span></span>
<span data-ttu-id="16604-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16604-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16604-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16604-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16604-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16604-133">INPUTS</span></span>

### <span data-ttu-id="16604-134">System.String</span><span class="sxs-lookup"><span data-stu-id="16604-134">System.String</span></span>

## <span data-ttu-id="16604-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16604-135">OUTPUTS</span></span>

### <span data-ttu-id="16604-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="16604-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="16604-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16604-137">NOTES</span></span>

## <span data-ttu-id="16604-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16604-138">RELATED LINKS</span></span>
