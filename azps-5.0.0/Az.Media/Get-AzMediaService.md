---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180292"
---
# <span data-ttu-id="9787b-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9787b-101">Get-AzMediaService</span></span>

## <span data-ttu-id="9787b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9787b-102">SYNOPSIS</span></span>
<span data-ttu-id="9787b-103">Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="9787b-103">Gets information about a media service.</span></span>

## <span data-ttu-id="9787b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9787b-104">SYNTAX</span></span>

### <span data-ttu-id="9787b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9787b-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9787b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9787b-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9787b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9787b-107">DESCRIPTION</span></span>
<span data-ttu-id="9787b-108">Das Cmdlet " **Get-AzMediaService** " Ruft Informationen zu einem Mediendienst ab.</span><span class="sxs-lookup"><span data-stu-id="9787b-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="9787b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9787b-109">EXAMPLES</span></span>

### <span data-ttu-id="9787b-110">Beispiel 1: Abrufen aller Mediendienste in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9787b-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="9787b-111">Dieser Befehl ruft Eigenschaften für alle Mediendienste in der Ressourcengruppe mit dem Namen ResourceGroup001 ab.</span><span class="sxs-lookup"><span data-stu-id="9787b-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="9787b-112">Beispiel 2: Abrufen von Mediendienst Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9787b-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="9787b-113">Dieser Befehl ruft die Eigenschaften des Medien Diensts mit dem Namen MediaService1 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="9787b-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="9787b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9787b-114">PARAMETERS</span></span>

### <span data-ttu-id="9787b-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9787b-115">-AccountName</span></span>
<span data-ttu-id="9787b-116">Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9787b-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9787b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9787b-117">-DefaultProfile</span></span>
<span data-ttu-id="9787b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9787b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9787b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9787b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9787b-120">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="9787b-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="9787b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9787b-121">CommonParameters</span></span>
<span data-ttu-id="9787b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9787b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9787b-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9787b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9787b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9787b-124">INPUTS</span></span>

### <span data-ttu-id="9787b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9787b-125">System.String</span></span>

## <span data-ttu-id="9787b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9787b-126">OUTPUTS</span></span>

### <span data-ttu-id="9787b-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="9787b-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="9787b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9787b-128">NOTES</span></span>

## <span data-ttu-id="9787b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9787b-129">RELATED LINKS</span></span>

[<span data-ttu-id="9787b-130">Neu – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9787b-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="9787b-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9787b-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="9787b-132">Satz-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9787b-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


