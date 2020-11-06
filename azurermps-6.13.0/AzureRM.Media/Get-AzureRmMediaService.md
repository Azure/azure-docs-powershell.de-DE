---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 76705a699b814bf52d7c874ec86e067735764936
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482393"
---
# <span data-ttu-id="cf607-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cf607-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="cf607-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf607-102">SYNOPSIS</span></span>
<span data-ttu-id="cf607-103">Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="cf607-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf607-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf607-104">SYNTAX</span></span>

### <span data-ttu-id="cf607-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf607-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf607-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf607-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf607-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf607-107">DESCRIPTION</span></span>
<span data-ttu-id="cf607-108">Das Cmdlet " **Get-AzureRmMediaService** " Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="cf607-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="cf607-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf607-109">EXAMPLES</span></span>

### <span data-ttu-id="cf607-110">Beispiel 1: Abrufen aller Mediendienste in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cf607-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="cf607-111">Dieser Befehl ruft Eigenschaften für alle Mediendienste in der Ressourcengruppe mit dem Namen ResourceGroup001 ab.</span><span class="sxs-lookup"><span data-stu-id="cf607-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="cf607-112">Beispiel 2: Abrufen von Mediendienst Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf607-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="cf607-113">Dieser Befehl ruft die Eigenschaften des Medien Diensts mit dem Namen MediaService1 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="cf607-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="cf607-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf607-114">PARAMETERS</span></span>

### <span data-ttu-id="cf607-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="cf607-115">-AccountName</span></span>
<span data-ttu-id="cf607-116">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cf607-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cf607-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf607-117">-DefaultProfile</span></span>
<span data-ttu-id="cf607-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cf607-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf607-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf607-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf607-120">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="cf607-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cf607-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf607-121">CommonParameters</span></span>
<span data-ttu-id="cf607-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf607-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf607-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf607-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf607-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf607-124">INPUTS</span></span>

### <span data-ttu-id="cf607-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cf607-125">System.String</span></span>

## <span data-ttu-id="cf607-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf607-126">OUTPUTS</span></span>

### <span data-ttu-id="cf607-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="cf607-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="cf607-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf607-128">NOTES</span></span>

## <span data-ttu-id="cf607-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf607-129">RELATED LINKS</span></span>

[<span data-ttu-id="cf607-130">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cf607-130">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="cf607-131">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cf607-131">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="cf607-132">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cf607-132">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


