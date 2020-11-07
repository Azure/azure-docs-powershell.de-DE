---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844660"
---
# <span data-ttu-id="2cf21-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="2cf21-101">Get-AzDisk</span></span>

## <span data-ttu-id="2cf21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cf21-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf21-103">Ruft die Eigenschaften eines verwalteten Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="2cf21-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="2cf21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cf21-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cf21-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf21-106">Das Cmdlet " **Get-AzDisk** " Ruft die Eigenschaften eines verwalteten Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="2cf21-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="2cf21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cf21-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf21-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cf21-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="2cf21-109">Dieser Befehl ruft die Eigenschaften des Datenträgers mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="2cf21-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2cf21-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2cf21-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="2cf21-111">Dieser Befehl ruft die Eigenschaften aller Datenträger in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="2cf21-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2cf21-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2cf21-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="2cf21-113">Mit diesem Befehl werden die Eigenschaften aller Datenträger unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2cf21-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="2cf21-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cf21-114">PARAMETERS</span></span>

### <span data-ttu-id="2cf21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf21-115">-DefaultProfile</span></span>
<span data-ttu-id="2cf21-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cf21-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf21-117">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="2cf21-117">-DiskName</span></span>
<span data-ttu-id="2cf21-118">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="2cf21-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="2cf21-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf21-119">-ResourceGroupName</span></span>
<span data-ttu-id="2cf21-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2cf21-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2cf21-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf21-121">CommonParameters</span></span>
<span data-ttu-id="2cf21-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf21-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf21-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf21-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf21-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cf21-124">INPUTS</span></span>

### <span data-ttu-id="2cf21-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf21-125">System.String</span></span>

## <span data-ttu-id="2cf21-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cf21-126">OUTPUTS</span></span>

### <span data-ttu-id="2cf21-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="2cf21-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2cf21-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cf21-128">NOTES</span></span>

## <span data-ttu-id="2cf21-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cf21-129">RELATED LINKS</span></span>

