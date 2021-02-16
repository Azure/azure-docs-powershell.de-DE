---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148953"
---
# <span data-ttu-id="13578-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="13578-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="13578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13578-102">SYNOPSIS</span></span>
<span data-ttu-id="13578-103">Ruft die Liste der Ressourcen ab, die dem angegebenen Datenträgerverschlüsselungssatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="13578-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="13578-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13578-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13578-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13578-105">DESCRIPTION</span></span>
<span data-ttu-id="13578-106">Das **Cmdlet "Get-AzDiskEncryptionSetAssociatedResource"** ruft die Liste der Ressourcen ab, die dem angegebenen Datenträgerverschlüsselungssatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="13578-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="13578-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13578-107">EXAMPLES</span></span>

### <span data-ttu-id="13578-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13578-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="13578-109">Das Cmdlet ruft die beiden Ressourcen "exampleDisk01" und "exampleDisk02" ab, die dem bereitgestellten Datenträgerverschlüsselungssatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="13578-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="13578-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13578-110">PARAMETERS</span></span>

### <span data-ttu-id="13578-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13578-111">-DefaultProfile</span></span>
<span data-ttu-id="13578-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13578-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13578-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="13578-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="13578-114">Name des Datenträgerverschlüsselungssatzs.</span><span class="sxs-lookup"><span data-stu-id="13578-114">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="13578-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13578-115">-ResourceGroupName</span></span>
<span data-ttu-id="13578-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="13578-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="13578-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13578-117">CommonParameters</span></span>
<span data-ttu-id="13578-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13578-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13578-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13578-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13578-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13578-120">INPUTS</span></span>

### <span data-ttu-id="13578-121">System.String</span><span class="sxs-lookup"><span data-stu-id="13578-121">System.String</span></span>

## <span data-ttu-id="13578-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13578-122">OUTPUTS</span></span>

### <span data-ttu-id="13578-123">System.URI[]</span><span class="sxs-lookup"><span data-stu-id="13578-123">System.Uri[]</span></span>

## <span data-ttu-id="13578-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13578-124">NOTES</span></span>

## <span data-ttu-id="13578-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13578-125">RELATED LINKS</span></span>
