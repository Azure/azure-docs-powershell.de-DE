---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179757"
---
# <span data-ttu-id="56a4f-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="56a4f-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="56a4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="56a4f-103">Listet die SKUs des Ressourcentyps auf.</span><span class="sxs-lookup"><span data-stu-id="56a4f-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="56a4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a4f-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="56a4f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="56a4f-106">Listet die SKUs des Ressourcentyps auf.</span><span class="sxs-lookup"><span data-stu-id="56a4f-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="56a4f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56a4f-107">EXAMPLES</span></span>

### <span data-ttu-id="56a4f-108">Beispiel 1: Auflisten der SKU für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="56a4f-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="56a4f-109">Dieser Befehl listet SKU für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="56a4f-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="56a4f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56a4f-110">PARAMETERS</span></span>

### <span data-ttu-id="56a4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a4f-111">-DefaultProfile</span></span>
<span data-ttu-id="56a4f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56a4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56a4f-113">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="56a4f-113">-SubscriptionId</span></span>
<span data-ttu-id="56a4f-114">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56a4f-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="56a4f-115">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="56a4f-115">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a4f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a4f-116">CommonParameters</span></span>
<span data-ttu-id="56a4f-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a4f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a4f-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56a4f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a4f-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56a4f-119">INPUTS</span></span>

## <span data-ttu-id="56a4f-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56a4f-120">OUTPUTS</span></span>

### <span data-ttu-id="56a4f-121">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="56a4f-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="56a4f-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="56a4f-122">NOTES</span></span>

<span data-ttu-id="56a4f-123">Aliase</span><span class="sxs-lookup"><span data-stu-id="56a4f-123">ALIASES</span></span>

## <span data-ttu-id="56a4f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56a4f-124">RELATED LINKS</span></span>

