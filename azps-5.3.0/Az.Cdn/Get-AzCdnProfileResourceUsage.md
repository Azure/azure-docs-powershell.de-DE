---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471010"
---
# <span data-ttu-id="cfe99-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="cfe99-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="cfe99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe99-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe99-103">Ruft die Ressourcennutzung eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="cfe99-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="cfe99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfe99-104">SYNTAX</span></span>

### <span data-ttu-id="cfe99-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfe99-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe99-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe99-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfe99-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfe99-107">DESCRIPTION</span></span>
<span data-ttu-id="cfe99-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="cfe99-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="cfe99-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cfe99-109">EXAMPLES</span></span>

### <span data-ttu-id="cfe99-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfe99-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cfe99-111">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="cfe99-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="cfe99-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfe99-112">PARAMETERS</span></span>

### <span data-ttu-id="cfe99-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cfe99-113">-CdnProfile</span></span>
<span data-ttu-id="cfe99-114">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="cfe99-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe99-115">-DefaultProfile</span></span>
<span data-ttu-id="cfe99-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cfe99-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfe99-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cfe99-117">-ProfileName</span></span>
<span data-ttu-id="cfe99-118">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="cfe99-118">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe99-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe99-119">-ResourceGroupName</span></span>
<span data-ttu-id="cfe99-120">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="cfe99-120">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe99-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe99-121">CommonParameters</span></span>
<span data-ttu-id="cfe99-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe99-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe99-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfe99-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe99-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cfe99-124">INPUTS</span></span>

### <span data-ttu-id="cfe99-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="cfe99-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cfe99-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cfe99-126">OUTPUTS</span></span>

### <span data-ttu-id="cfe99-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="cfe99-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="cfe99-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cfe99-128">NOTES</span></span>

## <span data-ttu-id="cfe99-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cfe99-129">RELATED LINKS</span></span>
