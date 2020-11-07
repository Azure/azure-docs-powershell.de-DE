---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652358"
---
# <span data-ttu-id="7d752-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="7d752-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="7d752-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d752-102">SYNOPSIS</span></span>
<span data-ttu-id="7d752-103">Erhalten Sie Registrierungs Konten.</span><span class="sxs-lookup"><span data-stu-id="7d752-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="7d752-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d752-104">SYNTAX</span></span>

### <span data-ttu-id="7d752-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d752-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d752-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="7d752-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d752-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d752-107">DESCRIPTION</span></span>
<span data-ttu-id="7d752-108">Das Cmdlet " **Get-AzEnrollmentAccount** " ruft Registrierungs Konten ab.</span><span class="sxs-lookup"><span data-stu-id="7d752-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="7d752-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d752-109">EXAMPLES</span></span>

### <span data-ttu-id="7d752-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d752-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="7d752-111">Abrufen aller verfügbaren Registrierungs Konten</span><span class="sxs-lookup"><span data-stu-id="7d752-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="7d752-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7d752-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="7d752-113">Rufen Sie das registrierungskonto mit der angegebenen Objekt-ID ab.</span><span class="sxs-lookup"><span data-stu-id="7d752-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="7d752-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d752-114">PARAMETERS</span></span>

### <span data-ttu-id="7d752-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d752-115">-DefaultProfile</span></span>
<span data-ttu-id="7d752-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7d752-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d752-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7d752-117">-ObjectId</span></span>
<span data-ttu-id="7d752-118">Die ObjectID eines bestimmten Registrierungs Kontos, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d752-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="7d752-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d752-119">CommonParameters</span></span>
<span data-ttu-id="7d752-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d752-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d752-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d752-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d752-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d752-122">INPUTS</span></span>

### <span data-ttu-id="7d752-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7d752-123">None</span></span>

## <span data-ttu-id="7d752-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d752-124">OUTPUTS</span></span>

### <span data-ttu-id="7d752-125">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="7d752-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="7d752-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d752-126">NOTES</span></span>

## <span data-ttu-id="7d752-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d752-127">RELATED LINKS</span></span>
