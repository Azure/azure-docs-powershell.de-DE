---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: dcb5913176af352c39867f7029523765aca0d781
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844583"
---
# <span data-ttu-id="6ea21-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6ea21-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="6ea21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ea21-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea21-103">Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="6ea21-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="6ea21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ea21-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ea21-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea21-106">Das Cmdlet " **Get-AzVMImagePublisher** " Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="6ea21-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="6ea21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ea21-107">EXAMPLES</span></span>

### <span data-ttu-id="6ea21-108">Beispiel 1: Abrufen von VMImage-Verlegern für eine Region</span><span class="sxs-lookup"><span data-stu-id="6ea21-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="6ea21-109">Dieser Befehl ruft die Herausgeber von VMImage-Instanzen für die zentrale US-Region innerhalb Ihres Azure-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="6ea21-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="6ea21-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ea21-110">PARAMETERS</span></span>

### <span data-ttu-id="6ea21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea21-111">-DefaultProfile</span></span>
<span data-ttu-id="6ea21-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ea21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ea21-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="6ea21-113">-Location</span></span>
<span data-ttu-id="6ea21-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="6ea21-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="6ea21-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea21-115">CommonParameters</span></span>
<span data-ttu-id="6ea21-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea21-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea21-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea21-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea21-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ea21-118">INPUTS</span></span>

### <span data-ttu-id="6ea21-119">Keine</span><span class="sxs-lookup"><span data-stu-id="6ea21-119">None</span></span>
<span data-ttu-id="6ea21-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6ea21-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ea21-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ea21-121">OUTPUTS</span></span>

### <span data-ttu-id="6ea21-122">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6ea21-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="6ea21-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ea21-123">NOTES</span></span>

## <span data-ttu-id="6ea21-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ea21-124">RELATED LINKS</span></span>

[<span data-ttu-id="6ea21-125">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6ea21-125">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="6ea21-126">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6ea21-126">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="6ea21-127">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6ea21-127">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="6ea21-128">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6ea21-128">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


