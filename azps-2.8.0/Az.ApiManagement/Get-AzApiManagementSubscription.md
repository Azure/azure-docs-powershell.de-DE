---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658300"
---
# <span data-ttu-id="e7911-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e7911-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e7911-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7911-102">SYNOPSIS</span></span>
<span data-ttu-id="e7911-103">Ruft Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="e7911-103">Gets subscriptions.</span></span>

## <span data-ttu-id="e7911-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7911-104">SYNTAX</span></span>

### <span data-ttu-id="e7911-105">GetAllSubscriptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7911-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7911-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7911-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7911-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="e7911-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7911-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="e7911-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7911-109">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="e7911-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7911-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="e7911-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7911-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7911-111">DESCRIPTION</span></span>
<span data-ttu-id="e7911-112">Das Cmdlet " **Get-AzApiManagementSubscription** " Ruft ein angegebenes Abonnement oder alle Abonnements ab, wenn kein Abonnement angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e7911-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="e7911-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7911-113">EXAMPLES</span></span>

### <span data-ttu-id="e7911-114">Beispiel 1: Abrufen aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="e7911-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="e7911-115">Dieser Befehl ruft alle Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="e7911-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="e7911-116">Beispiel 2: Abrufen eines Abonnements mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="e7911-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="e7911-117">Mit diesem Befehl wird ein Abonnement nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e7911-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="e7911-118">Beispiel 3: Abrufen aller Abonnements für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="e7911-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="e7911-119">Dieser Befehl ruft die Abonnements eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="e7911-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="e7911-120">Beispiel 4: Abrufen aller Abonnements für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="e7911-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="e7911-121">Dieser Befehl ruft alle Abonnements für das Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="e7911-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="e7911-122">Beispiel 5: Abrufen aller Abonnements für einen Bereich</span><span class="sxs-lookup"><span data-stu-id="e7911-122">Example 5: Get all subscriptions for a Scope</span></span>
```
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

<span data-ttu-id="e7911-123">Dieser Befehl ruft alle Abonnements ab, die für den globalen API-Bereich konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="e7911-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="e7911-124">Beispiel 5: Abrufen aller Abonnements für ein Produkt und einen Benutzerbereich</span><span class="sxs-lookup"><span data-stu-id="e7911-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
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

<span data-ttu-id="e7911-125">Dieser Befehl ruft alle Abonnements ab, die für den globalen API-Bereich konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="e7911-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="e7911-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7911-126">PARAMETERS</span></span>

### <span data-ttu-id="e7911-127">-Context</span><span class="sxs-lookup"><span data-stu-id="e7911-127">-Context</span></span>
<span data-ttu-id="e7911-128">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e7911-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e7911-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7911-129">-DefaultProfile</span></span>
<span data-ttu-id="e7911-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7911-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7911-131">-ProductID</span><span class="sxs-lookup"><span data-stu-id="e7911-131">-ProductId</span></span>
<span data-ttu-id="e7911-132">Gibt eine Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="e7911-132">Specifies a product identifier.</span></span>
<span data-ttu-id="e7911-133">Falls angegeben, findet dieses Cmdlet alle Abonnements nach dem Product Identifier.</span><span class="sxs-lookup"><span data-stu-id="e7911-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="e7911-134">-Scope</span><span class="sxs-lookup"><span data-stu-id="e7911-134">-Scope</span></span>
<span data-ttu-id="e7911-135">Bereichsbezeichner</span><span class="sxs-lookup"><span data-stu-id="e7911-135">Scope identifier.</span></span> <span data-ttu-id="e7911-136">Der Umfang des Abonnements, unabhängig davon, ob es sich um einen API-Bereich/APIs/{apiId} oder um einen Produktbereich handelt/Products/{ProductID} oder globaler API-Bereich/APIs oder globaler Bereich/.</span><span class="sxs-lookup"><span data-stu-id="e7911-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="e7911-137">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e7911-137">-SubscriptionId</span></span>
<span data-ttu-id="e7911-138">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="e7911-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="e7911-139">Falls angegeben, findet das Cmdlet das Abonnement für den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e7911-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="e7911-140">-UserID</span><span class="sxs-lookup"><span data-stu-id="e7911-140">-UserId</span></span>
<span data-ttu-id="e7911-141">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="e7911-141">Specifies a user identifier.</span></span>
<span data-ttu-id="e7911-142">Falls angegeben, findet dieses Cmdlet alle Abonnements durch die Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="e7911-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="e7911-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7911-143">CommonParameters</span></span>
<span data-ttu-id="e7911-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7911-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7911-145">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7911-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7911-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7911-146">INPUTS</span></span>

### <span data-ttu-id="e7911-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e7911-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e7911-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e7911-148">System.String</span></span>

## <span data-ttu-id="e7911-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7911-149">OUTPUTS</span></span>

### <span data-ttu-id="e7911-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e7911-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e7911-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7911-151">NOTES</span></span>

## <span data-ttu-id="e7911-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7911-152">RELATED LINKS</span></span>

[<span data-ttu-id="e7911-153">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e7911-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="e7911-154">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e7911-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="e7911-155">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e7911-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


