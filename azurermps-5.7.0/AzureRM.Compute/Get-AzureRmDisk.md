---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497737"
---
# <span data-ttu-id="94e32-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="94e32-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="94e32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94e32-102">SYNOPSIS</span></span>
<span data-ttu-id="94e32-103">Ruft die Eigenschaften eines Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="94e32-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94e32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94e32-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="94e32-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94e32-105">DESCRIPTION</span></span>
<span data-ttu-id="94e32-106">Das Cmdlet " **Get-AzureRmDisk** " Ruft die Eigenschaften eines Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="94e32-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="94e32-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94e32-107">EXAMPLES</span></span>

### <span data-ttu-id="94e32-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94e32-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="94e32-109">Dieser Befehl ruft die Eigenschaften des Datenträgers mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="94e32-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="94e32-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="94e32-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="94e32-111">Dieser Befehl ruft die Eigenschaften aller Datenträger in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="94e32-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="94e32-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="94e32-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="94e32-113">Mit diesem Befehl werden die Eigenschaften aller Datenträger unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="94e32-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="94e32-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="94e32-114">PARAMETERS</span></span>

### <span data-ttu-id="94e32-115">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="94e32-115">-DiskName</span></span>
<span data-ttu-id="94e32-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="94e32-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e32-117">-ResourceGroupName</span></span>
<span data-ttu-id="94e32-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="94e32-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e32-119">CommonParameters</span></span>
<span data-ttu-id="94e32-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e32-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e32-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e32-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94e32-122">INPUTS</span></span>

### <span data-ttu-id="94e32-123">System. String</span><span class="sxs-lookup"><span data-stu-id="94e32-123">System.String</span></span>

## <span data-ttu-id="94e32-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94e32-124">OUTPUTS</span></span>

### <span data-ttu-id="94e32-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="94e32-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="94e32-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="94e32-126">NOTES</span></span>

## <span data-ttu-id="94e32-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94e32-127">RELATED LINKS</span></span>

