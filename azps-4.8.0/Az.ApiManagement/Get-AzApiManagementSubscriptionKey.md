---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008766"
---
# <span data-ttu-id="2667a-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="2667a-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="2667a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2667a-102">SYNOPSIS</span></span>
<span data-ttu-id="2667a-103">Ruft Abonnementschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="2667a-103">Gets subscription keys.</span></span>

## <span data-ttu-id="2667a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2667a-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2667a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2667a-105">DESCRIPTION</span></span>
<span data-ttu-id="2667a-106">Das Cmdlet " **Get-AzApiManagementSubscriptionKey** " Ruft die Schlüssel eines angegebenen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="2667a-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="2667a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2667a-107">EXAMPLES</span></span>

### <span data-ttu-id="2667a-108">Beispiel 1: Abrufen von Abonnement Schlüsseln mit einer angegebenen ID</span><span class="sxs-lookup"><span data-stu-id="2667a-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="2667a-109">Mit diesem Befehl wird ein Abonnement nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2667a-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="2667a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2667a-110">PARAMETERS</span></span>

### <span data-ttu-id="2667a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2667a-111">-Context</span></span>
<span data-ttu-id="2667a-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2667a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2667a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2667a-113">-DefaultProfile</span></span>
<span data-ttu-id="2667a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2667a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2667a-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2667a-115">-SubscriptionId</span></span>
<span data-ttu-id="2667a-116">Gibt einen Abonnementbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="2667a-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="2667a-117">Falls angegeben, findet das Cmdlet das Abonnement für den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2667a-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="2667a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2667a-118">CommonParameters</span></span>
<span data-ttu-id="2667a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2667a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2667a-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2667a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2667a-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2667a-121">INPUTS</span></span>

### <span data-ttu-id="2667a-122">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2667a-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2667a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2667a-123">System.String</span></span>

## <span data-ttu-id="2667a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2667a-124">OUTPUTS</span></span>

### <span data-ttu-id="2667a-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="2667a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="2667a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="2667a-126">NOTES</span></span>

## <span data-ttu-id="2667a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2667a-127">RELATED LINKS</span></span>

[<span data-ttu-id="2667a-128">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2667a-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="2667a-129">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2667a-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="2667a-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2667a-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="2667a-131">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2667a-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


