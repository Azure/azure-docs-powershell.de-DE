---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: ae003c3c523c17db9c486edaa68d7e0991b0e6d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500054"
---
# <span data-ttu-id="8da32-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="8da32-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="8da32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8da32-102">SYNOPSIS</span></span>
<span data-ttu-id="8da32-103">Ruft die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="8da32-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8da32-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da32-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8da32-105">DESCRIPTION</span></span>
<span data-ttu-id="8da32-106">Das Cmdlet " **Get-AzureRmDtlAllowedVMSizesPolicy** " Ruft die zulässige Größen Richtlinie für virtuelle Maschinen ab, mit der Sie eine Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angeben können.</span><span class="sxs-lookup"><span data-stu-id="8da32-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="8da32-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und eine Liste aller zulässigen virtuellen Computer Größen zurück, die Sie in der angegebenen Richtlinie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="8da32-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="8da32-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8da32-108">EXAMPLES</span></span>

## <span data-ttu-id="8da32-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8da32-109">PARAMETERS</span></span>

### <span data-ttu-id="8da32-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="8da32-110">-LabName</span></span>
<span data-ttu-id="8da32-111">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet eine Größen Richtlinie für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="8da32-111">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="8da32-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da32-112">-ResourceGroupName</span></span>
<span data-ttu-id="8da32-113">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="8da32-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="8da32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da32-114">-DefaultProfile</span></span>
<span data-ttu-id="8da32-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8da32-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da32-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da32-116">CommonParameters</span></span>
<span data-ttu-id="8da32-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da32-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da32-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da32-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da32-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8da32-119">INPUTS</span></span>

## <span data-ttu-id="8da32-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8da32-120">OUTPUTS</span></span>

### <span data-ttu-id="8da32-121">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8da32-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="8da32-122">Dieses Cmdlet gibt die Richtlinie zurück, die die Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angibt.</span><span class="sxs-lookup"><span data-stu-id="8da32-122">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="8da32-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="8da32-123">NOTES</span></span>

## <span data-ttu-id="8da32-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8da32-124">RELATED LINKS</span></span>

[<span data-ttu-id="8da32-125">Satz-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="8da32-125">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="8da32-126">Azure-Entwicklungs Test Lab-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8da32-126">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


