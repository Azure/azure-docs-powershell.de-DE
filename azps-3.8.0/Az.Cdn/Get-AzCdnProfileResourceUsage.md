---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003661"
---
# <span data-ttu-id="f782a-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f782a-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="f782a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f782a-102">SYNOPSIS</span></span>
<span data-ttu-id="f782a-103">Ruft die Ressourcenverwendung eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="f782a-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="f782a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f782a-104">SYNTAX</span></span>

### <span data-ttu-id="f782a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f782a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f782a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f782a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f782a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f782a-107">DESCRIPTION</span></span>
<span data-ttu-id="f782a-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="f782a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f782a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f782a-109">EXAMPLES</span></span>

### <span data-ttu-id="f782a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f782a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f782a-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="f782a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f782a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f782a-112">PARAMETERS</span></span>

### <span data-ttu-id="f782a-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f782a-113">-CdnProfile</span></span>
<span data-ttu-id="f782a-114">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="f782a-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="f782a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f782a-115">-DefaultProfile</span></span>
<span data-ttu-id="f782a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f782a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f782a-117">-Profilname</span><span class="sxs-lookup"><span data-stu-id="f782a-117">-ProfileName</span></span>
<span data-ttu-id="f782a-118">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="f782a-118">The name of the profile.</span></span>

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

### <span data-ttu-id="f782a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f782a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f782a-120">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="f782a-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="f782a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f782a-121">CommonParameters</span></span>
<span data-ttu-id="f782a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f782a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f782a-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f782a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f782a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f782a-124">INPUTS</span></span>

### <span data-ttu-id="f782a-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f782a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f782a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f782a-126">OUTPUTS</span></span>

### <span data-ttu-id="f782a-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f782a-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="f782a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f782a-128">NOTES</span></span>

## <span data-ttu-id="f782a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f782a-129">RELATED LINKS</span></span>
