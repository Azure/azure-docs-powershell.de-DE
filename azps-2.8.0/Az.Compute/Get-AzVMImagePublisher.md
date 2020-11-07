---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: f2b0cd955cd63eb6066da43e8b468ab4ea9bb0bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652132"
---
# <span data-ttu-id="ac7f1-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ac7f1-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="ac7f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7f1-103">Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="ac7f1-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="ac7f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac7f1-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac7f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac7f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ac7f1-106">Das Cmdlet " **Get-AzVMImagePublisher** " Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="ac7f1-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="ac7f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="ac7f1-108">Beispiel 1: Abrufen von VMImage-Verlegern für eine Region</span><span class="sxs-lookup"><span data-stu-id="ac7f1-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="ac7f1-109">Dieser Befehl ruft die Herausgeber von VMImage-Instanzen für die zentrale US-Region innerhalb Ihres Azure-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="ac7f1-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="ac7f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac7f1-110">PARAMETERS</span></span>

### <span data-ttu-id="ac7f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac7f1-111">-DefaultProfile</span></span>
<span data-ttu-id="ac7f1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac7f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac7f1-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="ac7f1-113">-Location</span></span>
<span data-ttu-id="ac7f1-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="ac7f1-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="ac7f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7f1-115">CommonParameters</span></span>
<span data-ttu-id="ac7f1-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac7f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7f1-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac7f1-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7f1-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac7f1-118">INPUTS</span></span>

### <span data-ttu-id="ac7f1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ac7f1-119">System.String</span></span>

## <span data-ttu-id="ac7f1-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac7f1-120">OUTPUTS</span></span>

### <span data-ttu-id="ac7f1-121">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ac7f1-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="ac7f1-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac7f1-122">NOTES</span></span>

## <span data-ttu-id="ac7f1-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac7f1-123">RELATED LINKS</span></span>

[<span data-ttu-id="ac7f1-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ac7f1-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ac7f1-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="ac7f1-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="ac7f1-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ac7f1-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="ac7f1-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ac7f1-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


