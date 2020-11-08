---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179730"
---
# <span data-ttu-id="85171-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="85171-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="85171-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85171-102">SYNOPSIS</span></span>
<span data-ttu-id="85171-103">Ruft die unterstützten Optimierungs Typen für ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="85171-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="85171-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85171-104">SYNTAX</span></span>

### <span data-ttu-id="85171-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85171-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85171-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85171-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85171-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85171-107">DESCRIPTION</span></span>
<span data-ttu-id="85171-108">Das Cmdlet " **Get-AzCdnProfileSupportedOptimizationType** " Ruft die unterstützten Optimierungs Typen für das aktuelle Profil ab.</span><span class="sxs-lookup"><span data-stu-id="85171-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="85171-109">Ein Benutzer kann einen Endpunkt mit einem Optimierungs aus den aufgelisteten Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="85171-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="85171-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85171-110">EXAMPLES</span></span>

### <span data-ttu-id="85171-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85171-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="85171-112">Rufen Sie die unterstützten Optimierungs Typen für ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="85171-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="85171-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="85171-113">PARAMETERS</span></span>

### <span data-ttu-id="85171-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="85171-114">-CdnProfile</span></span>
<span data-ttu-id="85171-115">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="85171-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="85171-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85171-116">-DefaultProfile</span></span>
<span data-ttu-id="85171-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85171-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85171-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="85171-118">-ProfileName</span></span>
<span data-ttu-id="85171-119">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="85171-119">The name of the profile.</span></span>

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

### <span data-ttu-id="85171-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85171-120">-ResourceGroupName</span></span>
<span data-ttu-id="85171-121">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="85171-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="85171-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85171-122">CommonParameters</span></span>
<span data-ttu-id="85171-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85171-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85171-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85171-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85171-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85171-125">INPUTS</span></span>

### <span data-ttu-id="85171-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="85171-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="85171-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85171-127">OUTPUTS</span></span>

### <span data-ttu-id="85171-128">Microsoft. Azure. Commands. CDN. Models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="85171-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="85171-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="85171-129">NOTES</span></span>

## <span data-ttu-id="85171-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85171-130">RELATED LINKS</span></span>
