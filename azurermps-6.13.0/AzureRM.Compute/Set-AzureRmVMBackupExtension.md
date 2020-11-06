---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: 5a8f82168db41305042e976b9daa1828b2072f95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480421"
---
# <span data-ttu-id="37732-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="37732-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="37732-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37732-102">SYNOPSIS</span></span>
<span data-ttu-id="37732-103">Legt die Eigenschaften für die Sicherungs Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="37732-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37732-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37732-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37732-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37732-105">DESCRIPTION</span></span>

## <span data-ttu-id="37732-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37732-106">EXAMPLES</span></span>

### <span data-ttu-id="37732-107">1:</span><span class="sxs-lookup"><span data-stu-id="37732-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="37732-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37732-108">PARAMETERS</span></span>

### <span data-ttu-id="37732-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37732-109">-DefaultProfile</span></span>
<span data-ttu-id="37732-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37732-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37732-111">-Name</span><span class="sxs-lookup"><span data-stu-id="37732-111">-Name</span></span>
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

### <span data-ttu-id="37732-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37732-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="37732-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="37732-113">-Tag</span></span>
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

### <span data-ttu-id="37732-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="37732-114">-VMName</span></span>
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

### <span data-ttu-id="37732-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37732-115">CommonParameters</span></span>
<span data-ttu-id="37732-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37732-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37732-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37732-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37732-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37732-118">INPUTS</span></span>

### <span data-ttu-id="37732-119">System. String</span><span class="sxs-lookup"><span data-stu-id="37732-119">System.String</span></span>

## <span data-ttu-id="37732-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37732-120">OUTPUTS</span></span>

### <span data-ttu-id="37732-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="37732-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="37732-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="37732-122">NOTES</span></span>

## <span data-ttu-id="37732-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37732-123">RELATED LINKS</span></span>
