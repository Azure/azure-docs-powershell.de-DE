---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010259"
---
# <span data-ttu-id="5d5fe-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="5d5fe-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="5d5fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5fe-103">Erhalten Sie Registrierungs Konten.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="5d5fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d5fe-104">SYNTAX</span></span>

### <span data-ttu-id="5d5fe-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d5fe-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d5fe-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="5d5fe-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d5fe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d5fe-107">DESCRIPTION</span></span>
<span data-ttu-id="5d5fe-108">Das Cmdlet " **Get-AzEnrollmentAccount** " ruft Registrierungs Konten ab.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="5d5fe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d5fe-109">EXAMPLES</span></span>

### <span data-ttu-id="5d5fe-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d5fe-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="5d5fe-111">Abrufen aller verfügbaren Registrierungs Konten</span><span class="sxs-lookup"><span data-stu-id="5d5fe-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="5d5fe-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d5fe-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="5d5fe-113">Rufen Sie das registrierungskonto mit der angegebenen Objekt-ID ab.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="5d5fe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d5fe-114">PARAMETERS</span></span>

### <span data-ttu-id="5d5fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5fe-115">-DefaultProfile</span></span>
<span data-ttu-id="5d5fe-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5d5fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d5fe-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5d5fe-117">-ObjectId</span></span>
<span data-ttu-id="5d5fe-118">Die ObjectID eines bestimmten Registrierungs Kontos, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5fe-119">CommonParameters</span></span>
<span data-ttu-id="5d5fe-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5fe-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5fe-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5fe-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d5fe-122">INPUTS</span></span>

### <span data-ttu-id="5d5fe-123">Keine</span><span class="sxs-lookup"><span data-stu-id="5d5fe-123">None</span></span>

## <span data-ttu-id="5d5fe-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d5fe-124">OUTPUTS</span></span>

### <span data-ttu-id="5d5fe-125">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="5d5fe-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="5d5fe-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d5fe-126">NOTES</span></span>

## <span data-ttu-id="5d5fe-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d5fe-127">RELATED LINKS</span></span>
