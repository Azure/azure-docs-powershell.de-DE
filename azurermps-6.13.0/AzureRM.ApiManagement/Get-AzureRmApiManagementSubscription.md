---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 8695d8866b83ed6cd7b29a3d94546da1114d3eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501257"
---
# <span data-ttu-id="ecde0-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecde0-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="ecde0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecde0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecde0-103">Ruft Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="ecde0-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecde0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecde0-104">SYNTAX</span></span>

### <span data-ttu-id="ecde0-105">GetAllSubscriptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecde0-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecde0-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecde0-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecde0-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ecde0-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecde0-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="ecde0-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecde0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecde0-109">DESCRIPTION</span></span>
<span data-ttu-id="ecde0-110">Das Cmdlet " **Get-AzureRmApiManagementSubscription** " Ruft ein angegebenes Abonnement oder alle Abonnements ab, wenn kein Abonnement angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ecde0-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="ecde0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecde0-111">EXAMPLES</span></span>

### <span data-ttu-id="ecde0-112">Beispiel 1: Abrufen aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="ecde0-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="ecde0-113">Dieser Befehl ruft alle Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="ecde0-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="ecde0-114">Beispiel 2: Abrufen eines Abonnements mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="ecde0-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="ecde0-115">Mit diesem Befehl wird ein Abonnement nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ecde0-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="ecde0-116">Beispiel 3: Abrufen aller Abonnements für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="ecde0-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="ecde0-117">Dieser Befehl ruft die Abonnements eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="ecde0-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="ecde0-118">Beispiel 4: Abrufen aller Abonnements für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="ecde0-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="ecde0-119">Dieser Befehl ruft alle Abonnements für das Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="ecde0-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="ecde0-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecde0-120">PARAMETERS</span></span>

### <span data-ttu-id="ecde0-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ecde0-121">-Context</span></span>
<span data-ttu-id="ecde0-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ecde0-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecde0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecde0-123">-DefaultProfile</span></span>
<span data-ttu-id="ecde0-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecde0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecde0-125">-ProductID</span><span class="sxs-lookup"><span data-stu-id="ecde0-125">-ProductId</span></span>
<span data-ttu-id="ecde0-126">Gibt eine Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="ecde0-126">Specifies a product identifier.</span></span>
<span data-ttu-id="ecde0-127">Falls angegeben, findet dieses Cmdlet alle Abonnements nach dem Product Identifier.</span><span class="sxs-lookup"><span data-stu-id="ecde0-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="ecde0-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ecde0-128">-SubscriptionId</span></span>
<span data-ttu-id="ecde0-129">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="ecde0-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="ecde0-130">Falls angegeben, findet das Cmdlet das Abonnement für den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ecde0-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="ecde0-131">-UserID</span><span class="sxs-lookup"><span data-stu-id="ecde0-131">-UserId</span></span>
<span data-ttu-id="ecde0-132">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="ecde0-132">Specifies a user identifier.</span></span>
<span data-ttu-id="ecde0-133">Falls angegeben, findet dieses Cmdlet alle Abonnements durch die Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="ecde0-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="ecde0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecde0-134">CommonParameters</span></span>
<span data-ttu-id="ecde0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecde0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecde0-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecde0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecde0-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecde0-137">INPUTS</span></span>

### <span data-ttu-id="ecde0-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ecde0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ecde0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ecde0-139">System.String</span></span>

## <span data-ttu-id="ecde0-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecde0-140">OUTPUTS</span></span>

### <span data-ttu-id="ecde0-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecde0-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ecde0-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecde0-142">NOTES</span></span>

## <span data-ttu-id="ecde0-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecde0-143">RELATED LINKS</span></span>

[<span data-ttu-id="ecde0-144">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecde0-144">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ecde0-145">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecde0-145">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ecde0-146">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ecde0-146">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


