---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844247"
---
# <span data-ttu-id="f6fe3-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="f6fe3-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="f6fe3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fe3-103">Legt die Eigenschaften für die Sicherungs Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="f6fe3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6fe3-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6fe3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6fe3-105">DESCRIPTION</span></span>

## <span data-ttu-id="f6fe3-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6fe3-106">EXAMPLES</span></span>

### <span data-ttu-id="f6fe3-107">1:</span><span class="sxs-lookup"><span data-stu-id="f6fe3-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f6fe3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6fe3-108">PARAMETERS</span></span>

### <span data-ttu-id="f6fe3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fe3-109">-DefaultProfile</span></span>
<span data-ttu-id="f6fe3-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6fe3-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f6fe3-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6fe3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fe3-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f6fe3-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6fe3-113">-Tag</span></span>
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

### <span data-ttu-id="f6fe3-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="f6fe3-114">-VMName</span></span>
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

### <span data-ttu-id="f6fe3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fe3-115">CommonParameters</span></span>
<span data-ttu-id="f6fe3-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fe3-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fe3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fe3-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6fe3-118">INPUTS</span></span>

### <span data-ttu-id="f6fe3-119">Keine</span><span class="sxs-lookup"><span data-stu-id="f6fe3-119">None</span></span>
<span data-ttu-id="f6fe3-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6fe3-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6fe3-121">OUTPUTS</span></span>

### <span data-ttu-id="f6fe3-122">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f6fe3-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f6fe3-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6fe3-123">NOTES</span></span>

## <span data-ttu-id="f6fe3-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6fe3-124">RELATED LINKS</span></span>

