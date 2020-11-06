---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481350"
---
# <span data-ttu-id="08b4f-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="08b4f-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="08b4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="08b4f-103">Konvertieren von Hyper-V VM in Azure unterstützte virtuelle Festplatten-Dateien</span><span class="sxs-lookup"><span data-stu-id="08b4f-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08b4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b4f-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="08b4f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="08b4f-106">Konvertieren von Hyper-V VM in Azure unterstützte virtuelle Festplatten-Dateien</span><span class="sxs-lookup"><span data-stu-id="08b4f-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="08b4f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08b4f-107">EXAMPLES</span></span>

### <span data-ttu-id="08b4f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08b4f-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="08b4f-109">Konvertieren Sie die Hyper-V-VM mit dem Namen "Test" in Azure unterstützte virtuelle Festplatten-Dateien in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="08b4f-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="08b4f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08b4f-110">PARAMETERS</span></span>

### <span data-ttu-id="08b4f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08b4f-111">-AsJob</span></span>
<span data-ttu-id="08b4f-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="08b4f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b4f-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="08b4f-113">-ExportPath</span></span>
<span data-ttu-id="08b4f-114">Der Exportordner Pfad, in dem die Datenträgerdateien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="08b4f-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b4f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="08b4f-115">-Force</span></span>
<span data-ttu-id="08b4f-116">Erzwingen des Exports, auch wenn vorhandener Ordner gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="08b4f-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b4f-117">-Vserver</span><span class="sxs-lookup"><span data-stu-id="08b4f-117">-HyperVServer</span></span>
<span data-ttu-id="08b4f-118">Der Hyper-V-Server-DNS-Name mit "localhost" als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="08b4f-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b4f-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="08b4f-119">-HyperVVMName</span></span>
<span data-ttu-id="08b4f-120">Der Name des Hyper-V-namens.</span><span class="sxs-lookup"><span data-stu-id="08b4f-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b4f-121">CommonParameters</span></span>
<span data-ttu-id="08b4f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b4f-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b4f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b4f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08b4f-124">INPUTS</span></span>

### <span data-ttu-id="08b4f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="08b4f-125">System.String</span></span>

## <span data-ttu-id="08b4f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08b4f-126">OUTPUTS</span></span>

### <span data-ttu-id="08b4f-127">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="08b4f-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="08b4f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="08b4f-128">NOTES</span></span>

## <span data-ttu-id="08b4f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08b4f-129">RELATED LINKS</span></span>

