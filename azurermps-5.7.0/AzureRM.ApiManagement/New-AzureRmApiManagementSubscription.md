---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 08685a84817f55e030a62b0b98ddc35be9f05843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496690"
---
# <span data-ttu-id="33fd0-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="33fd0-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="33fd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="33fd0-103">Erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33fd0-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33fd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33fd0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33fd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="33fd0-106">Das Cmdlet **New-AzureRmApiManagementSubscription** erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33fd0-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="33fd0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="33fd0-108">Beispiel 1: Abonnieren eines Benutzers für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="33fd0-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="33fd0-109">Dieser Befehl abonniert einen vorhandenen Benutzer für ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="33fd0-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="33fd0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33fd0-110">PARAMETERS</span></span>

### <span data-ttu-id="33fd0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="33fd0-111">-Context</span></span>
<span data-ttu-id="33fd0-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="33fd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fd0-113">-DefaultProfile</span></span>
<span data-ttu-id="33fd0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33fd0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="33fd0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="33fd0-115">-Name</span></span>
<span data-ttu-id="33fd0-116">Gibt den Namen des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-116">Specifies the subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fd0-117">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="33fd0-117">-PrimaryKey</span></span>
<span data-ttu-id="33fd0-118">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="33fd0-119">Wenn dieser Parameter nicht angegeben wird, wird der Schlüssel automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="33fd0-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="33fd0-120">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="33fd0-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="33fd0-121">-ProductID</span><span class="sxs-lookup"><span data-stu-id="33fd0-121">-ProductId</span></span>
<span data-ttu-id="33fd0-122">Gibt die ID des Produkts an, das Sie abonnieren möchten.</span><span class="sxs-lookup"><span data-stu-id="33fd0-122">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fd0-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="33fd0-123">-SecondaryKey</span></span>
<span data-ttu-id="33fd0-124">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="33fd0-125">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="33fd0-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="33fd0-126">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="33fd0-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="33fd0-127">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="33fd0-127">-State</span></span>
<span data-ttu-id="33fd0-128">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-128">Specifies the subscription state.</span></span>
<span data-ttu-id="33fd0-129">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="33fd0-129">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fd0-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="33fd0-130">-SubscriptionId</span></span>
<span data-ttu-id="33fd0-131">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="33fd0-132">Dieser Parameter wird generiert, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="33fd0-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="33fd0-133">-UserID</span><span class="sxs-lookup"><span data-stu-id="33fd0-133">-UserId</span></span>
<span data-ttu-id="33fd0-134">Gibt die Abonnenten-ID an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-134">Specifies the subscriber ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fd0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fd0-135">CommonParameters</span></span>
<span data-ttu-id="33fd0-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33fd0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fd0-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33fd0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fd0-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33fd0-138">INPUTS</span></span>

### <span data-ttu-id="33fd0-139">Keine</span><span class="sxs-lookup"><span data-stu-id="33fd0-139">None</span></span>
<span data-ttu-id="33fd0-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="33fd0-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33fd0-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33fd0-141">OUTPUTS</span></span>

### <span data-ttu-id="33fd0-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="33fd0-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="33fd0-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="33fd0-143">NOTES</span></span>

## <span data-ttu-id="33fd0-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33fd0-144">RELATED LINKS</span></span>

[<span data-ttu-id="33fd0-145">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="33fd0-145">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="33fd0-146">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="33fd0-146">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="33fd0-147">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="33fd0-147">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


