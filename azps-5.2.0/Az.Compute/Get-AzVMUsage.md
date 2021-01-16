---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294100"
---
# <span data-ttu-id="781bf-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="781bf-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="781bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="781bf-102">SYNOPSIS</span></span>
<span data-ttu-id="781bf-103">Ruft die Core Count-Verwendung eines virtuellen Computers für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="781bf-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="781bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="781bf-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="781bf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="781bf-105">DESCRIPTION</span></span>
<span data-ttu-id="781bf-106">Das **Get-AzVMUsage-Cmdlet** ruft die Core Count-Verwendung des virtuellen Computers für einen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="781bf-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="781bf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="781bf-107">EXAMPLES</span></span>

### <span data-ttu-id="781bf-108">Beispiel 1: Nutzung der Kernanzahl für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="781bf-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="781bf-109">Dieser Befehl ruft die Core Count-Verwendung des virtuellen Computers für den Standort "USA, Mitte" ab.</span><span class="sxs-lookup"><span data-stu-id="781bf-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="781bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="781bf-110">PARAMETERS</span></span>

### <span data-ttu-id="781bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781bf-111">-DefaultProfile</span></span>
<span data-ttu-id="781bf-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="781bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="781bf-113">-Location</span><span class="sxs-lookup"><span data-stu-id="781bf-113">-Location</span></span>
<span data-ttu-id="781bf-114">Gibt den Speicherort an, für den dieses Cmdlet die Core count-Verwendung des virtuellen Computers erhält.</span><span class="sxs-lookup"><span data-stu-id="781bf-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="781bf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781bf-115">CommonParameters</span></span>
<span data-ttu-id="781bf-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="781bf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781bf-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="781bf-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781bf-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="781bf-118">INPUTS</span></span>

### <span data-ttu-id="781bf-119">System.String</span><span class="sxs-lookup"><span data-stu-id="781bf-119">System.String</span></span>

## <span data-ttu-id="781bf-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="781bf-120">OUTPUTS</span></span>

### <span data-ttu-id="781bf-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="781bf-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="781bf-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="781bf-122">NOTES</span></span>

## <span data-ttu-id="781bf-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="781bf-123">RELATED LINKS</span></span>

[<span data-ttu-id="781bf-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="781bf-124">Get-AzVM</span></span>](./Get-AzVM.md)


