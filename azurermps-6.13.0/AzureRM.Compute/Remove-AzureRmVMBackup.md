---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: cb28249d5c32119d187becd8b07f2137f3f312d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662323"
---
# <span data-ttu-id="9651f-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="9651f-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="9651f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9651f-102">SYNOPSIS</span></span>
<span data-ttu-id="9651f-103">Entfernt die Sicherung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9651f-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9651f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9651f-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9651f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9651f-105">DESCRIPTION</span></span>

## <span data-ttu-id="9651f-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9651f-106">EXAMPLES</span></span>

### <span data-ttu-id="9651f-107">1:</span><span class="sxs-lookup"><span data-stu-id="9651f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9651f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9651f-108">PARAMETERS</span></span>

### <span data-ttu-id="9651f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9651f-109">-DefaultProfile</span></span>
<span data-ttu-id="9651f-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9651f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9651f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9651f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9651f-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="9651f-112">-Tag</span></span>
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

### <span data-ttu-id="9651f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="9651f-113">-VMName</span></span>
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

### <span data-ttu-id="9651f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9651f-114">CommonParameters</span></span>
<span data-ttu-id="9651f-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9651f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9651f-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9651f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9651f-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9651f-117">INPUTS</span></span>

### <span data-ttu-id="9651f-118">System. String</span><span class="sxs-lookup"><span data-stu-id="9651f-118">System.String</span></span>

## <span data-ttu-id="9651f-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9651f-119">OUTPUTS</span></span>

### <span data-ttu-id="9651f-120">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9651f-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9651f-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="9651f-121">NOTES</span></span>

## <span data-ttu-id="9651f-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9651f-122">RELATED LINKS</span></span>
