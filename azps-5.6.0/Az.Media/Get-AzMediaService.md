---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: fcfd642ceaf2f371385ee1f09c99e1efa566941d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946072"
---
# <span data-ttu-id="61502-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61502-101">Get-AzMediaService</span></span>

## <span data-ttu-id="61502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61502-102">SYNOPSIS</span></span>
<span data-ttu-id="61502-103">Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="61502-103">Gets information about a media service.</span></span>

## <span data-ttu-id="61502-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61502-104">SYNTAX</span></span>

### <span data-ttu-id="61502-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="61502-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61502-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61502-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61502-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61502-107">DESCRIPTION</span></span>
<span data-ttu-id="61502-108">Das **Get-AzMediaService-Cmdlet** ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="61502-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="61502-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61502-109">EXAMPLES</span></span>

### <span data-ttu-id="61502-110">Beispiel 1: Alle Mediendienste in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="61502-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="61502-111">Dieser Befehl ruft Eigenschaften für alle Mediendienste in der Ressourcengruppe "ResourceGroup001" ab.</span><span class="sxs-lookup"><span data-stu-id="61502-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="61502-112">Beispiel 2: Erhalten von Mediendiensteigenschaften</span><span class="sxs-lookup"><span data-stu-id="61502-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="61502-113">Dieser Befehl ruft die Eigenschaften des Mediendiensts mit dem Namen MediaService1 ab, der zur Ressourcengruppe "ResourceGroup002" gehört.</span><span class="sxs-lookup"><span data-stu-id="61502-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="61502-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61502-114">PARAMETERS</span></span>

### <span data-ttu-id="61502-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61502-115">-AccountName</span></span>
<span data-ttu-id="61502-116">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="61502-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61502-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61502-117">-DefaultProfile</span></span>
<span data-ttu-id="61502-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="61502-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61502-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61502-119">-ResourceGroupName</span></span>
<span data-ttu-id="61502-120">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="61502-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="61502-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61502-121">CommonParameters</span></span>
<span data-ttu-id="61502-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61502-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61502-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61502-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61502-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61502-124">INPUTS</span></span>

### <span data-ttu-id="61502-125">System.String</span><span class="sxs-lookup"><span data-stu-id="61502-125">System.String</span></span>

## <span data-ttu-id="61502-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61502-126">OUTPUTS</span></span>

### <span data-ttu-id="61502-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="61502-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="61502-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="61502-128">NOTES</span></span>

## <span data-ttu-id="61502-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="61502-129">RELATED LINKS</span></span>

[<span data-ttu-id="61502-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61502-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="61502-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61502-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="61502-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61502-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


