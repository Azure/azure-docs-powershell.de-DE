---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844396"
---
# <span data-ttu-id="1c00c-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="1c00c-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="1c00c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c00c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c00c-103">Entfernt die Sicherung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1c00c-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="1c00c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c00c-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c00c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c00c-105">DESCRIPTION</span></span>

## <span data-ttu-id="1c00c-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c00c-106">EXAMPLES</span></span>

### <span data-ttu-id="1c00c-107">1:</span><span class="sxs-lookup"><span data-stu-id="1c00c-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1c00c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c00c-108">PARAMETERS</span></span>

### <span data-ttu-id="1c00c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c00c-109">-DefaultProfile</span></span>
<span data-ttu-id="1c00c-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c00c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c00c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c00c-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1c00c-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c00c-112">-Tag</span></span>
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

### <span data-ttu-id="1c00c-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="1c00c-113">-VMName</span></span>
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

### <span data-ttu-id="1c00c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c00c-114">CommonParameters</span></span>
<span data-ttu-id="1c00c-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c00c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c00c-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c00c-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c00c-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c00c-117">INPUTS</span></span>

### <span data-ttu-id="1c00c-118">Keine</span><span class="sxs-lookup"><span data-stu-id="1c00c-118">None</span></span>
<span data-ttu-id="1c00c-119">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1c00c-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c00c-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c00c-120">OUTPUTS</span></span>

### <span data-ttu-id="1c00c-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1c00c-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1c00c-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c00c-122">NOTES</span></span>

## <span data-ttu-id="1c00c-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c00c-123">RELATED LINKS</span></span>

