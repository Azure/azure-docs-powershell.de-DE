---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850931"
---
# <span data-ttu-id="0b033-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="0b033-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="0b033-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b033-102">SYNOPSIS</span></span>
<span data-ttu-id="0b033-103">Ruft die Verwendung des virtuellen Computers Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="0b033-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b033-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b033-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b033-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b033-105">DESCRIPTION</span></span>
<span data-ttu-id="0b033-106">Das Cmdlet " **Get-AzureRmVMUsage** " Ruft die Verwendung des Virtual Machine Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="0b033-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="0b033-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b033-107">EXAMPLES</span></span>

### <span data-ttu-id="0b033-108">Beispiel 1: Abrufen der Core count-Verwendung für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="0b033-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="0b033-109">Dieser Befehl ruft die Core count-Nutzung des virtuellen Computers für den Standort Central US ab.</span><span class="sxs-lookup"><span data-stu-id="0b033-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="0b033-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b033-110">PARAMETERS</span></span>

### <span data-ttu-id="0b033-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b033-111">-DefaultProfile</span></span>
<span data-ttu-id="0b033-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b033-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b033-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="0b033-113">-Location</span></span>
<span data-ttu-id="0b033-114">Gibt den Speicherort an, für den dieses Cmdlet die Verwendung des Core count für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="0b033-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="0b033-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b033-115">CommonParameters</span></span>
<span data-ttu-id="0b033-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b033-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b033-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b033-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b033-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b033-118">INPUTS</span></span>

### <span data-ttu-id="0b033-119">Keine</span><span class="sxs-lookup"><span data-stu-id="0b033-119">None</span></span>
<span data-ttu-id="0b033-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0b033-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b033-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b033-121">OUTPUTS</span></span>

### <span data-ttu-id="0b033-122">Microsoft. Azure. Commands. Compute. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="0b033-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="0b033-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b033-123">NOTES</span></span>

## <span data-ttu-id="0b033-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b033-124">RELATED LINKS</span></span>

[<span data-ttu-id="0b033-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0b033-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


