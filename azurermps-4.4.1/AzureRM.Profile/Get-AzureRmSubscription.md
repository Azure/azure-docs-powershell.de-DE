---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496962"
---
# <span data-ttu-id="5e32f-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="5e32f-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="5e32f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e32f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e32f-103">Sie erhalten Abonnements, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="5e32f-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e32f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e32f-104">SYNTAX</span></span>

### <span data-ttu-id="5e32f-105">ListByIdInTenant (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e32f-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e32f-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="5e32f-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e32f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e32f-107">DESCRIPTION</span></span>
<span data-ttu-id="5e32f-108">Das Get-AzureRmSubscription-Cmdlet ruft die Abonnement-ID, den Abonnement Namen und den Home-Mandanten für Abonnements ab, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="5e32f-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="5e32f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e32f-109">EXAMPLES</span></span>

### <span data-ttu-id="5e32f-110">Beispiel 1: Abrufen aller Abonnements in allen Mandanten</span><span class="sxs-lookup"><span data-stu-id="5e32f-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="5e32f-111">Dieser Befehl ruft alle Abonnements in allen Mandanten ab, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5e32f-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="5e32f-112">Beispiel 2: Abrufen aller Abonnements für einen bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="5e32f-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="5e32f-113">Listet alle Abonnements im angegebenen Mandanten auf, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5e32f-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="5e32f-114">Beispiel 3: Abrufen aller Abonnements im aktuellen Mandanten</span><span class="sxs-lookup"><span data-stu-id="5e32f-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="5e32f-115">Dieser Befehl ruft alle Abonnements im aktuellen Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5e32f-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="5e32f-116">Beispiel 4: Ändern des aktuellen Kontexts, um ein bestimmtes Abonnement zu verwenden</span><span class="sxs-lookup"><span data-stu-id="5e32f-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="5e32f-117">Dieser Befehl ruft das angegebene Abonnement ab und legt dann den aktuellen Kontext fest, um es zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e32f-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="5e32f-118">Alle nachfolgenden Cmdlets in dieser Sitzung verwenden standardmäßig das neue Abonnement (Contoso-Abonnement 1).</span><span class="sxs-lookup"><span data-stu-id="5e32f-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="5e32f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e32f-119">PARAMETERS</span></span>

### <span data-ttu-id="5e32f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e32f-120">-DefaultProfile</span></span>
<span data-ttu-id="5e32f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="5e32f-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e32f-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5e32f-122">-SubscriptionId</span></span>
<span data-ttu-id="5e32f-123">Gibt die ID des abzurufenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5e32f-123">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="5e32f-124">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="5e32f-124">-SubscriptionName</span></span>
<span data-ttu-id="5e32f-125">Gibt den Namen des abzurufenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5e32f-125">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="5e32f-126">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="5e32f-126">-TenantId</span></span>
<span data-ttu-id="5e32f-127">Gibt die ID des Mandanten an, der Abonnements enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e32f-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="5e32f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e32f-128">CommonParameters</span></span>
<span data-ttu-id="5e32f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e32f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e32f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e32f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e32f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e32f-131">INPUTS</span></span>

## <span data-ttu-id="5e32f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e32f-132">OUTPUTS</span></span>

### <span data-ttu-id="5e32f-133">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5e32f-133">PSAzureSubscription</span></span>

## <span data-ttu-id="5e32f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e32f-134">NOTES</span></span>

## <span data-ttu-id="5e32f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e32f-135">RELATED LINKS</span></span>

