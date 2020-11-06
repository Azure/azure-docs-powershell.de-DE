---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503325"
---
# <span data-ttu-id="c6ab4-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6ab4-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="c6ab4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ab4-103">Ruft Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6ab4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6ab4-104">SYNTAX</span></span>

### <span data-ttu-id="c6ab4-105">Abrufen aller Abonnements (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6ab4-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6ab4-106">Abrufen nach subsctiption-ID</span><span class="sxs-lookup"><span data-stu-id="c6ab4-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6ab4-107">Abrufen nach Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="c6ab4-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6ab4-108">Abrufen nach Produkt-ID</span><span class="sxs-lookup"><span data-stu-id="c6ab4-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6ab4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6ab4-109">DESCRIPTION</span></span>
<span data-ttu-id="c6ab4-110">Das Cmdlet " **Get-AzureRmApiManagementSubscription** " Ruft ein angegebenes Abonnement oder alle Abonnements ab, wenn kein Abonnement angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="c6ab4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6ab4-111">EXAMPLES</span></span>

### <span data-ttu-id="c6ab4-112">Beispiel 1: Abrufen aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="c6ab4-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="c6ab4-113">Dieser Befehl ruft alle Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="c6ab4-114">Beispiel 2: Abrufen eines Abonnements mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="c6ab4-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="c6ab4-115">Mit diesem Befehl wird ein Abonnement nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="c6ab4-116">Beispiel 3: Abrufen aller Abonnements für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="c6ab4-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="c6ab4-117">Dieser Befehl ruft die Abonnements eines Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="c6ab4-118">Beispiel 4: Abrufen aller Abonnements für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="c6ab4-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="c6ab4-119">Dieser Befehl ruft alle Abonnements für das Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="c6ab4-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6ab4-120">PARAMETERS</span></span>

### <span data-ttu-id="c6ab4-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c6ab4-121">-Context</span></span>
<span data-ttu-id="c6ab4-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c6ab4-123">-ProductID</span><span class="sxs-lookup"><span data-stu-id="c6ab4-123">-ProductId</span></span>
<span data-ttu-id="c6ab4-124">Gibt eine Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-124">Specifies a product identifier.</span></span>
<span data-ttu-id="c6ab4-125">Falls angegeben, findet dieses Cmdlet alle Abonnements nach dem Product Identifier.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ab4-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c6ab4-126">-SubscriptionId</span></span>
<span data-ttu-id="c6ab4-127">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="c6ab4-128">Falls angegeben, findet das Cmdlet das Abonnement für den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ab4-129">-UserID</span><span class="sxs-lookup"><span data-stu-id="c6ab4-129">-UserId</span></span>
<span data-ttu-id="c6ab4-130">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-130">Specifies a user identifier.</span></span>
<span data-ttu-id="c6ab4-131">Falls angegeben, findet dieses Cmdlet alle Abonnements durch die Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ab4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ab4-132">-DefaultProfile</span></span>
<span data-ttu-id="c6ab4-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6ab4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ab4-134">CommonParameters</span></span>
<span data-ttu-id="c6ab4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ab4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ab4-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6ab4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ab4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6ab4-137">INPUTS</span></span>

## <span data-ttu-id="c6ab4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6ab4-138">OUTPUTS</span></span>

### <span data-ttu-id="c6ab4-139">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="c6ab4-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="c6ab4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6ab4-140">NOTES</span></span>

## <span data-ttu-id="c6ab4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6ab4-141">RELATED LINKS</span></span>

[<span data-ttu-id="c6ab4-142">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6ab4-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c6ab4-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6ab4-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c6ab4-144">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6ab4-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


