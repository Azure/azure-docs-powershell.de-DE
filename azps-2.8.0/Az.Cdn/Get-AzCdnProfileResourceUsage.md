---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 689604037c709496f0ccc5208599f7151eaf2c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652300"
---
# <span data-ttu-id="dbfa0-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="dbfa0-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="dbfa0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbfa0-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfa0-103">Ruft die Ressourcenverwendung eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="dbfa0-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="dbfa0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbfa0-104">SYNTAX</span></span>

### <span data-ttu-id="dbfa0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbfa0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbfa0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbfa0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbfa0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbfa0-107">DESCRIPTION</span></span>
<span data-ttu-id="dbfa0-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="dbfa0-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="dbfa0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbfa0-109">EXAMPLES</span></span>

### <span data-ttu-id="dbfa0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbfa0-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dbfa0-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="dbfa0-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="dbfa0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbfa0-112">PARAMETERS</span></span>

### <span data-ttu-id="dbfa0-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="dbfa0-113">-CdnProfile</span></span>
<span data-ttu-id="dbfa0-114">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="dbfa0-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="dbfa0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfa0-115">-DefaultProfile</span></span>
<span data-ttu-id="dbfa0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dbfa0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbfa0-117">-Profilname</span><span class="sxs-lookup"><span data-stu-id="dbfa0-117">-ProfileName</span></span>
<span data-ttu-id="dbfa0-118">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="dbfa0-118">The name of the profile.</span></span>

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

### <span data-ttu-id="dbfa0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbfa0-119">-ResourceGroupName</span></span>
<span data-ttu-id="dbfa0-120">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="dbfa0-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="dbfa0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfa0-121">CommonParameters</span></span>
<span data-ttu-id="dbfa0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfa0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfa0-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbfa0-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfa0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbfa0-124">INPUTS</span></span>

### <span data-ttu-id="dbfa0-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="dbfa0-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="dbfa0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbfa0-126">OUTPUTS</span></span>

### <span data-ttu-id="dbfa0-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="dbfa0-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="dbfa0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbfa0-128">NOTES</span></span>

## <span data-ttu-id="dbfa0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbfa0-129">RELATED LINKS</span></span>
