---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475054"
---
# <span data-ttu-id="c7de1-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c7de1-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="c7de1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7de1-102">SYNOPSIS</span></span>
<span data-ttu-id="c7de1-103">Ruft die Metadaten ab, mit denen Azure Resource Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c7de1-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="c7de1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7de1-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="c7de1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7de1-105">DESCRIPTION</span></span>
<span data-ttu-id="c7de1-106">Das Get-AzureRmContext-Cmdlet ruft die aktuellen Metadaten ab, mit denen Azure-Ressourcen-Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c7de1-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="c7de1-107">Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die Ziel Azure-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="c7de1-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="c7de1-108">Azure Resource Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure-Ressourcen-Manager-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="c7de1-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="c7de1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7de1-109">EXAMPLES</span></span>

### <span data-ttu-id="c7de1-110">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="c7de1-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="c7de1-111">In diesem Beispiel melden wir uns mit einem Azure-Abonnement mit Add-AzureRmAccount bei unserem Konto an, und dann erhalten wir den Kontext der aktuellen Sitzung durch Aufrufen von Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="c7de1-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="c7de1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7de1-112">PARAMETERS</span></span>

### <span data-ttu-id="c7de1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7de1-113">CommonParameters</span></span>
<span data-ttu-id="c7de1-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7de1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7de1-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7de1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7de1-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7de1-116">INPUTS</span></span>

## <span data-ttu-id="c7de1-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7de1-117">OUTPUTS</span></span>

### <span data-ttu-id="c7de1-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c7de1-118">PSAzureContext</span></span>
<span data-ttu-id="c7de1-119">Dieses Cmdlet gibt das Konto, den Mandanten und das Abonnement zurück, das von Azure Resource Manager-Cmdlets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7de1-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="c7de1-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7de1-120">NOTES</span></span>

## <span data-ttu-id="c7de1-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7de1-121">RELATED LINKS</span></span>

[<span data-ttu-id="c7de1-122">Satz-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="c7de1-122">Set-AzureRMContext</span></span>]()

