---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477065"
---
# <span data-ttu-id="7ea7e-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7ea7e-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="7ea7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ea7e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea7e-103">Ruft Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ea7e-104">SYNTAX</span></span>

### <span data-ttu-id="7ea7e-105">GetAllSubscriptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ea7e-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea7e-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ea7e-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea7e-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="7ea7e-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea7e-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="7ea7e-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea7e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ea7e-109">DESCRIPTION</span></span>
<span data-ttu-id="7ea7e-110">Das Cmdlet " **Get-AzureRmApiManagementSubscription** " Ruft ein angegebenes Abonnement oder alle Abonnements ab, wenn kein Abonnement angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="7ea7e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ea7e-111">EXAMPLES</span></span>

### <span data-ttu-id="7ea7e-112">Beispiel 1: Abrufen aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="7ea7e-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="7ea7e-113">Dieser Befehl ruft alle Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="7ea7e-114">Beispiel 2: Abrufen eines Abonnements mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="7ea7e-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="7ea7e-115">Mit diesem Befehl wird ein Abonnement nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="7ea7e-116">Beispiel 3: Abrufen aller Abonnements für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="7ea7e-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="7ea7e-117">Dieser Befehl ruft die Abonnements eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="7ea7e-118">Beispiel 4: Abrufen aller Abonnements für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="7ea7e-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="7ea7e-119">Dieser Befehl ruft alle Abonnements für das Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="7ea7e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ea7e-120">PARAMETERS</span></span>

### <span data-ttu-id="7ea7e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="7ea7e-121">-Context</span></span>
<span data-ttu-id="7ea7e-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea7e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea7e-123">-DefaultProfile</span></span>
<span data-ttu-id="7ea7e-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7ea7e-125">-ProductID</span><span class="sxs-lookup"><span data-stu-id="7ea7e-125">-ProductId</span></span>
<span data-ttu-id="7ea7e-126">Gibt eine Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-126">Specifies a product identifier.</span></span>
<span data-ttu-id="7ea7e-127">Falls angegeben, findet dieses Cmdlet alle Abonnements nach dem Product Identifier.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea7e-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7ea7e-128">-SubscriptionId</span></span>
<span data-ttu-id="7ea7e-129">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="7ea7e-130">Falls angegeben, findet das Cmdlet das Abonnement für den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea7e-131">-UserID</span><span class="sxs-lookup"><span data-stu-id="7ea7e-131">-UserId</span></span>
<span data-ttu-id="7ea7e-132">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-132">Specifies a user identifier.</span></span>
<span data-ttu-id="7ea7e-133">Falls angegeben, findet dieses Cmdlet alle Abonnements durch die Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea7e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea7e-134">CommonParameters</span></span>
<span data-ttu-id="7ea7e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea7e-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea7e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea7e-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ea7e-137">INPUTS</span></span>

### <span data-ttu-id="7ea7e-138">Keine</span><span class="sxs-lookup"><span data-stu-id="7ea7e-138">None</span></span>
<span data-ttu-id="7ea7e-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ea7e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ea7e-140">OUTPUTS</span></span>

### <span data-ttu-id="7ea7e-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7ea7e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="7ea7e-142">Das Detail des Abonnements im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="7ea7e-143">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="7ea7e-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="7ea7e-144">Die Liste des Abonnements im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7ea7e-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="7ea7e-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ea7e-145">NOTES</span></span>

## <span data-ttu-id="7ea7e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ea7e-146">RELATED LINKS</span></span>

[<span data-ttu-id="7ea7e-147">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7ea7e-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="7ea7e-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7ea7e-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="7ea7e-149">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7ea7e-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


