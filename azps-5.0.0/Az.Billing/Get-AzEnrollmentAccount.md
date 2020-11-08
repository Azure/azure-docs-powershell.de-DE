---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178626"
---
# <span data-ttu-id="5d4d8-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="5d4d8-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="5d4d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4d8-103">Erhalten Sie Registrierungs Konten.</span><span class="sxs-lookup"><span data-stu-id="5d4d8-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="5d4d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d4d8-104">SYNTAX</span></span>

### <span data-ttu-id="5d4d8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d4d8-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4d8-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="5d4d8-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d4d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d4d8-107">DESCRIPTION</span></span>
<span data-ttu-id="5d4d8-108">Das Cmdlet " **Get-AzEnrollmentAccount** " ruft Registrierungs Konten ab.</span><span class="sxs-lookup"><span data-stu-id="5d4d8-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="5d4d8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d4d8-109">EXAMPLES</span></span>

### <span data-ttu-id="5d4d8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d4d8-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="5d4d8-111">Abrufen aller verfügbaren Registrierungs Konten</span><span class="sxs-lookup"><span data-stu-id="5d4d8-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="5d4d8-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5d4d8-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="5d4d8-113">Rufen Sie das registrierungskonto mit der angegebenen Objekt-ID ab.</span><span class="sxs-lookup"><span data-stu-id="5d4d8-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="5d4d8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d4d8-114">PARAMETERS</span></span>

### <span data-ttu-id="5d4d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4d8-115">-DefaultProfile</span></span>
<span data-ttu-id="5d4d8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5d4d8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d4d8-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5d4d8-117">-ObjectId</span></span>
<span data-ttu-id="5d4d8-118">Die ObjectID eines bestimmten Registrierungs Kontos, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d4d8-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="5d4d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4d8-119">CommonParameters</span></span>
<span data-ttu-id="5d4d8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4d8-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d4d8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4d8-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d4d8-122">INPUTS</span></span>

### <span data-ttu-id="5d4d8-123">Keine</span><span class="sxs-lookup"><span data-stu-id="5d4d8-123">None</span></span>

## <span data-ttu-id="5d4d8-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d4d8-124">OUTPUTS</span></span>

### <span data-ttu-id="5d4d8-125">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="5d4d8-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="5d4d8-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d4d8-126">NOTES</span></span>

## <span data-ttu-id="5d4d8-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d4d8-127">RELATED LINKS</span></span>
