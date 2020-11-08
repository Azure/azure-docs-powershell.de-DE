---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178631"
---
# <span data-ttu-id="22b18-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="22b18-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="22b18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22b18-102">SYNOPSIS</span></span>
<span data-ttu-id="22b18-103">Abrufen von Abrechnungs Profilen</span><span class="sxs-lookup"><span data-stu-id="22b18-103">Get billing profiles.</span></span>

## <span data-ttu-id="22b18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b18-104">SYNTAX</span></span>

### <span data-ttu-id="22b18-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="22b18-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22b18-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="22b18-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b18-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22b18-107">DESCRIPTION</span></span>
<span data-ttu-id="22b18-108">Das Cmdlet " **Get-AzBillingProfile** " ruft Abrechnungsprofile unter dem angegebenen Abrechnungskonto ab.</span><span class="sxs-lookup"><span data-stu-id="22b18-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="22b18-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22b18-109">EXAMPLES</span></span>

### <span data-ttu-id="22b18-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22b18-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="22b18-111">Abrufen aller Abrechnungsprofile unter dem angegebenen Abrechnungskonto</span><span class="sxs-lookup"><span data-stu-id="22b18-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="22b18-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="22b18-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="22b18-113">Rufen Sie das Abrechnungsprofil mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="22b18-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="22b18-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="22b18-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="22b18-115">Rufen Sie alle Abrechnungsprofile unter dem angegebenen Abrechnungskonto ab, und schließen Sie die Rechnungs Abschnitte in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="22b18-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="22b18-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="22b18-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="22b18-117">Rufen Sie das Abrechnungsprofil mit dem angegebenen Namen ab, und schließen Sie die Rechnungs Abschnitte in das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="22b18-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="22b18-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b18-118">PARAMETERS</span></span>

### <span data-ttu-id="22b18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b18-119">-DefaultProfile</span></span>
<span data-ttu-id="22b18-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="22b18-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22b18-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="22b18-121">-BillingAccountName</span></span>
<span data-ttu-id="22b18-122">Name des bestimmten Abrechnungskontos</span><span class="sxs-lookup"><span data-stu-id="22b18-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="22b18-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="22b18-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="22b18-124">Schließen Sie die Abschnitte Rechnungen unter Abrechnungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="22b18-124">Include the invoices sections under billing profile.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b18-125">-Name</span><span class="sxs-lookup"><span data-stu-id="22b18-125">-Name</span></span>
<span data-ttu-id="22b18-126">Name eines bestimmten Abrechnungs Profils.</span><span class="sxs-lookup"><span data-stu-id="22b18-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="22b18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b18-127">CommonParameters</span></span>
<span data-ttu-id="22b18-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b18-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b18-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b18-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22b18-130">INPUTS</span></span>

### <span data-ttu-id="22b18-131">Keine</span><span class="sxs-lookup"><span data-stu-id="22b18-131">None</span></span>

## <span data-ttu-id="22b18-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22b18-132">OUTPUTS</span></span>

### <span data-ttu-id="22b18-133">Microsoft. Azure. Commands. Billing. Models. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="22b18-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="22b18-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="22b18-134">NOTES</span></span>

## <span data-ttu-id="22b18-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22b18-135">RELATED LINKS</span></span>
