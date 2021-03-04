---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 7c2a7ef4c134d811d8c30266305f25d3d53b1289
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945161"
---
# <span data-ttu-id="1db10-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="1db10-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="1db10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db10-102">SYNOPSIS</span></span>
<span data-ttu-id="1db10-103">Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="1db10-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="1db10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1db10-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1db10-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1db10-105">DESCRIPTION</span></span>
<span data-ttu-id="1db10-106">Das **Get-AzDtlVMsPerUserPolicy-Cmdlet** ruft die virtuellen Computer pro Benutzerrichtlinie einer Übung ab, wodurch Sie die maximale Anzahl von virtuellen Computern festlegen können, die pro Benutzer zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1db10-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="1db10-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die maximale Anzahl virtueller Computer zurück, die pro Benutzer zulässig sind, die Sie in der Richtlinie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="1db10-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="1db10-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1db10-108">EXAMPLES</span></span>

## <span data-ttu-id="1db10-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1db10-109">PARAMETERS</span></span>

### <span data-ttu-id="1db10-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db10-110">-DefaultProfile</span></span>
<span data-ttu-id="1db10-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1db10-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1db10-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="1db10-112">-LabName</span></span>
<span data-ttu-id="1db10-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet den virtuellen Computer pro Benutzerrichtlinie erhält.</span><span class="sxs-lookup"><span data-stu-id="1db10-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="1db10-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db10-114">-ResourceGroupName</span></span>
<span data-ttu-id="1db10-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="1db10-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="1db10-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db10-116">CommonParameters</span></span>
<span data-ttu-id="1db10-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db10-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db10-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1db10-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db10-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1db10-119">INPUTS</span></span>

### <span data-ttu-id="1db10-120">System.String</span><span class="sxs-lookup"><span data-stu-id="1db10-120">System.String</span></span>

## <span data-ttu-id="1db10-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1db10-121">OUTPUTS</span></span>

### <span data-ttu-id="1db10-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1db10-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="1db10-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1db10-123">NOTES</span></span>

## <span data-ttu-id="1db10-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1db10-124">RELATED LINKS</span></span>

[<span data-ttu-id="1db10-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="1db10-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


