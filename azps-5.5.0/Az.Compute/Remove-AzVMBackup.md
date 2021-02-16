---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144801"
---
# <span data-ttu-id="474ec-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="474ec-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="474ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="474ec-102">SYNOPSIS</span></span>
<span data-ttu-id="474ec-103">Entfernt die Sicherung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="474ec-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="474ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="474ec-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="474ec-105">DESCRIPTION</span></span>

## <span data-ttu-id="474ec-106">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="474ec-106">EXAMPLES</span></span>

### <span data-ttu-id="474ec-107">1:</span><span class="sxs-lookup"><span data-stu-id="474ec-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="474ec-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="474ec-108">PARAMETERS</span></span>

### <span data-ttu-id="474ec-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474ec-109">-DefaultProfile</span></span>
<span data-ttu-id="474ec-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="474ec-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="474ec-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474ec-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="474ec-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="474ec-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="474ec-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="474ec-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="474ec-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474ec-114">CommonParameters</span></span>
<span data-ttu-id="474ec-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474ec-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474ec-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="474ec-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474ec-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="474ec-117">INPUTS</span></span>

### <span data-ttu-id="474ec-118">System.String</span><span class="sxs-lookup"><span data-stu-id="474ec-118">System.String</span></span>

## <span data-ttu-id="474ec-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="474ec-119">OUTPUTS</span></span>

### <span data-ttu-id="474ec-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="474ec-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="474ec-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="474ec-121">NOTES</span></span>

## <span data-ttu-id="474ec-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="474ec-122">RELATED LINKS</span></span>
