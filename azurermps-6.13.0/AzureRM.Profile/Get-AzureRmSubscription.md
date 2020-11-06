---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 62f3e1b357c0a85f30ba4eeba6a92d9b8dfc9dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495790"
---
# <span data-ttu-id="5c17d-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="5c17d-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="5c17d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c17d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c17d-103">Sie erhalten Abonnements, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="5c17d-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c17d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c17d-104">SYNTAX</span></span>

### <span data-ttu-id="5c17d-105">ListByIdInTenant (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c17d-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c17d-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="5c17d-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c17d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c17d-107">DESCRIPTION</span></span>
<span data-ttu-id="5c17d-108">Das Get-AzureRmSubscription-Cmdlet ruft die Abonnement-ID, den Abonnement Namen und den Home-Mandanten für Abonnements ab, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="5c17d-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="5c17d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c17d-109">EXAMPLES</span></span>

### <span data-ttu-id="5c17d-110">Beispiel 1: Abrufen aller Abonnements in allen Mandanten</span><span class="sxs-lookup"><span data-stu-id="5c17d-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="5c17d-111">Dieser Befehl ruft alle Abonnements in allen Mandanten ab, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5c17d-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="5c17d-112">Beispiel 2: Abrufen aller Abonnements für einen bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="5c17d-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="5c17d-113">Listet alle Abonnements im angegebenen Mandanten auf, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5c17d-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="5c17d-114">Beispiel 3: Abrufen aller Abonnements im aktuellen Mandanten</span><span class="sxs-lookup"><span data-stu-id="5c17d-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="5c17d-115">Dieser Befehl ruft alle Abonnements im aktuellen Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5c17d-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="5c17d-116">Beispiel 4: Ändern des aktuellen Kontexts, um ein bestimmtes Abonnement zu verwenden</span><span class="sxs-lookup"><span data-stu-id="5c17d-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="5c17d-117">Dieser Befehl ruft das angegebene Abonnement ab und legt dann den aktuellen Kontext fest, um es zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c17d-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="5c17d-118">Alle nachfolgenden Cmdlets in dieser Sitzung verwenden standardmäßig das neue Abonnement (Contoso-Abonnement 1).</span><span class="sxs-lookup"><span data-stu-id="5c17d-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="5c17d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c17d-119">PARAMETERS</span></span>

### <span data-ttu-id="5c17d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c17d-120">-AsJob</span></span>
<span data-ttu-id="5c17d-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="5c17d-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5c17d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c17d-122">-DefaultProfile</span></span>
<span data-ttu-id="5c17d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="5c17d-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c17d-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5c17d-124">-SubscriptionId</span></span>
<span data-ttu-id="5c17d-125">Gibt die ID des abzurufenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5c17d-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="5c17d-126">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="5c17d-126">-SubscriptionName</span></span>
<span data-ttu-id="5c17d-127">Gibt den Namen des abzurufenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5c17d-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="5c17d-128">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="5c17d-128">-TenantId</span></span>
<span data-ttu-id="5c17d-129">Gibt die ID des Mandanten an, der Abonnements enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c17d-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="5c17d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c17d-130">CommonParameters</span></span>
<span data-ttu-id="5c17d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c17d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c17d-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c17d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c17d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c17d-133">INPUTS</span></span>

### <span data-ttu-id="5c17d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5c17d-134">System.String</span></span>

## <span data-ttu-id="5c17d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c17d-135">OUTPUTS</span></span>

### <span data-ttu-id="5c17d-136">Microsoft. Azure. Commands. profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5c17d-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="5c17d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c17d-137">NOTES</span></span>

## <span data-ttu-id="5c17d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c17d-138">RELATED LINKS</span></span>
