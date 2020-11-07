---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850055"
---
# <span data-ttu-id="c9530-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="c9530-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="c9530-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9530-102">SYNOPSIS</span></span>
<span data-ttu-id="c9530-103">Entfernt die Sicherung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c9530-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9530-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9530-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9530-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9530-105">DESCRIPTION</span></span>

## <span data-ttu-id="c9530-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9530-106">EXAMPLES</span></span>

### <span data-ttu-id="c9530-107">1:</span><span class="sxs-lookup"><span data-stu-id="c9530-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c9530-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9530-108">PARAMETERS</span></span>

### <span data-ttu-id="c9530-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9530-109">-DefaultProfile</span></span>
<span data-ttu-id="c9530-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9530-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9530-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9530-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9530-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9530-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9530-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9530-113">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9530-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9530-114">CommonParameters</span></span>
<span data-ttu-id="c9530-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9530-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9530-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9530-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9530-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9530-117">INPUTS</span></span>

### <span data-ttu-id="c9530-118">Keine</span><span class="sxs-lookup"><span data-stu-id="c9530-118">None</span></span>
<span data-ttu-id="c9530-119">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c9530-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9530-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9530-120">OUTPUTS</span></span>

### <span data-ttu-id="c9530-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c9530-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c9530-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9530-122">NOTES</span></span>

## <span data-ttu-id="c9530-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9530-123">RELATED LINKS</span></span>

