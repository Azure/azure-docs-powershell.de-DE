---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: 963e6f4621276eda4fdf598d571f2c2171dbc4f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499018"
---
# <span data-ttu-id="cbac4-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="cbac4-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="cbac4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cbac4-102">SYNOPSIS</span></span>
<span data-ttu-id="cbac4-103">Legt die Bildverweis Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="cbac4-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbac4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbac4-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <Disk> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbac4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbac4-105">DESCRIPTION</span></span>
<span data-ttu-id="cbac4-106">Das Cmdlet " **Set-AzureRmDiskImageReference** " legt die Bildverweis Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="cbac4-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="cbac4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbac4-107">EXAMPLES</span></span>

### <span data-ttu-id="cbac4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbac4-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="cbac4-109">Der erste Befehl erstellt ein lokales Datenträgerobjekt mit einer Größe von 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="cbac4-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="cbac4-110">Außerdem wird der Windows-Betriebssystemtyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cbac4-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="cbac4-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="cbac4-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="cbac4-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cbac4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cbac4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbac4-113">PARAMETERS</span></span>

### <span data-ttu-id="cbac4-114">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="cbac4-114">-Disk</span></span>
<span data-ttu-id="cbac4-115">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="cbac4-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbac4-116">-ID</span><span class="sxs-lookup"><span data-stu-id="cbac4-116">-Id</span></span>
<span data-ttu-id="cbac4-117">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="cbac4-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="cbac4-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="cbac4-118">-Lun</span></span>
<span data-ttu-id="cbac4-119">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="cbac4-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbac4-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cbac4-120">-Confirm</span></span>
<span data-ttu-id="cbac4-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbac4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbac4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbac4-122">-WhatIf</span></span>
<span data-ttu-id="cbac4-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbac4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbac4-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbac4-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbac4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbac4-125">CommonParameters</span></span>
<span data-ttu-id="cbac4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbac4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbac4-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbac4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbac4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cbac4-128">INPUTS</span></span>

### <span data-ttu-id="cbac4-129">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="cbac4-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="cbac4-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cbac4-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cbac4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cbac4-131">OUTPUTS</span></span>

### <span data-ttu-id="cbac4-132">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="cbac4-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="cbac4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="cbac4-133">NOTES</span></span>

## <span data-ttu-id="cbac4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cbac4-134">RELATED LINKS</span></span>

