---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178623"
---
# <span data-ttu-id="0b2c5-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="0b2c5-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="0b2c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2c5-103">Abrufen von Rechnungs Abschnitten</span><span class="sxs-lookup"><span data-stu-id="0b2c5-103">Get invoice sections.</span></span>

## <span data-ttu-id="0b2c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b2c5-104">SYNTAX</span></span>

### <span data-ttu-id="0b2c5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b2c5-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b2c5-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="0b2c5-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b2c5-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2c5-108">Das Cmdlet " **Get-AzInvoiceSection** " ruft Rechnungs Abschnitte unter dem angegebenen Abrechnungsprofil ab.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="0b2c5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b2c5-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2c5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b2c5-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="0b2c5-111">Abrufen aller Rechnungs Abschnitte unter dem angegebenen Abrechnungsprofil</span><span class="sxs-lookup"><span data-stu-id="0b2c5-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="0b2c5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0b2c5-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="0b2c5-113">Rufen Sie den Abschnitt Rechnung mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="0b2c5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b2c5-114">PARAMETERS</span></span>

### <span data-ttu-id="0b2c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2c5-115">-DefaultProfile</span></span>
<span data-ttu-id="0b2c5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b2c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b2c5-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="0b2c5-117">-BillingAccountName</span></span>
<span data-ttu-id="0b2c5-118">Name des bestimmten Abrechnungskontos</span><span class="sxs-lookup"><span data-stu-id="0b2c5-118">Name of the specific billing account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c5-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="0b2c5-119">-BillingProfileName</span></span>
<span data-ttu-id="0b2c5-120">Name des bestimmten Abrechnungs Profils.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-120">Name of the specific billing profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b2c5-121">-Name</span></span>
<span data-ttu-id="0b2c5-122">Der Name eines bestimmten Rechnungs Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-122">Name of a specific invoice section.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2c5-123">CommonParameters</span></span>
<span data-ttu-id="0b2c5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2c5-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2c5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2c5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b2c5-126">INPUTS</span></span>

### <span data-ttu-id="0b2c5-127">Keine</span><span class="sxs-lookup"><span data-stu-id="0b2c5-127">None</span></span>

## <span data-ttu-id="0b2c5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b2c5-128">OUTPUTS</span></span>

### <span data-ttu-id="0b2c5-129">Microsoft. Azure. Commands. Billing. Models. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="0b2c5-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="0b2c5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b2c5-130">NOTES</span></span>

## <span data-ttu-id="0b2c5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b2c5-131">RELATED LINKS</span></span>
