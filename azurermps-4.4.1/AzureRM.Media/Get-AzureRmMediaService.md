---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: d54314686edafba9e72872411c678905adc55f47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665023"
---
# <span data-ttu-id="3f562-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3f562-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="3f562-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f562-102">SYNOPSIS</span></span>
<span data-ttu-id="3f562-103">Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="3f562-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f562-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f562-104">SYNTAX</span></span>

### <span data-ttu-id="3f562-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f562-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f562-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f562-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f562-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f562-107">DESCRIPTION</span></span>
<span data-ttu-id="3f562-108">Das Cmdlet " **Get-AzureRmMediaService** " Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="3f562-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="3f562-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f562-109">EXAMPLES</span></span>

### <span data-ttu-id="3f562-110">Beispiel 1: Abrufen aller Mediendienste in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3f562-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="3f562-111">Dieser Befehl ruft Eigenschaften für alle Mediendienste in der Ressourcengruppe mit dem Namen ResourceGroup001 ab.</span><span class="sxs-lookup"><span data-stu-id="3f562-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="3f562-112">Beispiel 2: Abrufen von Mediendienst Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f562-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="3f562-113">Dieser Befehl ruft die Eigenschaften des Medien Diensts mit dem Namen MediaService1 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="3f562-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="3f562-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f562-114">PARAMETERS</span></span>

### <span data-ttu-id="3f562-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="3f562-115">-AccountName</span></span>
<span data-ttu-id="3f562-116">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3f562-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3f562-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f562-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f562-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="3f562-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="3f562-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f562-119">-DefaultProfile</span></span>
<span data-ttu-id="3f562-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f562-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f562-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f562-121">CommonParameters</span></span>
<span data-ttu-id="3f562-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f562-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f562-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f562-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f562-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f562-124">INPUTS</span></span>

## <span data-ttu-id="3f562-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f562-125">OUTPUTS</span></span>

### <span data-ttu-id="3f562-126">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="3f562-126">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="3f562-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f562-127">NOTES</span></span>

## <span data-ttu-id="3f562-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f562-128">RELATED LINKS</span></span>

[<span data-ttu-id="3f562-129">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3f562-129">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="3f562-130">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3f562-130">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="3f562-131">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3f562-131">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


