---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927264"
---
# <span data-ttu-id="f92b5-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="f92b5-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="f92b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f92b5-103">Ruft die Liste der Ressourcen ab, die dem angegebenen Datenträgerverschlüsselungssatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f92b5-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="f92b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f92b5-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f92b5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f92b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f92b5-106">Das **Get-AzDiskEncryptionSetAssociatedResource-Cmdlet** ruft die Liste der Ressourcen ab, die dem angegebenen Datenträgerverschlüsselungssatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f92b5-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="f92b5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f92b5-107">EXAMPLES</span></span>

### <span data-ttu-id="f92b5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f92b5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="f92b5-109">Das Cmdlet ruft die beiden Ressourcen ab, "exampleDisk01" und "exampleDisk02", die dem bereitgestellten Datenträgerverschlüsselungssatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f92b5-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="f92b5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f92b5-110">PARAMETERS</span></span>

### <span data-ttu-id="f92b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92b5-111">-DefaultProfile</span></span>
<span data-ttu-id="f92b5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f92b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92b5-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="f92b5-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="f92b5-114">Name des Datenträgerverschlüsselungssatzs.</span><span class="sxs-lookup"><span data-stu-id="f92b5-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f92b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="f92b5-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f92b5-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f92b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92b5-117">CommonParameters</span></span>
<span data-ttu-id="f92b5-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f92b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92b5-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f92b5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92b5-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f92b5-120">INPUTS</span></span>

### <span data-ttu-id="f92b5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f92b5-121">System.String</span></span>

## <span data-ttu-id="f92b5-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f92b5-122">OUTPUTS</span></span>

### <span data-ttu-id="f92b5-123">System.Uri[]</span><span class="sxs-lookup"><span data-stu-id="f92b5-123">System.Uri[]</span></span>

## <span data-ttu-id="f92b5-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f92b5-124">NOTES</span></span>

## <span data-ttu-id="f92b5-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f92b5-125">RELATED LINKS</span></span>
