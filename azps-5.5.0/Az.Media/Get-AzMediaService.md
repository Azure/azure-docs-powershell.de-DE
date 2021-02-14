---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154644"
---
# <span data-ttu-id="f9f37-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f9f37-101">Get-AzMediaService</span></span>

## <span data-ttu-id="f9f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f37-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f37-103">Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="f9f37-103">Gets information about a media service.</span></span>

## <span data-ttu-id="f9f37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9f37-104">SYNTAX</span></span>

### <span data-ttu-id="f9f37-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9f37-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9f37-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9f37-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9f37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9f37-107">DESCRIPTION</span></span>
<span data-ttu-id="f9f37-108">Das **Cmdlet "Get-AzMediaService"** ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="f9f37-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="f9f37-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9f37-109">EXAMPLES</span></span>

### <span data-ttu-id="f9f37-110">Beispiel 1: Alle Mediendienste in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="f9f37-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="f9f37-111">Dieser Befehl ruft Eigenschaften für alle Mediendienste in der Ressourcengruppe mit dem Namen "ResourceGroup001" ab.</span><span class="sxs-lookup"><span data-stu-id="f9f37-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f9f37-112">Beispiel 2: Erhalten von Mediendiensteigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9f37-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="f9f37-113">Dieser Befehl ruft die Eigenschaften des Mediendiensts "MediaService1" ab, der zur Ressourcengruppe "ResourceGroup002" gehört.</span><span class="sxs-lookup"><span data-stu-id="f9f37-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f9f37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9f37-114">PARAMETERS</span></span>

### <span data-ttu-id="f9f37-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f9f37-115">-AccountName</span></span>
<span data-ttu-id="f9f37-116">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f9f37-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f9f37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f37-117">-DefaultProfile</span></span>
<span data-ttu-id="f9f37-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f9f37-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9f37-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f37-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9f37-120">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="f9f37-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f9f37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f37-121">CommonParameters</span></span>
<span data-ttu-id="f9f37-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f37-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f37-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f37-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9f37-124">INPUTS</span></span>

### <span data-ttu-id="f9f37-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f9f37-125">System.String</span></span>

## <span data-ttu-id="f9f37-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9f37-126">OUTPUTS</span></span>

### <span data-ttu-id="f9f37-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="f9f37-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f9f37-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f9f37-128">NOTES</span></span>

## <span data-ttu-id="f9f37-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f9f37-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9f37-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f9f37-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="f9f37-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f9f37-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f9f37-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f9f37-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


