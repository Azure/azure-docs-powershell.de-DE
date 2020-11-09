---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302838"
---
# <span data-ttu-id="0a724-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="0a724-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="0a724-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a724-102">SYNOPSIS</span></span>
<span data-ttu-id="0a724-103">Ruft die Liste der Ressourcen ab, die dem angegebenen Datenträger Verschlüsselungs Satz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0a724-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="0a724-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a724-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a724-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a724-105">DESCRIPTION</span></span>
<span data-ttu-id="0a724-106">Das Cmdlet " **Get-AzDiskEncryptionSetAssociatedResource** " Ruft die Liste der Ressourcen ab, die dem angegebenen Datenträger Verschlüsselungs Satz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0a724-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="0a724-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a724-107">EXAMPLES</span></span>

### <span data-ttu-id="0a724-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a724-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="0a724-109">Das Cmdlet ruft die beiden Ressourcen "exampleDisk01" und "exampleDisk02" ab, die mit dem bereitgestellten Datenträger Verschlüsselungs Satz verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0a724-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="0a724-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a724-110">PARAMETERS</span></span>

### <span data-ttu-id="0a724-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a724-111">-DefaultProfile</span></span>
<span data-ttu-id="0a724-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a724-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a724-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="0a724-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="0a724-114">Name des Festplatten-Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="0a724-114">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="0a724-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a724-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a724-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0a724-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0a724-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a724-117">CommonParameters</span></span>
<span data-ttu-id="0a724-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a724-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a724-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a724-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a724-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a724-120">INPUTS</span></span>

### <span data-ttu-id="0a724-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0a724-121">System.String</span></span>

## <span data-ttu-id="0a724-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a724-122">OUTPUTS</span></span>

### <span data-ttu-id="0a724-123">System. Uri []</span><span class="sxs-lookup"><span data-stu-id="0a724-123">System.Uri[]</span></span>

## <span data-ttu-id="0a724-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a724-124">NOTES</span></span>

## <span data-ttu-id="0a724-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a724-125">RELATED LINKS</span></span>
