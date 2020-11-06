---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506057"
---
# <span data-ttu-id="d20a8-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d20a8-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="d20a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d20a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d20a8-103">Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="d20a8-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d20a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d20a8-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d20a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d20a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d20a8-106">Das Cmdlet " **Get-AzureRmVMImagePublisher** " Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="d20a8-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="d20a8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d20a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d20a8-108">Beispiel 1: Abrufen von VMImage-Verlegern für eine Region</span><span class="sxs-lookup"><span data-stu-id="d20a8-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="d20a8-109">Dieser Befehl ruft die Herausgeber von VMImage-Instanzen für die zentrale US-Region innerhalb Ihres Azure-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="d20a8-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="d20a8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d20a8-110">PARAMETERS</span></span>

### <span data-ttu-id="d20a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20a8-111">-DefaultProfile</span></span>
<span data-ttu-id="d20a8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d20a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d20a8-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="d20a8-113">-Location</span></span>
<span data-ttu-id="d20a8-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="d20a8-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="d20a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20a8-115">CommonParameters</span></span>
<span data-ttu-id="d20a8-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20a8-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20a8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20a8-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d20a8-118">INPUTS</span></span>

### <span data-ttu-id="d20a8-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d20a8-119">System.String</span></span>

## <span data-ttu-id="d20a8-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d20a8-120">OUTPUTS</span></span>

### <span data-ttu-id="d20a8-121">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d20a8-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="d20a8-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="d20a8-122">NOTES</span></span>

## <span data-ttu-id="d20a8-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d20a8-123">RELATED LINKS</span></span>

[<span data-ttu-id="d20a8-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d20a8-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="d20a8-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d20a8-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="d20a8-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d20a8-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="d20a8-127">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d20a8-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


