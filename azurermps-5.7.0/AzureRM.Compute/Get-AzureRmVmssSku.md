---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478610"
---
# <span data-ttu-id="b751d-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="b751d-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="b751d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b751d-102">SYNOPSIS</span></span>
<span data-ttu-id="b751d-103">Ruft die verfügbaren SKUs für das VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="b751d-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b751d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b751d-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="b751d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b751d-105">DESCRIPTION</span></span>
<span data-ttu-id="b751d-106">Das Cmdlet " **Get-AzureRmVmssSku** " Ruft die verfügbaren SKUs für den virtuellen Computer-Skalierungs Satz (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="b751d-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b751d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b751d-107">EXAMPLES</span></span>

### <span data-ttu-id="b751d-108">Beispiel 1: Abrufen aller verfügbaren SKUs vom VMSS</span><span class="sxs-lookup"><span data-stu-id="b751d-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b751d-109">Dieser Befehl ruft alle verfügbaren SKUs aus dem VMSS mit dem Namen ContosoVMSS ab, das zur Ressourcengruppe namens contosogroup gehört.</span><span class="sxs-lookup"><span data-stu-id="b751d-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b751d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b751d-110">PARAMETERS</span></span>

### <span data-ttu-id="b751d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b751d-111">-ResourceGroupName</span></span>
<span data-ttu-id="b751d-112">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="b751d-112">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b751d-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b751d-113">-VMScaleSetName</span></span>
<span data-ttu-id="b751d-114">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="b751d-114">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b751d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b751d-115">CommonParameters</span></span>
<span data-ttu-id="b751d-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b751d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b751d-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b751d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b751d-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b751d-118">INPUTS</span></span>

### <span data-ttu-id="b751d-119">Keine</span><span class="sxs-lookup"><span data-stu-id="b751d-119">None</span></span>
<span data-ttu-id="b751d-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b751d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b751d-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b751d-121">OUTPUTS</span></span>

### <span data-ttu-id="b751d-122">Dieses Cmdlet erzeugt keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b751d-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="b751d-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="b751d-123">NOTES</span></span>

## <span data-ttu-id="b751d-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b751d-124">RELATED LINKS</span></span>

[<span data-ttu-id="b751d-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b751d-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


