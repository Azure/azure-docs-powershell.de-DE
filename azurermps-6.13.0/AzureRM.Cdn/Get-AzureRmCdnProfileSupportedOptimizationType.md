---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501190"
---
# <span data-ttu-id="50537-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="50537-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="50537-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50537-102">SYNOPSIS</span></span>
<span data-ttu-id="50537-103">Ruft die unterstützten Optimierungs Typen für ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="50537-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50537-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50537-104">SYNTAX</span></span>

### <span data-ttu-id="50537-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="50537-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50537-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50537-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50537-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50537-107">DESCRIPTION</span></span>
<span data-ttu-id="50537-108">Das Cmdlet " **Get-AzureRmCdnProfileSupportedOptimizationType** " Ruft die unterstützten Optimierungs Typen für das aktuelle Profil ab.</span><span class="sxs-lookup"><span data-stu-id="50537-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="50537-109">Ein Benutzer kann einen Endpunkt mit einem Optimierungs aus den aufgelisteten Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="50537-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="50537-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50537-110">EXAMPLES</span></span>

### <span data-ttu-id="50537-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50537-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="50537-112">Rufen Sie die unterstützten Optimierungs Typen für ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="50537-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="50537-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="50537-113">PARAMETERS</span></span>

### <span data-ttu-id="50537-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="50537-114">-CdnProfile</span></span>
<span data-ttu-id="50537-115">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="50537-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="50537-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50537-116">-DefaultProfile</span></span>
<span data-ttu-id="50537-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50537-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50537-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="50537-118">-ProfileName</span></span>
<span data-ttu-id="50537-119">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="50537-119">The name of the profile.</span></span>

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

### <span data-ttu-id="50537-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50537-120">-ResourceGroupName</span></span>
<span data-ttu-id="50537-121">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="50537-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="50537-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50537-122">CommonParameters</span></span>
<span data-ttu-id="50537-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50537-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50537-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50537-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50537-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50537-125">INPUTS</span></span>

### <span data-ttu-id="50537-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="50537-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="50537-127">Parameter: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50537-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="50537-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50537-128">OUTPUTS</span></span>

### <span data-ttu-id="50537-129">Microsoft. Azure. Commands. CDN. Models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="50537-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="50537-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="50537-130">NOTES</span></span>

## <span data-ttu-id="50537-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50537-131">RELATED LINKS</span></span>
