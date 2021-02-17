---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147484"
---
# <span data-ttu-id="d89c2-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="d89c2-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="d89c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d89c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d89c2-103">Ruft wichtige Informationen für den Zugriff auf den REST-Endpunkt ab, der dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d89c2-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="d89c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d89c2-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89c2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d89c2-105">DESCRIPTION</span></span>
<span data-ttu-id="d89c2-106">Das **Cmdlet "Get-AzMediaServiceKey"** ruft wichtige Informationen für den Zugriff auf den Representational State Transfer (REST)-Endpunkt ab, der dem Azure-Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d89c2-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="d89c2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d89c2-107">EXAMPLES</span></span>

### <span data-ttu-id="d89c2-108">Beispiel 1: Erhalten der wichtigsten Informationen für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="d89c2-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="d89c2-109">Dieser Befehl ruft die wichtigsten Informationen für den Zugriff auf den Mediendienst "MediaService001" ab, der zur Ressourcengruppe "ResourceGroup001" gehört.</span><span class="sxs-lookup"><span data-stu-id="d89c2-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="d89c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d89c2-110">PARAMETERS</span></span>

### <span data-ttu-id="d89c2-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d89c2-111">-AccountName</span></span>
<span data-ttu-id="d89c2-112">Gibt den Namen des Mediendiensts an, von dem dieses Cmdlet die Mediendienstschlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="d89c2-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="d89c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89c2-113">-DefaultProfile</span></span>
<span data-ttu-id="d89c2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d89c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d89c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d89c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="d89c2-116">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="d89c2-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d89c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89c2-117">CommonParameters</span></span>
<span data-ttu-id="d89c2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89c2-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89c2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89c2-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d89c2-120">INPUTS</span></span>

### <span data-ttu-id="d89c2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d89c2-121">System.String</span></span>

## <span data-ttu-id="d89c2-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d89c2-122">OUTPUTS</span></span>

### <span data-ttu-id="d89c2-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d89c2-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="d89c2-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d89c2-124">NOTES</span></span>

## <span data-ttu-id="d89c2-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d89c2-125">RELATED LINKS</span></span>

[<span data-ttu-id="d89c2-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="d89c2-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


