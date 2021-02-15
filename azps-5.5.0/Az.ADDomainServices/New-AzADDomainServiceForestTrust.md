---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143828"
---
# <span data-ttu-id="910b0-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="910b0-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="910b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="910b0-102">SYNOPSIS</span></span>
<span data-ttu-id="910b0-103">Erstellen eines Speicherobjekts für ForestTrust</span><span class="sxs-lookup"><span data-stu-id="910b0-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="910b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="910b0-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="910b0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="910b0-105">DESCRIPTION</span></span>
<span data-ttu-id="910b0-106">Erstellen eines Speicherobjekts für ForestTrust</span><span class="sxs-lookup"><span data-stu-id="910b0-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="910b0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="910b0-107">EXAMPLES</span></span>

### <span data-ttu-id="910b0-108">Beispiel 1: Erstellen von ServiceForestTrust für ADDomain</span><span class="sxs-lookup"><span data-stu-id="910b0-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="910b0-109">Erstellen von ServiceForestTrust für ADDomain</span><span class="sxs-lookup"><span data-stu-id="910b0-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="910b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="910b0-110">PARAMETERS</span></span>

### <span data-ttu-id="910b0-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="910b0-111">-FriendlyName</span></span>
<span data-ttu-id="910b0-112">Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="910b0-112">Friendly Name.</span></span>

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

### <span data-ttu-id="910b0-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="910b0-113">-RemoteDnsIP</span></span>
<span data-ttu-id="910b0-114">Remote-DNS-IPS.</span><span class="sxs-lookup"><span data-stu-id="910b0-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="910b0-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="910b0-115">-TrustDirection</span></span>
<span data-ttu-id="910b0-116">Vertrauensstellungsrichtung.</span><span class="sxs-lookup"><span data-stu-id="910b0-116">Trust Direction.</span></span>

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

### <span data-ttu-id="910b0-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="910b0-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="910b0-118">FQDN der vertrauenswürdigen Domäne.</span><span class="sxs-lookup"><span data-stu-id="910b0-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="910b0-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="910b0-119">-TrustPassword</span></span>
<span data-ttu-id="910b0-120">"Kennwort vertrauenswürdig".</span><span class="sxs-lookup"><span data-stu-id="910b0-120">Trust Password.</span></span>

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

### <span data-ttu-id="910b0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910b0-121">CommonParameters</span></span>
<span data-ttu-id="910b0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910b0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910b0-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="910b0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910b0-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="910b0-124">INPUTS</span></span>

## <span data-ttu-id="910b0-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="910b0-125">OUTPUTS</span></span>

### <span data-ttu-id="910b0-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="910b0-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="910b0-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="910b0-127">NOTES</span></span>

<span data-ttu-id="910b0-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="910b0-128">ALIASES</span></span>

## <span data-ttu-id="910b0-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="910b0-129">RELATED LINKS</span></span>

