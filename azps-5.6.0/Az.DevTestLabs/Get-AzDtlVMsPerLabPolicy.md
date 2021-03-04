---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: fa19f45527302c858593d200fb2a6ed605d02321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930083"
---
# <span data-ttu-id="8f42f-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="8f42f-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="8f42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f42f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f42f-103">Ruft die virtuellen Computer pro Lab-Richtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="8f42f-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="8f42f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f42f-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f42f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f42f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f42f-106">Das **Get-AzDtlVMsPerLabPolicy-Cmdlet** ruft die virtuellen Computer pro Lab-Richtlinie einer Übung ab, wodurch Sie die Gesamtanzahl der in einer Übung zugelassenen virtuellen Computer festlegen können.</span><span class="sxs-lookup"><span data-stu-id="8f42f-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="8f42f-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die Gesamtanzahl der virtuellen Computer zurück, die in der in der Richtlinie festgelegten Übungseinheit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8f42f-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="8f42f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f42f-108">EXAMPLES</span></span>

## <span data-ttu-id="8f42f-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f42f-109">PARAMETERS</span></span>

### <span data-ttu-id="8f42f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f42f-110">-DefaultProfile</span></span>
<span data-ttu-id="8f42f-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8f42f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f42f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="8f42f-112">-LabName</span></span>
<span data-ttu-id="8f42f-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die virtuellen Computer erhält.</span><span class="sxs-lookup"><span data-stu-id="8f42f-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="8f42f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f42f-114">-ResourceGroupName</span></span>
<span data-ttu-id="8f42f-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="8f42f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="8f42f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f42f-116">CommonParameters</span></span>
<span data-ttu-id="8f42f-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f42f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f42f-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f42f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f42f-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f42f-119">INPUTS</span></span>

### <span data-ttu-id="8f42f-120">System.String</span><span class="sxs-lookup"><span data-stu-id="8f42f-120">System.String</span></span>

## <span data-ttu-id="8f42f-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f42f-121">OUTPUTS</span></span>

### <span data-ttu-id="8f42f-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8f42f-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="8f42f-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f42f-123">NOTES</span></span>

## <span data-ttu-id="8f42f-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f42f-124">RELATED LINKS</span></span>

[<span data-ttu-id="8f42f-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="8f42f-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


