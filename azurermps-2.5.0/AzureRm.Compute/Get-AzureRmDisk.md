---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5bf1e7cb5a043afaaa4b6fd4d5e8f6820c14fbb1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849780"
---
# <span data-ttu-id="1ef6d-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1ef6d-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="1ef6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ef6d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef6d-103">Ruft die Eigenschaften eines verwalteten Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-103">Gets the properties of a Managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ef6d-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ef6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ef6d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef6d-106">Das Cmdlet " **Get-AzureRmDisk** " Ruft die Eigenschaften eines verwalteten Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-106">The **Get-AzureRmDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="1ef6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ef6d-107">EXAMPLES</span></span>

### <span data-ttu-id="1ef6d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ef6d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="1ef6d-109">Dieser Befehl ruft die Eigenschaften des Datenträgers mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1ef6d-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1ef6d-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="1ef6d-111">Dieser Befehl ruft die Eigenschaften aller Datenträger in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1ef6d-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1ef6d-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="1ef6d-113">Mit diesem Befehl werden die Eigenschaften aller Datenträger unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="1ef6d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ef6d-114">PARAMETERS</span></span>

### <span data-ttu-id="1ef6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef6d-115">-DefaultProfile</span></span>
<span data-ttu-id="1ef6d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef6d-117">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="1ef6d-117">-DiskName</span></span>
<span data-ttu-id="1ef6d-118">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="1ef6d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ef6d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ef6d-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1ef6d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef6d-121">CommonParameters</span></span>
<span data-ttu-id="1ef6d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef6d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef6d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef6d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef6d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ef6d-124">INPUTS</span></span>

### <span data-ttu-id="1ef6d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1ef6d-125">System.String</span></span>

## <span data-ttu-id="1ef6d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ef6d-126">OUTPUTS</span></span>

### <span data-ttu-id="1ef6d-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="1ef6d-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1ef6d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ef6d-128">NOTES</span></span>

## <span data-ttu-id="1ef6d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ef6d-129">RELATED LINKS</span></span>

