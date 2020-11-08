---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008099"
---
# <span data-ttu-id="c1e6b-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c1e6b-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="c1e6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e6b-103">Ruft die Ressourcenverwendung eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="c1e6b-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="c1e6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1e6b-104">SYNTAX</span></span>

### <span data-ttu-id="c1e6b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1e6b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e6b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1e6b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1e6b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1e6b-107">DESCRIPTION</span></span>
<span data-ttu-id="c1e6b-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="c1e6b-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c1e6b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1e6b-109">EXAMPLES</span></span>

### <span data-ttu-id="c1e6b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1e6b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c1e6b-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="c1e6b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="c1e6b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1e6b-112">PARAMETERS</span></span>

### <span data-ttu-id="c1e6b-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c1e6b-113">-CdnProfile</span></span>
<span data-ttu-id="c1e6b-114">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="c1e6b-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="c1e6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e6b-115">-DefaultProfile</span></span>
<span data-ttu-id="c1e6b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c1e6b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1e6b-117">-Profilname</span><span class="sxs-lookup"><span data-stu-id="c1e6b-117">-ProfileName</span></span>
<span data-ttu-id="c1e6b-118">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="c1e6b-118">The name of the profile.</span></span>

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

### <span data-ttu-id="c1e6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1e6b-120">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="c1e6b-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c1e6b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e6b-121">CommonParameters</span></span>
<span data-ttu-id="c1e6b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1e6b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e6b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1e6b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e6b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1e6b-124">INPUTS</span></span>

### <span data-ttu-id="c1e6b-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c1e6b-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c1e6b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1e6b-126">OUTPUTS</span></span>

### <span data-ttu-id="c1e6b-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c1e6b-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="c1e6b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1e6b-128">NOTES</span></span>

## <span data-ttu-id="c1e6b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1e6b-129">RELATED LINKS</span></span>
