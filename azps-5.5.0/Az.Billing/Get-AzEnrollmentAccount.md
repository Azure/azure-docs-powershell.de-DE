---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149236"
---
# <span data-ttu-id="9b32f-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="9b32f-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="9b32f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b32f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b32f-103">Registrierungskonten erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b32f-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="9b32f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b32f-104">SYNTAX</span></span>

### <span data-ttu-id="9b32f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b32f-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b32f-106">Single</span><span class="sxs-lookup"><span data-stu-id="9b32f-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b32f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b32f-107">DESCRIPTION</span></span>
<span data-ttu-id="9b32f-108">Das **Get-AzEnrollmentAccount-Cmdlet** ruft Registrierungskonten ab.</span><span class="sxs-lookup"><span data-stu-id="9b32f-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="9b32f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b32f-109">EXAMPLES</span></span>

### <span data-ttu-id="9b32f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b32f-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="9b32f-111">Erhalten Sie alle verfügbaren Registrierungskonten.</span><span class="sxs-lookup"><span data-stu-id="9b32f-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="9b32f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9b32f-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="9b32f-113">Holen Sie sich das Registrierungskonto mit der angegebenen Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="9b32f-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="9b32f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b32f-114">PARAMETERS</span></span>

### <span data-ttu-id="9b32f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b32f-115">-DefaultProfile</span></span>
<span data-ttu-id="9b32f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9b32f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b32f-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9b32f-117">-ObjectId</span></span>
<span data-ttu-id="9b32f-118">ObjectId eines bestimmten Registrierungskontos, das Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="9b32f-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="9b32f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b32f-119">CommonParameters</span></span>
<span data-ttu-id="9b32f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b32f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b32f-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b32f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b32f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b32f-122">INPUTS</span></span>

### <span data-ttu-id="9b32f-123">Keine</span><span class="sxs-lookup"><span data-stu-id="9b32f-123">None</span></span>

## <span data-ttu-id="9b32f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b32f-124">OUTPUTS</span></span>

### <span data-ttu-id="9b32f-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="9b32f-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="9b32f-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9b32f-126">NOTES</span></span>

## <span data-ttu-id="9b32f-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9b32f-127">RELATED LINKS</span></span>
