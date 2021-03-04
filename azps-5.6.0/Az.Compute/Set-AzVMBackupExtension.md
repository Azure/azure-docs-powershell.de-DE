---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 7be9116814af3f11e6bd61668b77df133676ab1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949464"
---
# <span data-ttu-id="a24e3-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="a24e3-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="a24e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a24e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a24e3-103">Legt die Eigenschaften der Sicherungserweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a24e3-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="a24e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a24e3-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a24e3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a24e3-105">DESCRIPTION</span></span>

## <span data-ttu-id="a24e3-106">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a24e3-106">EXAMPLES</span></span>

### <span data-ttu-id="a24e3-107">1:</span><span class="sxs-lookup"><span data-stu-id="a24e3-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="a24e3-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a24e3-108">PARAMETERS</span></span>

### <span data-ttu-id="a24e3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24e3-109">-DefaultProfile</span></span>
<span data-ttu-id="a24e3-110">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a24e3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24e3-111">-Name</span><span class="sxs-lookup"><span data-stu-id="a24e3-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24e3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24e3-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a24e3-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="a24e3-113">-Tag</span></span>
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

### <span data-ttu-id="a24e3-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="a24e3-114">-VMName</span></span>
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

### <span data-ttu-id="a24e3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24e3-115">CommonParameters</span></span>
<span data-ttu-id="a24e3-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24e3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24e3-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a24e3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24e3-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a24e3-118">INPUTS</span></span>

### <span data-ttu-id="a24e3-119">System.String</span><span class="sxs-lookup"><span data-stu-id="a24e3-119">System.String</span></span>

## <span data-ttu-id="a24e3-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a24e3-120">OUTPUTS</span></span>

### <span data-ttu-id="a24e3-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a24e3-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a24e3-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a24e3-122">NOTES</span></span>

## <span data-ttu-id="a24e3-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a24e3-123">RELATED LINKS</span></span>
