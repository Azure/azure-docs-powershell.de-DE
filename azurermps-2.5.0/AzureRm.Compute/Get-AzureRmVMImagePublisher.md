---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850160"
---
# <span data-ttu-id="99b44-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="99b44-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="99b44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99b44-102">SYNOPSIS</span></span>
<span data-ttu-id="99b44-103">Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="99b44-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99b44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99b44-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b44-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99b44-105">DESCRIPTION</span></span>
<span data-ttu-id="99b44-106">Das Cmdlet " **Get-AzureRmVMImagePublisher** " Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="99b44-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="99b44-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99b44-107">EXAMPLES</span></span>

### <span data-ttu-id="99b44-108">Beispiel 1: Abrufen von VMImage-Verlegern für eine Region</span><span class="sxs-lookup"><span data-stu-id="99b44-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="99b44-109">Dieser Befehl ruft die Herausgeber von VMImage-Instanzen für die zentrale US-Region innerhalb Ihres Azure-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="99b44-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="99b44-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="99b44-110">PARAMETERS</span></span>

### <span data-ttu-id="99b44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b44-111">-DefaultProfile</span></span>
<span data-ttu-id="99b44-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99b44-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b44-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="99b44-113">-Location</span></span>
<span data-ttu-id="99b44-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="99b44-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b44-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b44-115">CommonParameters</span></span>
<span data-ttu-id="99b44-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b44-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b44-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b44-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b44-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99b44-118">INPUTS</span></span>

### <span data-ttu-id="99b44-119">Keine</span><span class="sxs-lookup"><span data-stu-id="99b44-119">None</span></span>
<span data-ttu-id="99b44-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="99b44-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99b44-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99b44-121">OUTPUTS</span></span>

### <span data-ttu-id="99b44-122">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="99b44-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="99b44-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="99b44-123">NOTES</span></span>

## <span data-ttu-id="99b44-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99b44-124">RELATED LINKS</span></span>

[<span data-ttu-id="99b44-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="99b44-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="99b44-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="99b44-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="99b44-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="99b44-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="99b44-128">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="99b44-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


