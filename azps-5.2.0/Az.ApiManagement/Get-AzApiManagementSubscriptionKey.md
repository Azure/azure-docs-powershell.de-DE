---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294323"
---
# <span data-ttu-id="40dcd-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="40dcd-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="40dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="40dcd-103">Ruft Abonnementschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="40dcd-103">Gets subscription keys.</span></span>

## <span data-ttu-id="40dcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40dcd-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40dcd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40dcd-105">DESCRIPTION</span></span>
<span data-ttu-id="40dcd-106">Das **Cmdlet "Get-AzApiManagementSubscriptionKey"** ruft die Schlüssel eines angegebenen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="40dcd-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="40dcd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40dcd-107">EXAMPLES</span></span>

### <span data-ttu-id="40dcd-108">Beispiel 1: Erhalten eines Abonnementschlüssels mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="40dcd-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="40dcd-109">Dieser Befehl erhält ein Abonnement nach ID.</span><span class="sxs-lookup"><span data-stu-id="40dcd-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="40dcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40dcd-110">PARAMETERS</span></span>

### <span data-ttu-id="40dcd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="40dcd-111">-Context</span></span>
<span data-ttu-id="40dcd-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="40dcd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40dcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40dcd-113">-DefaultProfile</span></span>
<span data-ttu-id="40dcd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40dcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40dcd-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40dcd-115">-SubscriptionId</span></span>
<span data-ttu-id="40dcd-116">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="40dcd-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="40dcd-117">Falls angegeben, findet dieses Cmdlet das Abonnement nach dem Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="40dcd-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="40dcd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dcd-118">CommonParameters</span></span>
<span data-ttu-id="40dcd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40dcd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dcd-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40dcd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dcd-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40dcd-121">INPUTS</span></span>

### <span data-ttu-id="40dcd-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="40dcd-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40dcd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="40dcd-123">System.String</span></span>

## <span data-ttu-id="40dcd-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40dcd-124">OUTPUTS</span></span>

### <span data-ttu-id="40dcd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="40dcd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="40dcd-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40dcd-126">NOTES</span></span>

## <span data-ttu-id="40dcd-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40dcd-127">RELATED LINKS</span></span>

[<span data-ttu-id="40dcd-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40dcd-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="40dcd-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40dcd-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="40dcd-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40dcd-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="40dcd-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40dcd-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


