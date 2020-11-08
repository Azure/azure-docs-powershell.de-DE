---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997066"
---
# <span data-ttu-id="a104f-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="a104f-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="a104f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a104f-102">SYNOPSIS</span></span>
<span data-ttu-id="a104f-103">Ruft die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="a104f-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a104f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a104f-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a104f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a104f-105">DESCRIPTION</span></span>
<span data-ttu-id="a104f-106">Das Cmdlet " **Get-AzDtlAllowedVMSizesPolicy** " Ruft die zulässige Größen Richtlinie für virtuelle Maschinen ab, mit der Sie eine Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angeben können.</span><span class="sxs-lookup"><span data-stu-id="a104f-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="a104f-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und eine Liste aller zulässigen virtuellen Computer Größen zurück, die Sie in der angegebenen Richtlinie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="a104f-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="a104f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a104f-108">EXAMPLES</span></span>

## <span data-ttu-id="a104f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a104f-109">PARAMETERS</span></span>

### <span data-ttu-id="a104f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a104f-110">-DefaultProfile</span></span>
<span data-ttu-id="a104f-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a104f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a104f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a104f-112">-LabName</span></span>
<span data-ttu-id="a104f-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet eine Größen Richtlinie für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="a104f-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="a104f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a104f-114">-ResourceGroupName</span></span>
<span data-ttu-id="a104f-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="a104f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a104f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a104f-116">CommonParameters</span></span>
<span data-ttu-id="a104f-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a104f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a104f-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a104f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a104f-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a104f-119">INPUTS</span></span>

### <span data-ttu-id="a104f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a104f-120">System.String</span></span>

## <span data-ttu-id="a104f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a104f-121">OUTPUTS</span></span>

### <span data-ttu-id="a104f-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a104f-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a104f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="a104f-123">NOTES</span></span>

## <span data-ttu-id="a104f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a104f-124">RELATED LINKS</span></span>

[<span data-ttu-id="a104f-125">Satz-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="a104f-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


