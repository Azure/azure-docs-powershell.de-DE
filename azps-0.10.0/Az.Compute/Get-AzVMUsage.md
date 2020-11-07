---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844555"
---
# <span data-ttu-id="c80b9-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="c80b9-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="c80b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c80b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c80b9-103">Ruft die Verwendung des virtuellen Computers Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="c80b9-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c80b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c80b9-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c80b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c80b9-105">DESCRIPTION</span></span>
<span data-ttu-id="c80b9-106">Das Cmdlet " **Get-AzVMUsage** " Ruft die Verwendung des Virtual Machine Core count für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="c80b9-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c80b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c80b9-107">EXAMPLES</span></span>

### <span data-ttu-id="c80b9-108">Beispiel 1: Abrufen der Core count-Verwendung für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="c80b9-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="c80b9-109">Dieser Befehl ruft die Core count-Nutzung des virtuellen Computers für den Standort Central US ab.</span><span class="sxs-lookup"><span data-stu-id="c80b9-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="c80b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c80b9-110">PARAMETERS</span></span>

### <span data-ttu-id="c80b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80b9-111">-DefaultProfile</span></span>
<span data-ttu-id="c80b9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c80b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c80b9-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="c80b9-113">-Location</span></span>
<span data-ttu-id="c80b9-114">Gibt den Speicherort an, für den dieses Cmdlet die Verwendung des Core count für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="c80b9-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="c80b9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80b9-115">CommonParameters</span></span>
<span data-ttu-id="c80b9-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c80b9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80b9-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c80b9-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80b9-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c80b9-118">INPUTS</span></span>

### <span data-ttu-id="c80b9-119">Keine</span><span class="sxs-lookup"><span data-stu-id="c80b9-119">None</span></span>
<span data-ttu-id="c80b9-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c80b9-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c80b9-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c80b9-121">OUTPUTS</span></span>

### <span data-ttu-id="c80b9-122">Microsoft. Azure. Commands. Compute. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="c80b9-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="c80b9-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="c80b9-123">NOTES</span></span>

## <span data-ttu-id="c80b9-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c80b9-124">RELATED LINKS</span></span>

[<span data-ttu-id="c80b9-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c80b9-125">Get-AzVM</span></span>](./Get-AzVM.md)


