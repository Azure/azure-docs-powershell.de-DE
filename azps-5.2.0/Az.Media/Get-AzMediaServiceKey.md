---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372600"
---
# <span data-ttu-id="37620-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="37620-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="37620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37620-102">SYNOPSIS</span></span>
<span data-ttu-id="37620-103">Ruft wichtige Informationen für den Zugriff auf den REST-Endpunkt ab, der dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="37620-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="37620-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37620-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37620-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37620-105">DESCRIPTION</span></span>
<span data-ttu-id="37620-106">Das **Cmdlet "Get-AzMediaServiceKey"** ruft wichtige Informationen für den Zugriff auf den Representational State Transfer (REST)-Endpunkt ab, der dem Azure-Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="37620-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="37620-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37620-107">EXAMPLES</span></span>

### <span data-ttu-id="37620-108">Beispiel 1: Erhalten der wichtigsten Informationen für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="37620-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="37620-109">Dieser Befehl ruft die wichtigsten Informationen für den Zugriff auf den Mediendienst "MediaService001" ab, der zur Ressourcengruppe "ResourceGroup001" gehört.</span><span class="sxs-lookup"><span data-stu-id="37620-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="37620-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37620-110">PARAMETERS</span></span>

### <span data-ttu-id="37620-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="37620-111">-AccountName</span></span>
<span data-ttu-id="37620-112">Gibt den Namen des Mediendiensts an, von dem dieses Cmdlet die Mediendienstschlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="37620-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="37620-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37620-113">-DefaultProfile</span></span>
<span data-ttu-id="37620-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="37620-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37620-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37620-115">-ResourceGroupName</span></span>
<span data-ttu-id="37620-116">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="37620-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="37620-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37620-117">CommonParameters</span></span>
<span data-ttu-id="37620-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37620-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37620-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37620-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37620-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37620-120">INPUTS</span></span>

### <span data-ttu-id="37620-121">System.String</span><span class="sxs-lookup"><span data-stu-id="37620-121">System.String</span></span>

## <span data-ttu-id="37620-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37620-122">OUTPUTS</span></span>

### <span data-ttu-id="37620-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="37620-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="37620-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37620-124">NOTES</span></span>

## <span data-ttu-id="37620-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37620-125">RELATED LINKS</span></span>

[<span data-ttu-id="37620-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="37620-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


