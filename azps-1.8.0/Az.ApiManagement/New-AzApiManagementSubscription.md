---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821147"
---
# <span data-ttu-id="4f043-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4f043-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="4f043-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f043-102">SYNOPSIS</span></span>
<span data-ttu-id="4f043-103">Erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f043-103">Creates a subscription.</span></span>

## <span data-ttu-id="4f043-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f043-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f043-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f043-105">DESCRIPTION</span></span>
<span data-ttu-id="4f043-106">Das Cmdlet **New-AzApiManagementSubscription** erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f043-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="4f043-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f043-107">EXAMPLES</span></span>

### <span data-ttu-id="4f043-108">Beispiel 1: Abonnieren eines Benutzers für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="4f043-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="4f043-109">Dieser Befehl abonniert einen vorhandenen Benutzer für ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="4f043-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="4f043-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f043-110">PARAMETERS</span></span>

### <span data-ttu-id="4f043-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4f043-111">-Context</span></span>
<span data-ttu-id="4f043-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4f043-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4f043-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f043-113">-DefaultProfile</span></span>
<span data-ttu-id="4f043-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f043-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f043-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4f043-115">-Name</span></span>
<span data-ttu-id="4f043-116">Gibt den Namen des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="4f043-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="4f043-117">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="4f043-117">-PrimaryKey</span></span>
<span data-ttu-id="4f043-118">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="4f043-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="4f043-119">Wenn dieser Parameter nicht angegeben wird, wird der Schlüssel automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="4f043-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="4f043-120">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="4f043-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4f043-121">-ProductID</span><span class="sxs-lookup"><span data-stu-id="4f043-121">-ProductId</span></span>
<span data-ttu-id="4f043-122">Gibt die ID des Produkts an, das Sie abonnieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4f043-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="4f043-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4f043-123">-SecondaryKey</span></span>
<span data-ttu-id="4f043-124">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="4f043-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="4f043-125">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f043-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="4f043-126">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="4f043-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4f043-127">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="4f043-127">-State</span></span>
<span data-ttu-id="4f043-128">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="4f043-128">Specifies the subscription state.</span></span>
<span data-ttu-id="4f043-129">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4f043-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="4f043-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4f043-130">-SubscriptionId</span></span>
<span data-ttu-id="4f043-131">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="4f043-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="4f043-132">Dieser Parameter wird generiert, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="4f043-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="4f043-133">-UserID</span><span class="sxs-lookup"><span data-stu-id="4f043-133">-UserId</span></span>
<span data-ttu-id="4f043-134">Gibt die Abonnenten-ID an.</span><span class="sxs-lookup"><span data-stu-id="4f043-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="4f043-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f043-135">CommonParameters</span></span>
<span data-ttu-id="4f043-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f043-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f043-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f043-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f043-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f043-138">INPUTS</span></span>

### <span data-ttu-id="4f043-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4f043-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4f043-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4f043-140">System.String</span></span>

### <span data-ttu-id="4f043-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4f043-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4f043-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f043-142">OUTPUTS</span></span>

### <span data-ttu-id="4f043-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4f043-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="4f043-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f043-144">NOTES</span></span>

## <span data-ttu-id="4f043-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f043-145">RELATED LINKS</span></span>

[<span data-ttu-id="4f043-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4f043-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="4f043-147">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4f043-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="4f043-148">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4f043-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


