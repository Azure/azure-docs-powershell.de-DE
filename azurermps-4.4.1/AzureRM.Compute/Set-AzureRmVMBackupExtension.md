---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: d95ef152ed21439aafdc1cf9778b101473539b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477238"
---
# <span data-ttu-id="b3e1e-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="b3e1e-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="b3e1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e1e-103">Legt die Eigenschaften für die Sicherungs Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="b3e1e-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3e1e-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3e1e-105">DESCRIPTION</span></span>

## <span data-ttu-id="b3e1e-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3e1e-106">EXAMPLES</span></span>

### <span data-ttu-id="b3e1e-107">1:</span><span class="sxs-lookup"><span data-stu-id="b3e1e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b3e1e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3e1e-108">PARAMETERS</span></span>

### <span data-ttu-id="b3e1e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e1e-109">-DefaultProfile</span></span>
<span data-ttu-id="b3e1e-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3e1e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e1e-111">-Name</span><span class="sxs-lookup"><span data-stu-id="b3e1e-111">-Name</span></span>
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

### <span data-ttu-id="b3e1e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e1e-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b3e1e-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3e1e-113">-Tag</span></span>
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

### <span data-ttu-id="b3e1e-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="b3e1e-114">-VMName</span></span>
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

### <span data-ttu-id="b3e1e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e1e-115">CommonParameters</span></span>
<span data-ttu-id="b3e1e-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e1e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e1e-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e1e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e1e-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3e1e-118">INPUTS</span></span>

## <span data-ttu-id="b3e1e-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3e1e-119">OUTPUTS</span></span>

## <span data-ttu-id="b3e1e-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3e1e-120">NOTES</span></span>

## <span data-ttu-id="b3e1e-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3e1e-121">RELATED LINKS</span></span>

