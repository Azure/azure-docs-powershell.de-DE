---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503298"
---
# <span data-ttu-id="7df8d-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7df8d-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="7df8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7df8d-102">SYNOPSIS</span></span>
<span data-ttu-id="7df8d-103">Erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7df8d-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7df8d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7df8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7df8d-105">DESCRIPTION</span></span>
<span data-ttu-id="7df8d-106">Das Cmdlet **New-AzureRmApiManagementSubscription** erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7df8d-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="7df8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7df8d-107">EXAMPLES</span></span>

### <span data-ttu-id="7df8d-108">Beispiel 1: Abonnieren eines Benutzers für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="7df8d-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="7df8d-109">Dieser Befehl abonniert einen vorhandenen Benutzer für ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="7df8d-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="7df8d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7df8d-110">PARAMETERS</span></span>

### <span data-ttu-id="7df8d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7df8d-111">-Context</span></span>
<span data-ttu-id="7df8d-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7df8d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7df8d-113">-Name</span></span>
<span data-ttu-id="7df8d-114">Gibt den Namen des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-114">Specifies the subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df8d-115">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="7df8d-115">-PrimaryKey</span></span>
<span data-ttu-id="7df8d-116">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7df8d-117">Wenn dieser Parameter nicht angegeben wird, wird der Schlüssel automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="7df8d-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="7df8d-118">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7df8d-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7df8d-119">-ProductID</span><span class="sxs-lookup"><span data-stu-id="7df8d-119">-ProductId</span></span>
<span data-ttu-id="7df8d-120">Gibt die ID des Produkts an, das Sie abonnieren möchten.</span><span class="sxs-lookup"><span data-stu-id="7df8d-120">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df8d-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7df8d-121">-SecondaryKey</span></span>
<span data-ttu-id="7df8d-122">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7df8d-123">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7df8d-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="7df8d-124">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7df8d-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7df8d-125">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="7df8d-125">-State</span></span>
<span data-ttu-id="7df8d-126">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-126">Specifies the subscription state.</span></span>
<span data-ttu-id="7df8d-127">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7df8d-127">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df8d-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7df8d-128">-SubscriptionId</span></span>
<span data-ttu-id="7df8d-129">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="7df8d-130">Dieser Parameter wird generiert, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="7df8d-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="7df8d-131">-UserID</span><span class="sxs-lookup"><span data-stu-id="7df8d-131">-UserId</span></span>
<span data-ttu-id="7df8d-132">Gibt die Abonnenten-ID an.</span><span class="sxs-lookup"><span data-stu-id="7df8d-132">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df8d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df8d-133">-DefaultProfile</span></span>
<span data-ttu-id="7df8d-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7df8d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7df8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df8d-135">CommonParameters</span></span>
<span data-ttu-id="7df8d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df8d-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df8d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7df8d-138">INPUTS</span></span>

## <span data-ttu-id="7df8d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7df8d-139">OUTPUTS</span></span>

### <span data-ttu-id="7df8d-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7df8d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7df8d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7df8d-141">NOTES</span></span>

## <span data-ttu-id="7df8d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7df8d-142">RELATED LINKS</span></span>

[<span data-ttu-id="7df8d-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7df8d-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="7df8d-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7df8d-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="7df8d-145">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7df8d-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


