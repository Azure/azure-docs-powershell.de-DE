---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949480"
---
# <span data-ttu-id="f1965-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="f1965-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="f1965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1965-102">SYNOPSIS</span></span>
<span data-ttu-id="f1965-103">Ruft die Kernanzahl der virtuellen Computer für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="f1965-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="f1965-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1965-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1965-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1965-105">DESCRIPTION</span></span>
<span data-ttu-id="f1965-106">Das **Get-AzVMUsage-Cmdlet** ruft die Kernanzahl des virtuellen Computers für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="f1965-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="f1965-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1965-107">EXAMPLES</span></span>

### <span data-ttu-id="f1965-108">Beispiel 1: Kernanzahl für einen Speicherort erhalten</span><span class="sxs-lookup"><span data-stu-id="f1965-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="f1965-109">Mit diesem Befehl wird die Kernanzahl des virtuellen Computers für den Standort "Usa, Mitte" ab.</span><span class="sxs-lookup"><span data-stu-id="f1965-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="f1965-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1965-110">PARAMETERS</span></span>

### <span data-ttu-id="f1965-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1965-111">-DefaultProfile</span></span>
<span data-ttu-id="f1965-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1965-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1965-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f1965-113">-Location</span></span>
<span data-ttu-id="f1965-114">Gibt den Speicherort an, für den dieses Cmdlet die Core-Anzahl der virtuellen Computer erhält.</span><span class="sxs-lookup"><span data-stu-id="f1965-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="f1965-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1965-115">CommonParameters</span></span>
<span data-ttu-id="f1965-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1965-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1965-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1965-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1965-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1965-118">INPUTS</span></span>

### <span data-ttu-id="f1965-119">System.String</span><span class="sxs-lookup"><span data-stu-id="f1965-119">System.String</span></span>

## <span data-ttu-id="f1965-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1965-120">OUTPUTS</span></span>

### <span data-ttu-id="f1965-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="f1965-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="f1965-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1965-122">NOTES</span></span>

## <span data-ttu-id="f1965-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1965-123">RELATED LINKS</span></span>

[<span data-ttu-id="f1965-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1965-124">Get-AzVM</span></span>](./Get-AzVM.md)


