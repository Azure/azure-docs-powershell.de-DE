---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467848"
---
# <span data-ttu-id="62de9-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="62de9-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="62de9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62de9-102">SYNOPSIS</span></span>
<span data-ttu-id="62de9-103">Ruft die Zulässige Größenrichtlinie für virtuelle Computer in einem Labor in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="62de9-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="62de9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62de9-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62de9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62de9-105">DESCRIPTION</span></span>
<span data-ttu-id="62de9-106">Das **Cmdlet "Get-AzDtlAllowedVMSizesPolicy"** ruft die Richtlinie für zulässige Größen für virtuelle Computer ab, mit der Sie eine Liste der im Labor zulässigen Größen virtueller Computer angeben können.</span><span class="sxs-lookup"><span data-stu-id="62de9-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="62de9-107">Das Cmdlet gibt den Status "Aktiviert" oder "Deaktiviert" der Richtlinie und eine Liste aller zulässigen Größen für virtuelle Computer zurück, die Sie in der angegebenen Richtlinie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="62de9-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="62de9-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62de9-108">EXAMPLES</span></span>

## <span data-ttu-id="62de9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62de9-109">PARAMETERS</span></span>

### <span data-ttu-id="62de9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62de9-110">-DefaultProfile</span></span>
<span data-ttu-id="62de9-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="62de9-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62de9-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="62de9-112">-LabName</span></span>
<span data-ttu-id="62de9-113">Gibt den Namen der Übung an, für die dieses Cmdlet die Größenrichtlinie für virtuelle Computer erhält.</span><span class="sxs-lookup"><span data-stu-id="62de9-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="62de9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62de9-114">-ResourceGroupName</span></span>
<span data-ttu-id="62de9-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="62de9-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62de9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62de9-116">CommonParameters</span></span>
<span data-ttu-id="62de9-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62de9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62de9-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62de9-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62de9-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62de9-119">INPUTS</span></span>

### <span data-ttu-id="62de9-120">System.String</span><span class="sxs-lookup"><span data-stu-id="62de9-120">System.String</span></span>

## <span data-ttu-id="62de9-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62de9-121">OUTPUTS</span></span>

### <span data-ttu-id="62de9-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="62de9-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="62de9-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="62de9-123">NOTES</span></span>

## <span data-ttu-id="62de9-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="62de9-124">RELATED LINKS</span></span>

[<span data-ttu-id="62de9-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="62de9-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


