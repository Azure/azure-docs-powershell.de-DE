---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478701"
---
# <span data-ttu-id="9da33-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="9da33-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="9da33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9da33-102">SYNOPSIS</span></span>
<span data-ttu-id="9da33-103">Erhalten Sie Registrierungs Konten.</span><span class="sxs-lookup"><span data-stu-id="9da33-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9da33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9da33-104">SYNTAX</span></span>

### <span data-ttu-id="9da33-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9da33-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9da33-106">Einzel</span><span class="sxs-lookup"><span data-stu-id="9da33-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9da33-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9da33-107">DESCRIPTION</span></span>
<span data-ttu-id="9da33-108">Das Cmdlet " **Get-AzureRmEnrollmentAccount** " ruft Registrierungs Konten ab.</span><span class="sxs-lookup"><span data-stu-id="9da33-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="9da33-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9da33-109">EXAMPLES</span></span>

### <span data-ttu-id="9da33-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9da33-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="9da33-111">Abrufen aller verfügbaren Registrierungs Konten</span><span class="sxs-lookup"><span data-stu-id="9da33-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="9da33-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9da33-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="9da33-113">Rufen Sie das registrierungskonto mit der angegebenen Objekt-ID ab.</span><span class="sxs-lookup"><span data-stu-id="9da33-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="9da33-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9da33-114">PARAMETERS</span></span>

### <span data-ttu-id="9da33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da33-115">-DefaultProfile</span></span>
<span data-ttu-id="9da33-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9da33-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9da33-117">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="9da33-117">-ObjectId</span></span>
<span data-ttu-id="9da33-118">Die ObjectID eines bestimmten Registrierungs Kontos, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9da33-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da33-119">CommonParameters</span></span>
<span data-ttu-id="9da33-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da33-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da33-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da33-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9da33-122">INPUTS</span></span>

### <span data-ttu-id="9da33-123">Keine</span><span class="sxs-lookup"><span data-stu-id="9da33-123">None</span></span>

## <span data-ttu-id="9da33-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9da33-124">OUTPUTS</span></span>

### <span data-ttu-id="9da33-125">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Abrechnungs. Models. PSEnrollmentAccount; Microsoft. Azure. Commands. Billing; Version = 0.14.0.0; Kultur = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9da33-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9da33-126">Microsoft. Azure. Commands. Billing. Models. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="9da33-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="9da33-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9da33-127">NOTES</span></span>

## <span data-ttu-id="9da33-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9da33-128">RELATED LINKS</span></span>

