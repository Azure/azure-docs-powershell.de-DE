---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008340"
---
# <span data-ttu-id="fcbec-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fcbec-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="fcbec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcbec-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbec-103">Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="fcbec-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="fcbec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcbec-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcbec-105">DESCRIPTION</span></span>
<span data-ttu-id="fcbec-106">Das Cmdlet " **Get-AzVMImagePublisher** " Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="fcbec-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="fcbec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcbec-107">EXAMPLES</span></span>

### <span data-ttu-id="fcbec-108">Beispiel 1: Abrufen von VMImage-Verlegern für eine Region</span><span class="sxs-lookup"><span data-stu-id="fcbec-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="fcbec-109">Dieser Befehl ruft die Herausgeber von VMImage-Instanzen für die zentrale US-Region innerhalb Ihres Azure-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="fcbec-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="fcbec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcbec-110">PARAMETERS</span></span>

### <span data-ttu-id="fcbec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbec-111">-DefaultProfile</span></span>
<span data-ttu-id="fcbec-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcbec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcbec-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="fcbec-113">-Location</span></span>
<span data-ttu-id="fcbec-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="fcbec-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbec-115">CommonParameters</span></span>
<span data-ttu-id="fcbec-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcbec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbec-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcbec-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbec-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcbec-118">INPUTS</span></span>

### <span data-ttu-id="fcbec-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fcbec-119">System.String</span></span>

## <span data-ttu-id="fcbec-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcbec-120">OUTPUTS</span></span>

### <span data-ttu-id="fcbec-121">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fcbec-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="fcbec-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcbec-122">NOTES</span></span>

## <span data-ttu-id="fcbec-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcbec-123">RELATED LINKS</span></span>

[<span data-ttu-id="fcbec-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="fcbec-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="fcbec-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fcbec-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="fcbec-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fcbec-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="fcbec-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="fcbec-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


