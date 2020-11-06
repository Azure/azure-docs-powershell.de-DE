---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502533"
---
# <span data-ttu-id="f724b-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="f724b-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="f724b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f724b-102">SYNOPSIS</span></span>
<span data-ttu-id="f724b-103">Sie erhalten Abonnements, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f724b-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f724b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f724b-104">SYNTAX</span></span>

### <span data-ttu-id="f724b-105">ListByIdInTenant (Standard)</span><span class="sxs-lookup"><span data-stu-id="f724b-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f724b-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="f724b-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f724b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f724b-107">DESCRIPTION</span></span>
<span data-ttu-id="f724b-108">Das Get-AzureRmSubscription-Cmdlet ruft die Abonnement-ID, den Abonnement Namen und den Home-Mandanten für Abonnements ab, auf die das aktuelle Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="f724b-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="f724b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f724b-109">EXAMPLES</span></span>

### <span data-ttu-id="f724b-110">Beispiel 1: Abrufen aller Abonnements in allen Mandanten</span><span class="sxs-lookup"><span data-stu-id="f724b-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

<span data-ttu-id="f724b-111">Dieser Befehl ruft alle Abonnements in allen Mandanten ab, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f724b-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="f724b-112">Beispiel 2: Abrufen aller Abonnements für einen bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="f724b-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="f724b-113">Listet alle Abonnements im angegebenen Mandanten auf, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f724b-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="f724b-114">Beispiel 3: Abrufen aller Abonnements im aktuellen Mandanten</span><span class="sxs-lookup"><span data-stu-id="f724b-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="f724b-115">Dieser Befehl ruft alle Abonnements im aktuellen Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f724b-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="f724b-116">Beispiel 4: Ändern des aktuellen Kontexts, um ein bestimmtes Abonnement zu verwenden</span><span class="sxs-lookup"><span data-stu-id="f724b-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

<span data-ttu-id="f724b-117">Dieser Befehl ruft das angegebene Abonnement ab und legt dann den aktuellen Kontext fest, um es zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f724b-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="f724b-118">Alle nachfolgenden Cmdlets in dieser Sitzung verwenden standardmäßig das neue Abonnement (Contoso-Abonnement 1).</span><span class="sxs-lookup"><span data-stu-id="f724b-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="f724b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f724b-119">PARAMETERS</span></span>

### <span data-ttu-id="f724b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f724b-120">-AsJob</span></span>
<span data-ttu-id="f724b-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="f724b-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f724b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f724b-122">-DefaultProfile</span></span>
<span data-ttu-id="f724b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="f724b-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f724b-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f724b-124">-SubscriptionId</span></span>
<span data-ttu-id="f724b-125">Gibt die ID des abzurufenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f724b-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f724b-126">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="f724b-126">-SubscriptionName</span></span>
<span data-ttu-id="f724b-127">Gibt den Namen des abzurufenden Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f724b-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f724b-128">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="f724b-128">-TenantId</span></span>
<span data-ttu-id="f724b-129">Gibt die ID des Mandanten an, der Abonnements enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f724b-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f724b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f724b-130">CommonParameters</span></span>
<span data-ttu-id="f724b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f724b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f724b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f724b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f724b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f724b-133">INPUTS</span></span>

### <span data-ttu-id="f724b-134">Keine</span><span class="sxs-lookup"><span data-stu-id="f724b-134">None</span></span>
<span data-ttu-id="f724b-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f724b-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f724b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f724b-136">OUTPUTS</span></span>

### <span data-ttu-id="f724b-137">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f724b-137">PSAzureSubscription</span></span>

## <span data-ttu-id="f724b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f724b-138">NOTES</span></span>

## <span data-ttu-id="f724b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f724b-139">RELATED LINKS</span></span>

