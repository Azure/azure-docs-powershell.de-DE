---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505641"
---
# <span data-ttu-id="82ef2-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="82ef2-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="82ef2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="82ef2-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="82ef2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ef2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82ef2-104">SYNTAX</span></span>

### <span data-ttu-id="82ef2-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="82ef2-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82ef2-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="82ef2-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82ef2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82ef2-107">DESCRIPTION</span></span>
<span data-ttu-id="82ef2-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="82ef2-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="82ef2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82ef2-109">EXAMPLES</span></span>

### <span data-ttu-id="82ef2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82ef2-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="82ef2-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="82ef2-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="82ef2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="82ef2-112">PARAMETERS</span></span>

### <span data-ttu-id="82ef2-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="82ef2-113">-CdnProfile</span></span>
<span data-ttu-id="82ef2-114">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="82ef2-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ef2-115">-Profilname</span><span class="sxs-lookup"><span data-stu-id="82ef2-115">-ProfileName</span></span>
<span data-ttu-id="82ef2-116">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="82ef2-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ef2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ef2-117">-ResourceGroupName</span></span>
<span data-ttu-id="82ef2-118">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="82ef2-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ef2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ef2-119">-DefaultProfile</span></span>
<span data-ttu-id="82ef2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82ef2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ef2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ef2-121">CommonParameters</span></span>
<span data-ttu-id="82ef2-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ef2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ef2-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ef2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ef2-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82ef2-124">INPUTS</span></span>

### <span data-ttu-id="82ef2-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="82ef2-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="82ef2-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82ef2-126">OUTPUTS</span></span>

### <span data-ttu-id="82ef2-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="82ef2-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="82ef2-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="82ef2-128">NOTES</span></span>

## <span data-ttu-id="82ef2-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82ef2-129">RELATED LINKS</span></span>

