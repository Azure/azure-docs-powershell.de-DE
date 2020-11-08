---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005540"
---
# <span data-ttu-id="30c76-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="30c76-101">Get-AzsOffer</span></span>

## <span data-ttu-id="30c76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30c76-102">SYNOPSIS</span></span>
<span data-ttu-id="30c76-103">Rufen Sie die Liste der öffentlichen Angebote für den Stammanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="30c76-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="30c76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30c76-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="30c76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30c76-105">DESCRIPTION</span></span>
<span data-ttu-id="30c76-106">Rufen Sie die Liste der öffentlichen Angebote für den Stammanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="30c76-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="30c76-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30c76-107">EXAMPLES</span></span>

### <span data-ttu-id="30c76-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30c76-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="30c76-109">Abrufen der Liste der öffentlichen Angebote</span><span class="sxs-lookup"><span data-stu-id="30c76-109">Get the list of public offers</span></span>

## <span data-ttu-id="30c76-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30c76-110">PARAMETERS</span></span>

### <span data-ttu-id="30c76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c76-111">-DefaultProfile</span></span>
<span data-ttu-id="30c76-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30c76-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30c76-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c76-113">CommonParameters</span></span>
<span data-ttu-id="30c76-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c76-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c76-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30c76-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c76-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30c76-116">INPUTS</span></span>

## <span data-ttu-id="30c76-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30c76-117">OUTPUTS</span></span>

### <span data-ttu-id="30c76-118">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="30c76-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="30c76-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="30c76-119">NOTES</span></span>

## <span data-ttu-id="30c76-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30c76-120">RELATED LINKS</span></span>

