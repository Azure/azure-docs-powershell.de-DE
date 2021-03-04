---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: 59f288c74c8f5230375a475df839c491e07e58d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941800"
---
# <span data-ttu-id="2d073-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="2d073-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="2d073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d073-102">SYNOPSIS</span></span>
<span data-ttu-id="2d073-103">Ruft wichtige Informationen für den Zugriff auf den REST-Endpunkt ab, der dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2d073-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="2d073-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d073-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d073-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d073-105">DESCRIPTION</span></span>
<span data-ttu-id="2d073-106">Das **Get-AzMediaServiceKey-Cmdlet** ruft wichtige Informationen für den Zugriff auf den Restendpunkt (Representational State Transfer) ab, der dem Azure-Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2d073-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="2d073-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d073-107">EXAMPLES</span></span>

### <span data-ttu-id="2d073-108">Beispiel 1: Erhalten der wichtigsten Informationen für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="2d073-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="2d073-109">Dieser Befehl ruft die wichtigsten Informationen für den Zugriff auf den Mediendienst mit dem Namen MediaService001 ab, der zur Ressourcengruppe "ResourceGroup001" gehört.</span><span class="sxs-lookup"><span data-stu-id="2d073-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="2d073-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d073-110">PARAMETERS</span></span>

### <span data-ttu-id="2d073-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d073-111">-AccountName</span></span>
<span data-ttu-id="2d073-112">Gibt den Namen des Mediendiensts an, von dem dieses Cmdlet die Mediendienstschlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="2d073-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d073-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d073-113">-DefaultProfile</span></span>
<span data-ttu-id="2d073-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2d073-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d073-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d073-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d073-116">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="2d073-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d073-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d073-117">CommonParameters</span></span>
<span data-ttu-id="2d073-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d073-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d073-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d073-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d073-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d073-120">INPUTS</span></span>

### <span data-ttu-id="2d073-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2d073-121">System.String</span></span>

## <span data-ttu-id="2d073-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d073-122">OUTPUTS</span></span>

### <span data-ttu-id="2d073-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="2d073-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="2d073-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d073-124">NOTES</span></span>

## <span data-ttu-id="2d073-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d073-125">RELATED LINKS</span></span>

[<span data-ttu-id="2d073-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="2d073-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


