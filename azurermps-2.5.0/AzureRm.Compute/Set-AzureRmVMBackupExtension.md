---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849687"
---
# <span data-ttu-id="03889-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="03889-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="03889-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03889-102">SYNOPSIS</span></span>
<span data-ttu-id="03889-103">Legt die Eigenschaften für die Sicherungs Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="03889-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03889-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03889-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03889-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03889-105">DESCRIPTION</span></span>

## <span data-ttu-id="03889-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03889-106">EXAMPLES</span></span>

### <span data-ttu-id="03889-107">1:</span><span class="sxs-lookup"><span data-stu-id="03889-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="03889-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03889-108">PARAMETERS</span></span>

### <span data-ttu-id="03889-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03889-109">-DefaultProfile</span></span>
<span data-ttu-id="03889-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03889-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03889-111">-Name</span><span class="sxs-lookup"><span data-stu-id="03889-111">-Name</span></span>
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

### <span data-ttu-id="03889-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03889-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="03889-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="03889-113">-Tag</span></span>
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

### <span data-ttu-id="03889-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="03889-114">-VMName</span></span>
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

### <span data-ttu-id="03889-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03889-115">CommonParameters</span></span>
<span data-ttu-id="03889-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03889-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03889-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03889-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03889-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03889-118">INPUTS</span></span>

### <span data-ttu-id="03889-119">Keine</span><span class="sxs-lookup"><span data-stu-id="03889-119">None</span></span>
<span data-ttu-id="03889-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="03889-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03889-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03889-121">OUTPUTS</span></span>

### <span data-ttu-id="03889-122">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="03889-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="03889-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="03889-123">NOTES</span></span>

## <span data-ttu-id="03889-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03889-124">RELATED LINKS</span></span>

