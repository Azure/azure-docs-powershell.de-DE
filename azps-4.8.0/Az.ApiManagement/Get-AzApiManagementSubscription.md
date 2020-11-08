---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010101"
---
# <span data-ttu-id="d3de0-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3de0-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="d3de0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3de0-102">SYNOPSIS</span></span>
<span data-ttu-id="d3de0-103">Ruft Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="d3de0-103">Gets subscriptions.</span></span>

## <span data-ttu-id="d3de0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3de0-104">SYNTAX</span></span>

### <span data-ttu-id="d3de0-105">GetAllSubscriptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3de0-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3de0-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3de0-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3de0-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="d3de0-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3de0-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="d3de0-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3de0-109">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="d3de0-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3de0-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="d3de0-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3de0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3de0-111">DESCRIPTION</span></span>
<span data-ttu-id="d3de0-112">Das Cmdlet " **Get-AzApiManagementSubscription** " Ruft ein angegebenes Abonnement oder alle Abonnements ab, wenn kein Abonnement angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d3de0-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="d3de0-113">Schlüssel werden nicht in Ergebnisdetails berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d3de0-113">Keys will not be included into result details.</span></span> <span data-ttu-id="d3de0-114">Zum Abrufen von Schlüsseln verwenden **Sie Get-AzApiManagementSubscriptionKey**.</span><span class="sxs-lookup"><span data-stu-id="d3de0-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="d3de0-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3de0-115">EXAMPLES</span></span>

### <span data-ttu-id="d3de0-116">Beispiel 1: Abrufen aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="d3de0-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="d3de0-117">Dieser Befehl ruft alle Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="d3de0-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="d3de0-118">Beispiel 2: Abrufen eines Abonnements mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="d3de0-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="d3de0-119">Mit diesem Befehl wird ein Abonnement nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d3de0-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="d3de0-120">Beispiel 3: Abrufen aller Abonnements für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="d3de0-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="d3de0-121">Dieser Befehl ruft die Abonnements eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="d3de0-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="d3de0-122">Beispiel 4: Abrufen aller Abonnements für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="d3de0-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="d3de0-123">Dieser Befehl ruft alle Abonnements für das Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="d3de0-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="d3de0-124">Beispiel 5: Abrufen aller Abonnements für einen Bereich</span><span class="sxs-lookup"><span data-stu-id="d3de0-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="d3de0-125">Dieser Befehl ruft alle Abonnements ab, die für den globalen API-Bereich konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="d3de0-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="d3de0-126">Beispiel 6: Abrufen aller Abonnements für ein Produkt und einen Benutzerbereich</span><span class="sxs-lookup"><span data-stu-id="d3de0-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="d3de0-127">Dieser Befehl ruft alle Abonnements ab, die für den globalen API-Bereich konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="d3de0-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="d3de0-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3de0-128">PARAMETERS</span></span>

### <span data-ttu-id="d3de0-129">-Context</span><span class="sxs-lookup"><span data-stu-id="d3de0-129">-Context</span></span>
<span data-ttu-id="d3de0-130">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d3de0-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3de0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3de0-131">-DefaultProfile</span></span>
<span data-ttu-id="d3de0-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3de0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3de0-133">-ProductID</span><span class="sxs-lookup"><span data-stu-id="d3de0-133">-ProductId</span></span>
<span data-ttu-id="d3de0-134">Gibt eine Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="d3de0-134">Specifies a product identifier.</span></span>
<span data-ttu-id="d3de0-135">Falls angegeben, findet dieses Cmdlet alle Abonnements nach dem Product Identifier.</span><span class="sxs-lookup"><span data-stu-id="d3de0-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3de0-136">-Scope</span><span class="sxs-lookup"><span data-stu-id="d3de0-136">-Scope</span></span>
<span data-ttu-id="d3de0-137">Bereichsbezeichner</span><span class="sxs-lookup"><span data-stu-id="d3de0-137">Scope identifier.</span></span> <span data-ttu-id="d3de0-138">Der Umfang des Abonnements, unabhängig davon, ob es sich um einen API-Bereich/APIs/{apiId} oder um einen Produktbereich handelt/Products/{ProductID} oder globaler API-Bereich/APIs oder globaler Bereich/.</span><span class="sxs-lookup"><span data-stu-id="d3de0-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3de0-139">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d3de0-139">-SubscriptionId</span></span>
<span data-ttu-id="d3de0-140">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="d3de0-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="d3de0-141">Falls angegeben, findet das Cmdlet das Abonnement für den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d3de0-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3de0-142">-UserID</span><span class="sxs-lookup"><span data-stu-id="d3de0-142">-UserId</span></span>
<span data-ttu-id="d3de0-143">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="d3de0-143">Specifies a user identifier.</span></span>
<span data-ttu-id="d3de0-144">Falls angegeben, findet dieses Cmdlet alle Abonnements durch die Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="d3de0-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3de0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3de0-145">CommonParameters</span></span>
<span data-ttu-id="d3de0-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3de0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3de0-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3de0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3de0-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3de0-148">INPUTS</span></span>

### <span data-ttu-id="d3de0-149">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d3de0-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d3de0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d3de0-150">System.String</span></span>

## <span data-ttu-id="d3de0-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3de0-151">OUTPUTS</span></span>

### <span data-ttu-id="d3de0-152">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3de0-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="d3de0-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3de0-153">NOTES</span></span>

## <span data-ttu-id="d3de0-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3de0-154">RELATED LINKS</span></span>

[<span data-ttu-id="d3de0-155">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3de0-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="d3de0-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3de0-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="d3de0-157">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3de0-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


