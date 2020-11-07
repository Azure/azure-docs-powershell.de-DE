---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664681"
---
# <span data-ttu-id="52afd-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="52afd-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="52afd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52afd-102">SYNOPSIS</span></span>
<span data-ttu-id="52afd-103">Ruft die Verwendung des virtuellen Computers Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="52afd-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52afd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52afd-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="52afd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52afd-105">DESCRIPTION</span></span>
<span data-ttu-id="52afd-106">Das Cmdlet " **Get-AzureRmVMUsage** " Ruft die Verwendung des Virtual Machine Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="52afd-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="52afd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52afd-107">EXAMPLES</span></span>

### <span data-ttu-id="52afd-108">Beispiel 1: Abrufen der Core count-Verwendung für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="52afd-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="52afd-109">Dieser Befehl ruft die Core count-Nutzung des virtuellen Computers für den Standort Central US ab.</span><span class="sxs-lookup"><span data-stu-id="52afd-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="52afd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52afd-110">PARAMETERS</span></span>

### <span data-ttu-id="52afd-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="52afd-111">-Location</span></span>
<span data-ttu-id="52afd-112">Gibt den Speicherort an, für den dieses Cmdlet die Verwendung des Core count für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="52afd-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52afd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52afd-113">CommonParameters</span></span>
<span data-ttu-id="52afd-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52afd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52afd-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52afd-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52afd-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52afd-116">INPUTS</span></span>

### <span data-ttu-id="52afd-117">Keine</span><span class="sxs-lookup"><span data-stu-id="52afd-117">None</span></span>
<span data-ttu-id="52afd-118">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="52afd-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52afd-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52afd-119">OUTPUTS</span></span>

## <span data-ttu-id="52afd-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="52afd-120">NOTES</span></span>

## <span data-ttu-id="52afd-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52afd-121">RELATED LINKS</span></span>

[<span data-ttu-id="52afd-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52afd-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


