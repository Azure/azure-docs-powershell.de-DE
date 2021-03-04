---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935912"
---
# <span data-ttu-id="70678-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="70678-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="70678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70678-102">SYNOPSIS</span></span>
<span data-ttu-id="70678-103">Erstellen eines Speicherobjekts für ForestTrust</span><span class="sxs-lookup"><span data-stu-id="70678-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="70678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70678-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="70678-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70678-105">DESCRIPTION</span></span>
<span data-ttu-id="70678-106">Erstellen eines Speicherobjekts für ForestTrust</span><span class="sxs-lookup"><span data-stu-id="70678-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="70678-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70678-107">EXAMPLES</span></span>

### <span data-ttu-id="70678-108">Beispiel 1: Erstellen von ServiceForestTrust für ADDomain</span><span class="sxs-lookup"><span data-stu-id="70678-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="70678-109">Erstellen von ServiceForestTrust für ADDomain</span><span class="sxs-lookup"><span data-stu-id="70678-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="70678-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="70678-110">PARAMETERS</span></span>

### <span data-ttu-id="70678-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="70678-111">-FriendlyName</span></span>
<span data-ttu-id="70678-112">Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="70678-112">Friendly Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70678-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="70678-113">-RemoteDnsIP</span></span>
<span data-ttu-id="70678-114">Remote-Dns-Ips.</span><span class="sxs-lookup"><span data-stu-id="70678-114">Remote Dns ips.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70678-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="70678-115">-TrustDirection</span></span>
<span data-ttu-id="70678-116">Richtung vertrauen.</span><span class="sxs-lookup"><span data-stu-id="70678-116">Trust Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70678-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="70678-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="70678-118">FQDN für vertrauenswürdige Domäne.</span><span class="sxs-lookup"><span data-stu-id="70678-118">Trusted Domain FQDN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70678-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="70678-119">-TrustPassword</span></span>
<span data-ttu-id="70678-120">Kennwort vertrauen.</span><span class="sxs-lookup"><span data-stu-id="70678-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70678-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70678-121">CommonParameters</span></span>
<span data-ttu-id="70678-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70678-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70678-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70678-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70678-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70678-124">INPUTS</span></span>

## <span data-ttu-id="70678-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70678-125">OUTPUTS</span></span>

### <span data-ttu-id="70678-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="70678-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="70678-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="70678-127">NOTES</span></span>

<span data-ttu-id="70678-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="70678-128">ALIASES</span></span>

## <span data-ttu-id="70678-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="70678-129">RELATED LINKS</span></span>

