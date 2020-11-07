---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 420226346f89b480c283a190ee54f87cde2de005
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661161"
---
# <span data-ttu-id="0f22b-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="0f22b-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="0f22b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f22b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f22b-103">Ruft die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="0f22b-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="0f22b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f22b-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f22b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f22b-105">DESCRIPTION</span></span>
<span data-ttu-id="0f22b-106">Das Cmdlet " **Get-AzDtlAllowedVMSizesPolicy** " Ruft die zulässige Größen Richtlinie für virtuelle Maschinen ab, mit der Sie eine Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angeben können.</span><span class="sxs-lookup"><span data-stu-id="0f22b-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="0f22b-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und eine Liste aller zulässigen virtuellen Computer Größen zurück, die Sie in der angegebenen Richtlinie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="0f22b-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="0f22b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f22b-108">EXAMPLES</span></span>

## <span data-ttu-id="0f22b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f22b-109">PARAMETERS</span></span>

### <span data-ttu-id="0f22b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f22b-110">-DefaultProfile</span></span>
<span data-ttu-id="0f22b-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0f22b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f22b-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="0f22b-112">-LabName</span></span>
<span data-ttu-id="0f22b-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet eine Größen Richtlinie für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="0f22b-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="0f22b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f22b-114">-ResourceGroupName</span></span>
<span data-ttu-id="0f22b-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="0f22b-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0f22b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f22b-116">CommonParameters</span></span>
<span data-ttu-id="0f22b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f22b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f22b-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f22b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f22b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f22b-119">INPUTS</span></span>

### <span data-ttu-id="0f22b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="0f22b-120">System.String</span></span>

## <span data-ttu-id="0f22b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f22b-121">OUTPUTS</span></span>

### <span data-ttu-id="0f22b-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0f22b-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="0f22b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f22b-123">NOTES</span></span>

## <span data-ttu-id="0f22b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f22b-124">RELATED LINKS</span></span>

[<span data-ttu-id="0f22b-125">Satz-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="0f22b-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="0f22b-126">Azure-Entwicklungs Test Lab-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0f22b-126">Azure Development Test Lab Cmdlets</span></span>](./Az.DevTestLabs.md)


